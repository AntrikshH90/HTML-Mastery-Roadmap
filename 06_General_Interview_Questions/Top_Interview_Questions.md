# 🎯 Top General HTML Interview Questions

When applying for Frontend or Full-Stack roles, recruiters often use extremely fast-paced screening questions to verify you deeply understand the browser. Below is a curated list of rapid-fire technical questions frequently asked in tier-1 technical interviews.

---

### **1. What is the fundamental difference between HTML elements and tags?**
* **Answer:** An HTML *tag* is strictly the characters inside the angle brackets (e.g., `<h1>` or `</h1>`), whereas the *element* is the everything combined: the opening tag, the content inside it, and the closing tag (e.g., `<h1>Hello World</h1>`).

### **2. Are the HTML tags `<b>` and `<strong>` exactly the same?**
* **Answer:** No. Visually, they both render text bold. However, semantically, `<b>` just means "physically bold this text for style", whereas `<strong>` means "this text carries critical semantic importance". Screen readers ignore `<b>` but will explicitly emphasize `<strong>` text out loud.

### **3. Explain what a generic "Block-level" element vs an "Inline" element is natively.**
* **Answer:** 
  * A **Block-level** element (like `<div>`, `<h1>`, `<p>`, `<ul>`) strictly starts on a completely new line and forces itself to stretch the entire 100% width of its parent container.
  * An **Inline** element (like `<span>`, `<a>`, `<img>`, `<strong>`) strictly only takes up as much horizontal width as absolutely necessary to wrap its content and does not break the line below it.

### **4. How does the browser natively handle formatting, like multiple spaces or line breaks (`\n`) in your raw HTML code?**
* **Answer:** The browser ignores them completely! This is called **White Space Collapse**. If you type 10 spaces or 5 enter-key returns in your HTML file, the browser renders it visually as exactly one single space. To explicitly force spaces, you must use HTML entities like `&nbsp;` (Non-Breaking Space) or the `<br>` block-return tag.

### **5. What is the `iframe` element used for today? What are its massive security risks?**
* **Answer:** An `<iframe>` natively embeds an entirely separate HTML document from another server directly into the current webpage (e.g., embedding a YouTube player or Google Maps). The massive security risk is **Clickjacking**, where an attacker embeds your bank website into an invisible iframe layered directly over a fake "Win a Prize" button.

### **6. Can you nest an `<a>` tag inside another `<a>` tag?**
* **Answer:** It is strictly illegal according to the W3C HTML5 Specification! You cannot nest interactive links inside other interactive links. Browsers will silently break the DOM or forcibly close the anchor tag prematurely.

### **7. What specifically is the HTML DOM?**
* **Answer:** The DOM stands for the Document Object Model. HTML is just the static text file saved on your hard drive. When the browser downloads the HTML string, it converts every single tag into a living, nested JavaScript Object tree called the DOM. JavaScript then mutates the DOM, *not* the raw HTML file.

### **8. Why we use `data-` attributes in HTML5? Why not just make up our own attributes like `<div my-custom-id="5">`?**
* **Answer:** Making up custom attributes strictly violates HTML specification, causes W3C validation to fail, and runs the massive risk of colliding with future official HTML tags. The `data-*` attribute is the universally agreed, highly secure prefix strictly designed to pass raw data to JavaScript securely via `HTMLElement.dataset`.

### **9. If a page contains two elements with the same exact `id`, what does the browser do?**
* **Answer:** Identifiers must be strictly unique globally per window! If you have multiple identical IDs, the browser silently allows the CSS to apply to all of them, but `document.getElementById()` in JavaScript will silently crash logic by ONLY ever returning the very first element it detects in the DOM tree, ignoring the rest!

### **10. What is a Favicon, and how do you explicitly inject it natively into HTML?**
* **Answer:** A Favicon (Favorite Icon) is the tiny 16x16 or 32x32 image logo displayed on the browser Tab next to the page `<title>`. You strictly inject it in the `<head>` tag:
`<link rel="icon" type="image/x-icon" href="/favicon.ico">`
