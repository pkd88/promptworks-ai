Project Foundation Document 1: The Resilience Blueprint
Topic: DOM Stability & MutationObservers
Status: Approved for Implementation
Version: 1.0
1. Executive Summary
This document establishes the protocol for interacting with the Document Object Model (DOM). Standard userscripts often fail because they attempt to access elements that have not yet loaded (race conditions) or use inefficient polling methods (setInterval) that degrade performance. This blueprint mandates the use of MutationObservers wrapped in Promises to ensure scripts never "give up" and never slow down the host machine.
2. Required Metadata
The following metadata configuration is required for any script operating under this blueprint to ensure correct execution timing.

JavaScript


// ==UserScript==// @run-at      document-start// ==/UserScript==
@run-at document-start: Essential. We do not wait for DOMContentLoaded because modern SPAs (Single Page Applications) load content asynchronously long after the initial document is ready. We start the observer immediately.
3. Validation Logic & Standard Pattern
The core validation mechanism is the waitForElm utility. This function validates the existence of an element before allowing the script to proceed.
3.1 The Utility Function
Standard: All scripts must include this utility to replace document.querySelector for dynamic elements.

JavaScript


/** * Waits for an element to appear in the DOM using MutationObserver. * Validates existence immediately, then observes changes if not found. * @param {string} selector - The CSS selector to wait for * @returns {Promise<Element>} - Resolves with the found element */function waitForElm(selector) {    return new Promise(resolve => {        // Validation 1: Check if element already exists (Immediate resolution)        const existingElement = document.querySelector(selector);        if (existingElement) {            return resolve(existingElement);        }        // Validation 2: Observe DOM for new nodes        const observer = new MutationObserver(mutations => {            const targetElement = document.querySelector(selector);            if (targetElement) {                observer.disconnect(); // CRITICAL: Stop observing to save memory                resolve(targetElement);            }        });        // Configuration: recursive subtree check is required for SPAs        observer.observe(document.body, {            childList: true,            subtree: true        });    });}
3.2 Implementation Strategy
Code must not execute until validation passes.

JavaScript


// BAD Pattern (Fragile)// const btn = document.querySelector('.submit-btn');// btn.click(); // Fails if button loads 1ms later// GOOD Pattern (Resilient)(async function() {    console.log('Script started, waiting for button...');        // The script pauses here until validation passes (element exists)    const btn = await waitForElm('.submit-btn');        console.log('Validation passed. Element found:', btn);    btn.click();})();
4. Performance Constraints
Observer Cleanup: The observer.disconnect() call inside the utility is mandatory. Leaving observers running indefinitely causes memory leaks.
Scope Limitation: While document.body is used for generic waiting, specific observers should target the nearest stable parent container whenever possible to reduce CPU load[1].