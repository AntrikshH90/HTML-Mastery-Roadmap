# 🔴 Advanced HTML: Answer Key & Detailed Theory

This sheet contains senior-level technical theoretical answers focusing on HTML5 APIs, DOM performance, and rendering logics.

---

## 📌 Q1. What are ARIA roles, and why do we use them when building a modern web application?
**Answer:**
ARIA stands for **Accessible Rich Internet Applications**. It is a set of specific HTML attributes (`role`, `aria-label`, `aria-hidden`) created by the W3C. 

When you build complex web applications using JavaScript (like custom dropdown menus or dynamic pop-up modals using `<div>`), normal HTML semantics fail. Screen readers have no idea that a `<div>` is suddenly acting as a button or an alert. ARIA attributes explicitly define the JavaScript component's behavior to assistive technologies without fundamentally changing how the browser visually renders the code.
* Example: `<div role="button" aria-pressed="false" tabindex="0">Save Form</div>` tells the screen reader this element behaves precisely like a clickable button.

---

## 📌 Q2. Explain Custom Data Attributes (`data-*`). How are they used to bridge the gap between HTML and JavaScript?
**Answer:**
The `data-*` attribute is an HTML5 specification allowing developers to securely store extra, hidden information on standard, semantic HTML elements without needing non-standard attributes or extra DOM properties.
* Example: `<button data-user-action="submitForm" data-user-id="9871">Submit</button>`

**How they bridge the gap:**
JavaScript can seamlessly access these attributes via the DOM's strictly typed `.dataset` property.
`const userId = document.querySelector('button').dataset.userId; // Returns "9871"`
This is crucial for modern frameworks, React bindings, and vanilla UI tracking because it keeps data securely embedded in the front-end layout without sending it to the server!

---

## 📌 Q3. What is the fundamental rendering difference between the `<canvas>` element and the `<svg>` tag? When should you use each?
**Answer:**
* **`<canvas>`:** A resolution-dependent bitmap canvas entirely controlled pixel-by-pixel using the JavaScript rendering API. 
* **`<svg>` (Scalable Vector Graphics):** A resolution-independent vector graphic completely built using mathematical XML code representing shapes (like circles, paths).

**When to use:**
Use **SVG** when rendering highly detailed logos, UI icons, or simple interactive charts that must easily scale infinitely on a retina display without losing quality.
Use **Canvas** when building a heavy 60FPS browser video game, applying live image filters, or parsing 10,000 data points continuously. SVG slows down massively with thousands of objects because every path becomes a DOM element; Canvas does not impact the DOM tree.

---

## 📌 Q4. Write the exact `<meta>` tags required to ensure a webpage is purely responsive on all mobile devices and correctly optimized for search engines.
**Answer:**
```html
<head>
    <!-- Base character encoding parsing -->
    <meta charset="UTF-8">
    
    <!-- STRICTLY forces the mobile device viewport to scale logically to screen dimension! -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- SEO specific -->
    <meta name="description" content="A highly optimized website teaching HTML theory.">
    <meta name="keywords" content="html, coding, web development">
    <meta name="author" content="Antriksh Yadav">
</head>
```
💡 **Interview Tip:** Missing the `<meta name="viewport">` tag completely breaks media queries in CSS. The website will incorrectly zoom out like a tiny desktop on a mobile phone!

---

## 📌 Q5. What is the difference between `localStorage` and `sessionStorage` in HTML5 Web Storage?
**Answer:**
Both APIs allow developers to safely store key/value string pairs directly inside the user's browser (up to 5MB natively without using cookies).
- **`localStorage`**: The data has absolutely NO expiration date. The data remains stored forever inside that browser globally until the user manually invokes the browser settings to clear their cache or the script uses `localStorage.clear()`.
- **`sessionStorage`**: The data is strictly isolated to the exact active browser TAB or WINDOW. The instant the user closes that tab, ALL data is entirely wiped from existence.

---

## 📌 Q6. How does the `defer` and `async` attribute work on a `<script>` tag, and which one is strictly best for performance when loading independent third-party scripts?
**Answer:**
* **Normal `<script>`:** The HTML parser pauses, perfectly locks up, downloads the script, executes it, and ONLY THEN goes back to rendering the HTML page. (Causes massive lag).
* **`defer`:** The HTML parser keeps perfectly running, downloads the script in the background simultaneously, but WAITs to execute the script until the entire HTML DOM is 100% loaded. **Use this when the script depends on the HTML existing (like manipulating buttons).**
* **`async`:** The HTML parser keeps running, downloads the script simultaneously, and the absolute millisecond it finishes downloading, it pauses the HTML and executes the script. 

**Best for independent scripts (e.g., Google Analytics)?**
Strictly **`async`**. Because it does not care about what state the DOM is in, it simply runs in the background whenever it can, zero-blocking the layout render.
