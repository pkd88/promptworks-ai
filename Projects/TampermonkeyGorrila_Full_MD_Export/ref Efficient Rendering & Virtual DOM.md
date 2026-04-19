Project Foundation Document 5: The Performance Code
Topic: Efficient Rendering & Virtual DOM
Status: Approved for Implementation
Version: 1.0
1. Executive Summary
Directly manipulating the DOM (e.g., innerHTML +=) causes "Layout Thrashing" and makes the page feel choppy. The Performance Code requires the use of a lightweight Virtual DOM (Preact) loaded via CDN. This allows us to inject complex UIs (menus, buttons, dashboards) that update smoothly without freezing the browser.
2. Required Metadata
We use @require to pull in Preact and HTM (Hyperscript Tagged Markup) so we can write React-like code without a build step (no Webpack needed).

JavaScript


// ==UserScript==// @require     https://unpkg.com/htm@3.1.1/dist/htm.umd.js// @require     https://unpkg.com/preact@10.19.3/dist/preact.umd.js// ==/UserScript==
3. Validation Logic & Component System
The validation here involves ensuring the UI mounts only once and updates efficiently via the Virtual DOM.
3.1 The No-Build Setup
This boilerplate initializes the Preact environment within the userscript.

JavaScript


// Bind htm to preactconst html = htm.bind(preact.h);const { render, useState, useEffect } = preact;// Validation: Prevent multiple UI injectionsif (document.getElementById('tm-gorilla-ui-root')) {    console.warn('UI already exists. Aborting re-injection.');    return;}// Create a shadow host to isolate our CSS from the site's CSSconst host = document.createElement('div');host.id = 'tm-gorilla-ui-root';document.body.appendChild(host);const shadow = host.attachShadow({ mode: 'open' });
3.2 The Efficient UI Component
This pattern batches updates. Clicking the button 50 times in a second won't trigger 50 layout reflows; the Virtual DOM handles the diffing.

JavaScript


function GorillaPanel() {    const [count, setCount] = useState(0);    // Efficiently updates only the text node, not the whole container    return html`        <div style="            position: fixed;             top: 10px; right: 10px;             background: #222; color: #fff;             padding: 15px;             border-radius: 8px;            z-index: 99999;            box-shadow: 0 4px 6px rgba(0,0,0,0.3);            font-family: sans-serif;        ">            <h3>🦍 Control Panel</h3>            <p>Status: Active</p>            <p>Clicks: ${count}</p>            <button onclick=${() => setCount(count + 1)} style="                background: #4CAF50; border: none; padding: 8px 12px; color: white; cursor: pointer;            ">                Boost Performance            </button>        </div>    `;}// Mount the apprender(html`<${GorillaPanel} />`, shadow);
4. Best Practices
Isolation: Always mount the Preact app inside a Shadow DOM (as shown above) to prevent the website's CSS from breaking your UI.
Batching: Do not use setInterval to update the UI. Use useState and let Preact handle the rendering cycle.