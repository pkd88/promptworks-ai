Project Foundation Document 3: The Safe & Vault Manual
Topic: GM_Storage & Data Persistence
Status: Approved for Implementation
Version: 1.0
1. Executive Summary
Browser localStorage is volatile; it can be cleared by the user or the site at any time. The "Safe & Vault" manual mandates the use of the Greasemonkey/Tampermonkey storage API (GM_setValue/GM.setValue) to create a persistent layer that survives cache clearing and browser restarts.
2. Required Metadata
The script must explicitly request storage permissions. Note the inclusion of both GM_ (synchronous) and GM. (asynchronous/modern) grants for compatibility.

JavaScript


// ==UserScript==// @grant       GM_setValue// @grant       GM_getValue// @grant       GM.setValue// @grant       GM.getValue// ==/UserScript==
3. Validation Logic & Abstraction
Directly calling GM_setValue is risky due to API differences between engines (e.g., Greasemonkey 4 vs. Tampermonkey). We implement a "Vault" class to handle validation and serialization.
3.1 The Vault Class
This class validates that data is stored correctly and handles type safety (JSON serialization).

JavaScript


class Vault {    constructor(prefix = "TG_") {        this.prefix = prefix;    }    /**     * Saves a value securely.     * @param {string} key      * @param {any} value      */    async save(key, value) {        const fullKey = this.prefix + key;        const serialized = JSON.stringify(value);                // Validation: Check which API is available        if (typeof GM!== 'undefined' && GM.setValue) {            await GM.setValue(fullKey, serialized);        } else if (typeof GM_setValue!== 'undefined') {            GM_setValue(fullKey, serialized);        } else {            console.warn("Vault Error: No persistence API found. Falling back to localStorage.");            localStorage.setItem(fullKey, serialized);        }    }    /**     * Retrieves a value with a default fallback.     * @param {string} key      * @param {any} defaultValue      */    async load(key, defaultValue) {        const fullKey = this.prefix + key;        let serialized;        if (typeof GM!== 'undefined' && GM.getValue) {            serialized = await GM.getValue(fullKey);        } else if (typeof GM_getValue!== 'undefined') {            serialized = GM_getValue(fullKey);        } else {            serialized = localStorage.getItem(fullKey);        }        // Validation: Ensure data is not undefined/null        if (serialized === undefined || serialized === null) {            return defaultValue;        }        try {            return JSON.parse(serialized);        } catch (e) {            console.error("Vault Validation Error: Corrupt data", e);            return defaultValue;        }    }}
4. Usage Pattern

JavaScript


const configVault = new Vault("MyScript_");// Save settingsawait configVault.save("user_preferences", { theme: "dark", autoScroll: true });// Load settings (survives browser restart)const prefs = await configVault.load("user_preferences", { theme: "light", autoScroll: false });