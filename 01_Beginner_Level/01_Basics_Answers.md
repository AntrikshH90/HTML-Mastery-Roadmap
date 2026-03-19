# 🟢 Beginner HTML: Answer Key & Detailed Theory

This sheet contains high-quality, interview-ready answers to the beginner questions. Use this to study, memorize syntax, and understand the "why" behind the code.

## 📌 Q1. What is HTML? Explain its core purpose in web development.
**Answer:**
HTML stands for **HyperText Markup Language**. It is the standard markup language used to create the structure and framework of a webpage. 

* **Metaphor:** If a website were a house, HTML is the concrete foundation and the wooden framing. CSS would be the paint and interior design, and JavaScript would be the electricity and plumbing.
* **Core Purpose:** HTML tells the browser *what* content is on the page (e.g., "This is a paragraph", "This is a heading", "This is an image link").

---

## 📌 Q2. Write out the standard boilerplate (skeleton) of an HTML5 document.
**Answer:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My First Website</title>
</head>
<body>
  <h1>Welcome to my website</h1>
</body>
</html>
```

💡 **Trick:** If you use VS Code, you can type `!` and hit `Enter` (Emmet abbreviation) to auto-generate this entire skeleton instantly!
* **Interview Tip:** Always explain that `<!DOCTYPE html>` at the very top is crucial because it tells the browser we are running HTML5, preventing older browsers from breaking.

---

## 📌 Q3. What is the difference between `<head>` and `<body>` tags?
**Answer:**
- **`<head>`**: Contains the *metadata* of the website. Nothing in the head tag is actually visible on the main screen of the webpage. This is where you put your CSS links, font links, SEO data, and the browser tab `<title>`.
- **`<body>`**: Contains the *content* of the website. Everything you visually see on a webpage (buttons, images, forms, text) lives inside the body tags.

---

## 📌 Q4. List 3 text formatting tags and explain what they do.
**Answer:**
1. **`<strong>`**: Makes text bold. It also semantically indicates to screen readers that the text is strictly important. (Unlike `<b>`, which just makes it physically bold).
2. **`<em>`**: Italicizes text and emphasizes it semantically.
3. **`<s>`**: Renders text with a strikethrough (a line through the middle), often used to indicate deleted, outdated, or discounted content.

---

## 📌 Q5. How do you create a hyperlink that opens in a NEW tab? Write the exact code.
**Answer:**
```html
<a href="https://github.com/AntrikshH90" target="_blank">Click here to view my GitHub</a>
```

💡 **Security Trick:** When using `target="_blank"`, it is best practice to also include `rel="noopener noreferrer"`. This prevents the newly opened tab from exploiting potential security flaws in the original window's API.
**Professional Example:**
```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">Secure Link</a>
```

---

## 📌 Q6. How do you insert an image? Explain the importance of the `alt` attribute.
**Answer:**
```html
<img src="profile_photo.jpg" alt="A headshot of Antriksh wearing a blue tie">
```

**Interview Answer & Importance of `alt`:**
1. **Accessibility (Screen Readers):** Visually impaired users rely on software to read the webpage out loud. The software reads the `alt` text to them.
2. **SEO (Search Engine Optimization):** Google cannot "see" images. Its algorithm reads the `alt` text to index what your image is about.
3. **Fallback:** If the user has a slow connection or the image link breaks, the `alt` text displays in place of the broken image.
