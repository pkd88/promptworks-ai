Project Foundation Document 4: The Border Crossing Protocol
Topic: CORS Evasion & Cross-Origin Requests
Status: Approved for Implementation
Version: 1.0
1. Executive Summary
Web pages are restricted by the Same-Origin Policy (SOP). They cannot fetch data from api.weather.com if the user is on google.com. This protocol uses the GM_xmlhttpRequest API to tunnel through the browser's extension layer, bypassing SOP and CORS headers entirely.
2. Required Metadata
Strict security whitelisting is required. You must declare exactly which domains you intend to "cross borders" into using @connect.

JavaScript


// ==UserScript==// @grant       GM_xmlhttpRequest// @grant       GM.xmlHttpRequest// @connect     api.example.com// @connect     www.google.com// ==/UserScript==
3. Validation Logic & Wrapper
The raw GM_xmlhttpRequest API uses outdated callbacks (onload). We use a secureFetch wrapper that returns a Promise and validates HTTP status codes.
3.1 The secureFetch Wrapper

JavaScript


/** * Performs a cross-origin network request. * @param {string} url - The destination URL * @param {object} options - Request options (method, headers, body) * @returns {Promise<string>} - The response text */function secureFetch(url, options = {}) {    return new Promise((resolve, reject) => {        const requestDetails = {            method: options.method || 'GET',            url: url,            headers: options.headers || {},            data: options.body,            onload: (response) => {                // Validation: Check for HTTP success codes (200-299)                if (response.status >= 200 && response.status < 300) {                    resolve(response.responseText);                } else {                    reject(new Error(`Border Crossing Error: HTTP ${response.status} ${response.statusText}`));                }            },            onerror: (err) => {                reject(new Error("Network Error: Request failed completely. Check @connect permissions."));            },            onabort: () => reject(new Error("Request Aborted"))        };        // Environment Detection        if (typeof GM!== 'undefined' && GM.xmlHttpRequest) {            GM.xmlHttpRequest(requestDetails);        } else {            GM_xmlhttpRequest(requestDetails);        }    });}
4. Usage Example
This allows the script to grab data from a completely different website.

JavaScript


async function getPriceData() {    try {        console.log("Initiating Border Crossing...");        const data = await secureFetch('https://api.example.com/prices');        const json = JSON.parse(data);        console.log("Data successfully retrieved across origins:", json);    } catch (e) {        console.error("Crossing Denied:", e);    }}