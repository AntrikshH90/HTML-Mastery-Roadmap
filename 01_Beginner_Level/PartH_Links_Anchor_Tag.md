# 🅷 PART H: LINKS & ANCHOR TAG

## 📖 Theory (from PDF)

> HTML links are a powerful way to allow **seamless navigation** of pages on your website. When a user clicks on the link, the browser automatically follows it and loads the link URL.
> 
> To insert links in the webpage we have to use the **`<a>` tag**. The anchor tag is used to create hyperlinks. It allows users to navigate from one page to another or to different sections of the same page.

## Anchor Tag Attributes (from PDF)

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `href` | Used to specify the link. Specifies the destination URL (external link, internal page, or anchor within same page) |
| `target` | Used to specify where link should be opened. Values: `_blank`, `_parent`, `_self`, `_top` |
| `download` | Used to specify the target file if you want to add download file feature |
| `title` | Provides additional information about the link, displayed as a tooltip when user hovers over link |

## Target Attribute Values Explained

| Value | Description |
|-------|-------------|
| `_self` | Opens in same window/tab **(default)** |
| `_blank` | Opens in a **new** tab or window |
| `_parent` | Opens in parent frame |
| `_top` | Opens in full body of window |

## All Types of Links

```html
<!-- 1. Basic link -->
<a href="https://google.com">Go to google.com</a>

<!-- 2. Open in new tab -->
<a href="https://google.com" target="_blank" rel="noopener noreferrer">
    Google (New Tab)
</a>

<!-- 3. Link to another page on same site -->
<a href="about.html">About Us</a>
<a href="pages/contact.html">Contact</a>

<!-- 4. Link to section on SAME page (anchor/bookmark) -->
<a href="#section1">Go to Section 1</a>
<!-- ... further down the page ... -->
<h2 id="section1">Section 1</h2>

<!-- 5. Email link -->
<a href="mailto:hello@example.com">Send Email</a>

<!-- 6. Phone link -->
<a href="tel:+1234567890">Call Us</a>

<!-- 7. Download link -->
<a href="files/resume.pdf" download>Download Resume</a>
<a href="files/resume.pdf" download="my-resume">Download with custom name</a>

<!-- 8. Link with tooltip -->
<a href="https://mdn.dev" title="Mozilla Developer Network">MDN</a>

<!-- 9. Image as link (from PDF) -->
<a href="https://www.google.com">
    <img src="icon.jpg" alt="Google Icon">
</a>

<!-- 10. Displaying image via link (from PDF) -->
<a href="nature.jpg">View Image</a>

<!-- 11. Back to top -->
<a href="#">Back to Top ↑</a>
```

## Link Example from PDF (Page 9)

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Links</title>
</head>
<body>
    <section>
        <a href="https://google.com">
            Go to google.com
        </a>
    </section>
</body>
</html>
```

## Navigation Best Practice

```html
<nav aria-label="Main Navigation">
    <ul>
        <li><a href="/" aria-current="page">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/services">Services</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>
```

> ⚠️ **Security Tip:** Always use `rel="noopener noreferrer"` with `target="_blank"` to prevent security vulnerabilities (tab hijacking).

---

