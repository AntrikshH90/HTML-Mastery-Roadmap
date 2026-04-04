# 🅵 PART F: PARAGRAPHS, LINE BREAKS & HORIZONTAL RULES

## 📖 Theory (from PDF)

> 1. **Paragraph tags** — Used to create paragraph. Syntax: `<p>this is paragraph</p>`
> 2. **`<br>`** — Used to insert blank line in the document
> 3. **Horizontal ruler `<hr>`** — Used to draw horizontal line across the web page

## Code Examples

```html
<!-- Paragraphs -->
<p>This is the first paragraph. HTML ignores extra     spaces and
line breaks in source code — they collapse into single spaces.</p>

<p>This is a second paragraph. Each paragraph gets automatic spacing.</p>

<!-- Line Break (empty tag, no closing) -->
<p>Line one<br>Line two<br>Line three</p>

<!-- Horizontal Rule (thematic break between sections) -->
<h2>Section One</h2>
<p>Content of section one...</p>

<hr>

<h2>Section Two</h2>
<p>Content of section two...</p>
```

### How HTML Handles Whitespace

```html
<!-- In your code: -->
<p>Hello     World     !!!
Multiple   spaces   and
line breaks</p>

<!-- Browser renders as: -->
<!-- "Hello World !!! Multiple spaces and line breaks" -->
<!-- All extra spaces/breaks collapse into single space! -->
```

### Solutions for Multiple Spaces

```html
<!-- Method 1: Non-breaking space entity -->
<p>Hello&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;World</p>

<!-- Method 2: Pre tag (preserves everything) -->
<pre>Hello     World     !!!</pre>

<!-- Method 3: CSS (best approach) -->
<p style="white-space: pre;">Hello     World</p>
```

---

