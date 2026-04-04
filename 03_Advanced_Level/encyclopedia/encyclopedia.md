# 📋 COMPLETE HTML TAG ENCYCLOPEDIA (All 110+ Tags)

Every HTML tag with theory and code — side by side:

---

## 📄 DOCUMENT STRUCTURE TAGS

### `<!DOCTYPE html>`
**Theory:** Declaration that tells the browser this document is an HTML5 document. Must be the very first line. Not actually an HTML tag — it's an instruction to the browser.
```html
<!DOCTYPE html>
<!-- Must be FIRST line. No closing tag needed. -->
```

### `<html>`
**Theory:** The root element that wraps ALL other HTML elements. Everything goes inside this tag. Add `lang` attribute for accessibility and SEO.
```html
<html lang="en">
    <head>...</head>
    <body>...</body>
</html>
```

### `<head>`
**Theory:** Contains metadata about the document — information NOT displayed on the page itself. Holds title, meta tags, links to CSS, scripts, and other configuration.
```html
<head>
    <meta charset="UTF-8">
    <title>Page Title</title>
    <link rel="stylesheet" href="style.css">
</head>
```

### `<title>`
**Theory:** Sets the title shown in the browser's tab/title bar and in search engine results. Critical for SEO — should be unique per page and descriptive.
```html
<title>Complete HTML Guide 2025 | MyWebsite</title>
```

### `<body>`
**Theory:** Contains ALL visible content of the page — headings, paragraphs, images, links, tables, lists, everything the user sees and interacts with.
```html
<body>
    <h1>Welcome</h1>
    <p>Visible content here</p>
</body>
```

### `<meta>`
**Theory:** Provides metadata (data about data) — character set, viewport settings, description, keywords, author. Self-closing tag. Goes inside `<head>`.
```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Page description for SEO">
```

### `<link>`
**Theory:** Defines relationship between current document and external resources. Most commonly used to link CSS stylesheets, favicons, and preload resources.
```html
<link rel="stylesheet" href="styles.css">
<link rel="icon" href="/favicon.ico">
<link rel="preconnect" href="https://fonts.googleapis.com">
```

### `<style>`
**Theory:** Contains internal CSS rules applied to the document. Placed inside `<head>`. Useful for page-specific styles or critical CSS.
```html
<style>
    body { font-family: Arial, sans-serif; }
    .highlight { background: yellow; }
</style>
```

### `<script>`
**Theory:** Embeds or references JavaScript code. Can be inline or reference external files. Use `defer` or `async` for performance. Place at end of `<body>` or use `defer`.
```html
<script>alert('Hello!');</script>
<script src="app.js" defer></script>
<script src="analytics.js" async></script>
<script type="module" src="module.js"></script>
```

### `<noscript>`
**Theory:** Provides fallback content for users who have JavaScript disabled. Content inside is only shown when JS is unavailable.
```html
<noscript>
    <p>This website requires JavaScript. Please enable it.</p>
</noscript>
```

### `<base>`
**Theory:** Specifies the base URL and/or target for all relative URLs in the document. Only ONE `<base>` allowed per document. Rarely used.
```html
<base href="https://www.example.com/" target="_blank">
<!-- Now all relative links use this base URL -->
```

---

## 📝 TEXT CONTENT TAGS

### `<h1>` to `<h6>`
**Theory:** Define headings from most important (h1) to least (h6). Use only one h1 per page. Follow hierarchy — don't skip levels.
```html
<h1>Main Page Title</h1>
<h2>Section Heading</h2>
<h3>Sub-section</h3>
```

### `<p>`
**Theory:** Defines a paragraph. Block-level element. Browser adds spacing above and below automatically. HTML collapses multiple spaces/breaks into one.
```html
<p>This is a paragraph of text.</p>
```

### `<br>`
**Theory:** Inserts a single line break. Self-closing/void element. Use for line breaks within content (like addresses or poems), NOT for spacing (use CSS margin/padding).
```html
<p>Line one<br>Line two<br>Line three</p>
```

### `<hr>`
**Theory:** Creates a horizontal rule (thematic break). Self-closing. Represents a shift in topic or section. Originally visual, now semantic.
```html
<p>Topic one content</p>
<hr>
<p>Topic two content</p>
```

### `<pre>`
**Theory:** Displays preformatted text. Preserves ALL whitespace, spaces, tabs, and line breaks exactly as written in the source code. Uses monospace font.
```html
<pre>
    This    text
    preserves   ALL
    spacing   and   breaks.
</pre>
```

### `<blockquote>`
**Theory:** Indicates a block of text quoted from another source. Browser typically indents it. Use `cite` attribute for the source URL.
```html
<blockquote cite="https://example.com/source">
    <p>This is a long quotation from another source.</p>
</blockquote>
```

### `<div>`
**Theory:** Generic block-level container with NO semantic meaning. Used for grouping elements for styling/layout purposes. Use semantic tags when possible.
```html
<div class="card">
    <h3>Card Title</h3>
    <p>Card content</p>
</div>
```

### `<span>`
**Theory:** Generic inline container with NO semantic meaning. Used to apply styles or JS to a specific portion of text within a block element.
```html
<p>My favorite color is <span style="color: blue;">blue</span>.</p>
```

### `<main>`
**Theory:** Represents the dominant/main content of the `<body>`. Only ONE per page. Should be unique content — not repeated across pages (like nav, footer).
```html
<main>
    <article>
        <h1>Article Title</h1>
        <p>Main content goes here...</p>
    </article>
</main>
```

### `<section>`
**Theory:** Represents a thematic grouping of content, typically with a heading. Used to divide a document into sections like chapters or tabs.
```html
<section>
    <h2>About Us</h2>
    <p>We are a web development company...</p>
</section>
```

### `<article>`
**Theory:** Represents self-contained, independently distributable content — blog posts, news articles, forum posts, product cards. Should make sense on its own.
```html
<article>
    <h2>Blog Post Title</h2>
    <p>Published on <time datetime="2025-01-15">Jan 15</time></p>
    <p>Article content...</p>
</article>
```

### `<aside>`
**Theory:** Content tangentially related to the main content — sidebars, pull quotes, ads, related links. Not essential to the main flow.
```html
<aside>
    <h3>Related Articles</h3>
    <ul>
        <li><a href="#">CSS Grid Guide</a></li>
    </ul>
</aside>
```

### `<header>`
**Theory:** Introductory content for a section or the whole page. Contains headings, logos, navigation, search. Can be used multiple times (page header, article header).
```html
<header>
    <h1>My Website</h1>
    <nav>...</nav>
</header>
```

### `<footer>`
**Theory:** Footer for a section or the whole page. Contains copyright, contact info, links, social media. Can be used multiple times.
```html
<footer>
    <p>&copy; 2025 MyWebsite. All rights reserved.</p>
</footer>
```

### `<nav>`
**Theory:** Section containing navigation links. Use for main navigation, breadcrumbs, table of contents. Add `aria-label` to distinguish multiple navs.
```html
<nav aria-label="Main Navigation">
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
    </ul>
</nav>
```

### `<figure>` & `<figcaption>`
**Theory:** `<figure>` wraps self-contained content like images, diagrams, code. `<figcaption>` provides a caption. Moving the figure shouldn't affect document flow.
```html
<figure>
    <img src="chart.png" alt="Sales chart">
    <figcaption>Fig 1: Q4 Sales Report</figcaption>
</figure>
```

### `<details>` & `<summary>`
**Theory:** Creates expandable/collapsible content widget. `<summary>` is the visible clickable heading. No JavaScript needed. `open` attribute shows expanded by default.
```html
<details>
    <summary>Click for more info</summary>
    <p>Hidden content revealed on click!</p>
</details>
```

### `<dialog>`
**Theory:** Native modal/popup dialog. Use `showModal()` to open, `close()` to close. Supports `::backdrop` CSS pseudo-element. Form `method="dialog"` auto-closes.
```html
<dialog id="dlg">
    <h2>Dialog Title</h2>
    <form method="dialog">
        <button>Close</button>
    </form>
</dialog>
<button onclick="dlg.showModal()">Open</button>
```

### `<search>` (NEW 2023!)
**Theory:** Semantic element that wraps search functionality. Replaces `<div role="search">`. Clearly indicates search section of page.
```html
<search>
    <form action="/search">
        <input type="search" name="q">
        <button>Search</button>
    </form>
</search>
```

### `<address>`
**Theory:** Provides contact information for author/owner. Displays in italic by default. Not for random addresses — specifically for contact info.
```html
<address>
    Contact: <a href="mailto:info@example.com">info@example.com</a><br>
    123 Main Street, City
</address>
```

### `<hgroup>`
**Theory:** Groups a heading with related content like subheadings or taglines. Tells browser these elements form one logical heading.
```html
<hgroup>
    <h1>HTML Complete Guide</h1>
    <p>From Zero to Hero in 2025</p>
</hgroup>
```

### `<menu>`
**Theory:** Represents a list of commands or toolbar. Semantic alternative to `<ul>` for interactive lists/toolbars.
```html
<menu>
    <li><button>Cut</button></li>
    <li><button>Copy</button></li>
    <li><button>Paste</button></li>
</menu>
```

---

## ✏️ INLINE TEXT SEMANTICS

### `<a>` — Anchor/Hyperlink
**Theory:** Creates hyperlinks to other pages, files, locations, or email/phone. Most important navigation element. `href` is primary attribute.
```html
<a href="https://example.com" target="_blank" rel="noopener">Visit</a>
<a href="mailto:hi@example.com">Email Us</a>
<a href="tel:+1234567890">Call</a>
<a href="file.pdf" download>Download</a>
```

### `<strong>` vs `<b>`
**Theory:** `<strong>` = strong importance (semantic, screen readers emphasize). `<b>` = bold text (visual only, no semantic meaning). Prefer `<strong>`.
```html
<strong>This is important!</strong>  <!-- Semantic: important -->
<b>This is just bold.</b>            <!-- Visual only -->
```

### `<em>` vs `<i>`
**Theory:** `<em>` = emphasis (semantic, screen readers change tone). `<i>` = italic text (visual only, or for foreign terms/technical terms). Prefer `<em>`.
```html
<em>This is emphasized!</em>   <!-- Semantic: stressed -->
<i>This is italic text.</i>    <!-- Visual or alternative voice -->
```

### `<mark>`
**Theory:** Highlights text — represents text marked/highlighted for reference. Default yellow background. Great for search results highlighting.
```html
<p>Search results for: <mark>HTML</mark> found on this page.</p>
```

### `<small>`
**Theory:** Side comments, fine print, legal text, disclaimers. Renders smaller text. Semantic meaning: secondary importance.
```html
<p><small>&copy; 2025 All rights reserved. Terms apply.</small></p>
```

### `<del>` & `<ins>`
**Theory:** `<del>` = text deleted from document (strikethrough). `<ins>` = text inserted (underlined). Together show edits/changes.
```html
<p>Price: <del>$50</del> <ins>$30</ins></p>
```

### `<sub>` & `<sup>`
**Theory:** `<sub>` = subscript (below baseline — chemical formulas). `<sup>` = superscript (above baseline — exponents, footnotes).
```html
<p>H<sub>2</sub>O (water)</p>
<p>E = mc<sup>2</sup></p>
<p>Footnote<sup><a href="#fn1">1</a></sup></p>
```

### `<code>`
**Theory:** Represents inline computer code. Displays in monospace font. For multi-line code blocks, wrap with `<pre>`.
```html
<p>Use <code>document.getElementById()</code> to select elements.</p>
```

### `<kbd>`
**Theory:** Represents keyboard input — keys the user should press. Typically shown in monospace.
```html
<p>Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.</p>
```

### `<samp>`
**Theory:** Represents sample output from a computer program. Monospace font.
```html
<p>The console shows: <samp>Error: File not found</samp></p>
```

### `<var>`
**Theory:** Represents a variable in math or programming. Displays in italic.
```html
<p>Area = <var>π</var> × <var>r</var><sup>2</sup></p>
```

### `<abbr>`
**Theory:** Defines an abbreviation or acronym. `title` attribute provides the full form — shown as tooltip on hover. Helps accessibility.
```html
<p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
```

### `<cite>`
**Theory:** Represents the title of a creative work — book, article, song, film. Renders in italic. NOT for citing a person's name.
```html
<p>My favorite book is <cite>The Great Gatsby</cite>.</p>
```

### `<q>`
**Theory:** Short inline quotation. Browser automatically adds quotation marks. For longer quotes, use `<blockquote>`.
```html
<p>Einstein said <q>Imagination is more important than knowledge</q>.</p>
```

### `<dfn>`
**Theory:** Marks the term being defined in a definition context. The paragraph/section containing it should provide the definition.
```html
<p><dfn>HTML</dfn> is the standard markup language for web pages.</p>
```

### `<time>`
**Theory:** Represents a date, time, or duration. `datetime` attribute provides machine-readable format. Helps search engines and calendars.
```html
<p>Published on <time datetime="2025-01-15">January 15, 2025</time></p>
<p>The event starts at <time datetime="14:00">2:00 PM</time></p>
```

### `<data>`
**Theory:** Links content with a machine-readable value. The `value` attribute provides the machine version of the human-readable content.
```html
<p>Product: <data value="SKU-12345">Premium Widget</data></p>
```

### `<ruby>`, `<rt>`, `<rp>`
**Theory:** Ruby annotations — pronunciation guides for East Asian characters. `<ruby>` wraps, `<rt>` provides annotation, `<rp>` provides fallback parentheses.
```html
<ruby>漢<rp>(</rp><rt>かん</rt><rp>)</rp>字<rp>(</rp><rt>じ</rt><rp>)</rp></ruby>
```

### `<bdi>` & `<bdo>`
**Theory:** `<bdi>` isolates text that might have different direction (Arabic in English text). `<bdo>` overrides text direction. Important for internationalization.
```html
<p>User: <bdi>إيان</bdi> posted 3 comments.</p>
<bdo dir="rtl">This text is reversed</bdo>
```

### `<wbr>`
**Theory:** Word Break Opportunity. Suggests where a line break CAN occur in a long word/URL. Browser breaks only if needed.
```html
<p>https://www.example.com/<wbr>very-long-path/<wbr>to-some-page</p>
```

### `<u>`
**Theory:** Underlined text. In modern HTML, represents text with non-textual annotation — like misspelled words or proper names in Chinese. NOT for emphasis.
```html
<p>This word is <u>misspeled</u>.</p>
```

### `<s>`
**Theory:** Strikethrough text — represents content that is no longer relevant or accurate. Different from `<del>` (which represents actual edits).
```html
<p><s>Free shipping on orders over $50</s> (Offer expired)</p>
```

---

## 📋 LIST TAGS

### `<ul>`, `<ol>`, `<li>`
```html
<ul><li>Unordered item</li></ul>
<ol type="A" start="3"><li>Ordered item</li></ol>
<ol reversed><li>Countdown item</li></ol>
```

### `<dl>`, `<dt>`, `<dd>`
```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>
</dl>
```

---

## 📊 TABLE TAGS

### `<table>`, `<caption>`, `<colgroup>`, `<col>`
### `<thead>`, `<tbody>`, `<tfoot>`
### `<tr>`, `<th>`, `<td>`

*(All covered in detail in Part K above)*

---

## 📝 FORM TAGS

### `<form>`, `<input>`, `<textarea>`, `<select>`, `<option>`, `<optgroup>`
### `<button>`, `<label>`, `<fieldset>`, `<legend>`, `<datalist>`
### `<output>`, `<progress>`, `<meter>`

*(All covered in detail in Part L above)*

---

## 🖼️ MEDIA & EMBEDDED TAGS

### `<img>`, `<picture>`, `<source>`, `<video>`, `<audio>`, `<track>`
### `<iframe>`, `<embed>`, `<object>`, `<param>`
### `<map>`, `<area>`
### `<canvas>`, `<svg>`, `<math>`

*(All covered in their respective Parts above)*

---

## 🔧 SCRIPTING & MISC TAGS

### `<template>`
**Theory:** Holds HTML that is NOT rendered on page load. Content is cloned via JavaScript to create dynamic elements. Like a blueprint.
```html
<template id="card-template">
    <div class="card">
        <h3 class="title"></h3>
        <p class="body"></p>
    </div>
</template>

<script>
const template = document.getElementById('card-template');
const clone = template.content.cloneNode(true);
clone.querySelector('.title').textContent = 'Dynamic Card';
document.body.appendChild(clone);
</script>
```

### `<slot>`
**Theory:** Placeholder inside a web component (Shadow DOM) where external content can be inserted. Enables component composition.
```html
<template>
    <div class="header">
        <slot name="title"><h2>Default Title</h2></slot>
    </div>
    <slot>Default content</slot>
</template>
```

---

## ⚠️ DEPRECATED TAGS (Don't Use!)

| Tag | Replacement |
|-----|-------------|
| `<font>` | CSS `font-family`, `color`, `font-size` |
| `<center>` | CSS `text-align: center` |
| `<marquee>` | CSS animations |
| `<blink>` | CSS animations |
| `<frame>`, `<frameset>` | `<iframe>` or CSS layout |
| `<big>` | CSS `font-size` |
| `<strike>` | `<del>` or `<s>` |
| `<tt>` | `<code>` |
| `<acronym>` | `<abbr>` |
| `<applet>` | Nothing (dead technology) |

---

