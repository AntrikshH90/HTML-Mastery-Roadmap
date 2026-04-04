# ❓ COMPREHENSIVE QUESTION BANK

---

## 🟢 BEGINNER QUESTIONS (50 Questions)

### Theory Questions

**Q1.** What does HTML stand for?
> **A:** HyperText Markup Language

**Q2.** Who created HTML and when?
> **A:** Tim Berners-Lee in 1991

**Q3.** Is HTML a programming language? Why or why not?
> **A:** No, HTML is a markup language. It doesn't have logic, loops, conditions, or variables. It only describes the structure and content of web pages.

**Q4.** What is the difference between a tag and an element?
> **A:** A tag is the markup code in angle brackets (`<p>`). An element is the complete structure: opening tag + content + closing tag (`<p>Content</p>`).

**Q5.** What are void/self-closing elements? Name 5 examples.
> **A:** Elements that don't have closing tags and can't contain content. Examples: `<br>`, `<hr>`, `<img>`, `<input>`, `<meta>`, `<link>`.

**Q6.** What is an HTML attribute? Where is it placed?
> **A:** An attribute provides additional information about an element. It's always placed in the opening/start tag as name="value" pairs.

**Q7.** What is the purpose of `<!DOCTYPE html>`?
> **A:** It tells the browser that the document is an HTML5 document and prevents "quirks mode" rendering.

**Q8.** What goes inside the `<head>` tag?
> **A:** Metadata — title, meta tags, links to CSS, scripts, favicon, character encoding, viewport settings. None of this is visible on the page.

**Q9.** What is the difference between `<head>` and `<header>`?
> **A:** `<head>` contains metadata (not visible). `<header>` is a semantic element for introductory content that IS visible on the page (logo, navigation).

**Q10.** Why should you use only one `<h1>` per page?
> **A:** For SEO — search engines use `<h1>` to understand the main topic of the page. Multiple h1s confuse search engines about the page's primary focus.

**Q11.** What's the difference between `<b>` and `<strong>`?
> **A:** `<b>` is visual only (bold appearance). `<strong>` has semantic meaning (indicates importance) — screen readers will emphasize it differently.

**Q12.** What's the difference between `<i>` and `<em>`?
> **A:** `<i>` is visual only (italic). `<em>` has semantic meaning (emphasis) — screen readers will change their tone of voice.

**Q13.** What does the `alt` attribute do on images?
> **A:** Provides alternative text if the image can't load, describes the image for screen readers (accessibility), and helps with SEO.

**Q14.** What's the difference between `<ul>` and `<ol>`?
> **A:** `<ul>` creates an unordered list with bullets. `<ol>` creates an ordered list with numbers/letters. Use `<ol>` when sequence matters.

**Q15.** What is the `target="_blank"` attribute?
> **A:** It makes the link open in a new tab/window instead of the current one.

**Q16.** Why should you add `rel="noopener noreferrer"` with `target="_blank"`?
> **A:** For security — prevents the new page from accessing the original page's `window.opener` object, which could be used for phishing attacks.

**Q17.** What is the purpose of the `<br>` tag?
> **A:** To insert a line break within content (like addresses or poems). It should NOT be used for spacing — use CSS margin/padding instead.

**Q18.** What are HTML entities? Give 3 examples.
> **A:** Special codes to display reserved characters. Examples: `&lt;` (<), `&gt;` (>), `&amp;` (&), `&nbsp;` (non-breaking space).

**Q19.** What is the difference between `<div>` and `<span>`?
> **A:** `<div>` is a block-level generic container (takes full width, starts new line). `<span>` is an inline generic container (takes only needed space, stays in flow).

**Q20.** What is `<meta charset="UTF-8">`?
> **A:** It sets the character encoding to UTF-8, which supports ALL languages and symbols (including emojis). Should be the first tag inside `<head>`.

### Code-Based Questions

**Q21.** Write the minimal valid HTML5 document structure.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
</head>
<body>
    <h1>Hello World</h1>
</body>
</html>
```

**Q22.** Create a link that opens email with a subject line.
```html
<a href="mailto:hi@example.com?subject=Hello&body=I want to say hi">
    Email Us
</a>
```

**Q23.** Create an image that links to another page.
```html
<a href="https://example.com">
    <img src="banner.jpg" alt="Click to visit Example" width="300" height="200">
</a>
```

**Q24.** Create a description list with 3 items.
```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language — structure of web pages</dd>
    <dt>CSS</dt>
    <dd>Cascading Style Sheets — styling of web pages</dd>
    <dt>JavaScript</dt>
    <dd>Programming language for web interactivity</dd>
</dl>
```

**Q25.** What's wrong with this code?
```html
<p>Hello <strong>World</p></strong>
```
> **A:** Tags are closed in wrong order. The inner tag must close before the outer tag. Correct: `<p>Hello <strong>World</strong></p>`

**Q26.** What's wrong with this code?
```html
<img src="photo.jpg">
```
> **A:** Missing `alt` attribute. Should be: `<img src="photo.jpg" alt="Description of photo">`

**Q27.** What's wrong with this code?
```html
<a href="https://google.com" target="_blank">Google</a>
```
> **A:** Missing `rel="noopener noreferrer"` for security with `target="_blank"`.

**Q28.** Write code for a numbered list starting from 5.
```html
<ol start="5">
    <li>Fifth item</li>
    <li>Sixth item</li>
    <li>Seventh item</li>
</ol>
```

**Q29.** Create a table with a cell that spans 3 columns.
```html
<table border="1">
    <tr>
        <th colspan="3">Full Width Header</th>
    </tr>
    <tr>
        <td>Col 1</td>
        <td>Col 2</td>
        <td>Col 3</td>
    </tr>
</table>
```

**Q30.** Create a form with a required email field and submit button.
```html
<form action="/submit" method="POST">
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required placeholder="you@example.com">
    <button type="submit">Submit</button>
</form>
```

**Q31-Q50:** Quick Answer Questions

**Q31.** Which tag creates a line break? → `<br>`

**Q32.** Which tag creates a horizontal line? → `<hr>`

**Q33.** Which tag makes text bold with semantic meaning? → `<strong>`

**Q34.** Which tag is for navigation links? → `<nav>`

**Q35.** Which attribute specifies the URL of a link? → `href`

**Q36.** Which attribute specifies the image source? → `src`

**Q37.** Which tag creates a dropdown select menu? → `<select>` with `<option>`

**Q38.** Which tag groups form fields? → `<fieldset>` with `<legend>`

**Q39.** Which tag is for the main content? → `<main>` (only one per page)

**Q40.** What does `<pre>` do? → Preserves whitespace and line breaks exactly as written

**Q41.** How do you create a checkbox? → `<input type="checkbox">`

**Q42.** How do you make an input required? → Add `required` attribute

**Q43.** How do you add a tooltip to any element? → Add `title="tooltip text"` attribute

**Q44.** What is the `download` attribute on `<a>`? → Makes the link download the file instead of navigating

**Q45.** How do you embed a YouTube video? → Use `<iframe>` with YouTube embed URL

**Q46.** What's the difference between `GET` and `POST` form methods? → GET sends data in URL (visible), POST sends in request body (hidden, more secure)

**Q47.** How do you comment in HTML? → `<!-- comment -->`

**Q48.** Which tag defines the page title in the browser tab? → `<title>`

**Q49.** What is `loading="lazy"` on images? → Defers loading until image is near the viewport (better performance)

**Q50.** What does semantic HTML mean? → Using tags that clearly describe their content's meaning and purpose (like `<article>`, `<nav>`) instead of generic tags (like `<div>`).

---
