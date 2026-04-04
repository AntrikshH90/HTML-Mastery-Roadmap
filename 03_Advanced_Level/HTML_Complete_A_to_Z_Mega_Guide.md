# 📘 HTML: Complete A-to-Z Mega Guide (Zero to Advanced)
### *Incorporating PDF Reference Notes by Atul Kumar / Coding Bugs / Notes Gallery*

---

# 📑 TABLE OF CONTENTS

| Part | Topic | Level |
|------|-------|-------|
| **A** | [What is HTML — Foundations](#part-a) | 🟢 Beginner |
| **B** | [Setting Up & First File](#part-b) | 🟢 Beginner |
| **C** | [HTML Document Structure](#part-c) | 🟢 Beginner |
| **D** | [HTML Elements, Tags & Attributes](#part-d) | 🟢 Beginner |
| **E** | [Heading Tags](#part-e) | 🟢 Beginner |
| **F** | [Paragraphs, Line Breaks & Horizontal Rules](#part-f) | 🟢 Beginner |
| **G** | [Text Formatting — Physical & Logical Tags](#part-g) | 🟢 Beginner |
| **H** | [Links & Anchor Tag](#part-h) | 🟢 Beginner |
| **I** | [Images](#part-i) | 🟢 Beginner |
| **J** | [Lists](#part-j) | 🟢 Beginner |
| **K** | [Tables](#part-k) | 🟡 Intermediate |
| **L** | [Forms & All Input Types](#part-l) | 🟡 Intermediate |
| **M** | [Semantic vs Non-Semantic Elements](#part-m) | 🟡 Intermediate |
| **N** | [HTML Layout & Page Structure](#part-n) | 🟡 Intermediate |
| **O** | [Multimedia — Audio & Video](#part-o) | 🟡 Intermediate |
| **P** | [Iframes & Embeds](#part-p) | 🟡 Intermediate |
| **Q** | [HTML Entities & Special Characters](#part-q) | 🟡 Intermediate |
| **R** | [Meta Tags & SEO](#part-r) | 🔴 Advanced |
| **S** | [Block vs Inline Elements](#part-s) | 🟡 Intermediate |
| **T** | [Adding CSS & JavaScript to HTML](#part-t) | 🟡 Intermediate |
| **U** | [HTML Comments](#part-u) | 🟢 Beginner |
| **V** | [Preformatted Text & Code Tags](#part-v) | 🟢 Beginner |
| **W** | [Image Maps](#part-w) | 🔴 Advanced |
| **X** | [HTML5 APIs & Modern Features](#part-x) | 🔴 Advanced |
| **Y** | [Accessibility (a11y)](#part-y) | 🔴 Advanced |
| **Z** | [Graphics — Canvas & SVG](#part-z) | 🔴 Advanced |
| **+** | [Complete Tag Encyclopedia (All 110+ Tags)](#all-tags) | Reference |
| **+** | [Data Attributes](#data-attr) | 🔴 Advanced |
| **+** | [Web Components & Templates](#web-comp) | 🔴 Advanced |
| **+** | [Performance & Best Practices](#performance) | 🔴 Advanced |
| **+** | [Tips & Tricks](#tips) | All Levels |
| **+** | [Mini Projects](#projects) | All Levels |
| **+** | [2024–2025 Trends](#trends) | 🔴 Advanced |

---

<a name="part-a"></a>
# 🅰️ PART A: WHAT IS HTML — FOUNDATIONS

## 📖 Theory (from PDF)

> **HTML stands for HyperText Markup Language.** It was created by **Tim Berners-Lee in 1991** as a standard for creating web pages.

Key points from the PDF:
- HTML is like the **skeleton** of a website
- HTML gives **structure** to a web page
- It contains text known as **tags**
- Tags are **understandable by the browser**
- HTML is the standard markup language for creating web pages
- HTML describes the **structure** of a web page
- HTML consists of a **series of elements**
- HTML elements tell the browser **how to display the content**
- HTML elements are represented by **tags**
- HTML tags label pieces of content such as "heading", "paragraph", "table"

## What is an HTML Document?

> An HTML document is a text document saved with the **'.html' or '.htm' extension**, containing text and specific tags enclosed in `< >`.

## HTML is NOT a Programming Language

```
❌ Programming Language → Has logic, loops, conditions (JavaScript, Python)
✅ Markup Language      → Describes structure and content (HTML)
```

## How the Web Works

```
[User types URL] 
    → [Browser sends HTTP request to server]
        → [Server responds with HTML file]
            → [Browser PARSES the HTML]
                → [Browser RENDERS the page visually]
```

## History Timeline

| Year | Version | Key Feature |
|------|---------|-------------|
| 1991 | HTML 1.0 | Tim Berners-Lee, 18 basic elements |
| 1995 | HTML 2.0 | Form elements added |
| 1997 | HTML 3.2 | Tables, applets |
| 1999 | HTML 4.01 | CSS support, accessibility |
| 2014 | HTML5 | Multimedia, canvas, semantic tags |
| 2017+ | Living Standard | Continuous updates by WHATWG |

---

<a name="part-b"></a>
# 🅱️ PART B: SETTING UP YOUR ENVIRONMENT

## Tools You Need

| Tool | Recommendation |
|------|---------------|
| **Text Editor** | VS Code (free), Sublime Text, Notepad++ |
| **Browser** | Chrome, Firefox (with DevTools) |
| **VS Code Extensions** | Live Server, Emmet, Prettier, Auto Rename Tag |

## Creating Your First HTML File

**Step 1:** Open VS Code  
**Step 2:** Create a file named `index.html`  
**Step 3:** Type `!` and press `Tab` (Emmet shortcut) — full boilerplate appears!  
**Step 4:** Save the file  
**Step 5:** Right-click → "Open with Live Server" (or just open in browser)

## Emmet Shortcuts (Massive Productivity Boost)

```
!                    → Full HTML5 boilerplate
html:5               → Same boilerplate
div.container        → <div class="container"></div>
div#main             → <div id="main"></div>
ul>li*5              → <ul> with 5 <li> items
h1+p+a               → <h1> then <p> then <a>
div#main.wrapper     → <div id="main" class="wrapper"></div>
p{Hello World}       → <p>Hello World</p>
table>tr*3>td*4      → Table with 3 rows, 4 columns
nav>ul>li*5>a{Item $} → Nav with 5 numbered links
lorem                → Lorem ipsum paragraph
lorem10              → 10 words of lorem ipsum
```

> 💡 **Tip:** Install the **Live Server** extension in VS Code for auto-reload on every save.

---

<a name="part-c"></a>
# 🅲 PART C: HTML DOCUMENT STRUCTURE

## Visual Layout (from PDF Page 2)

```
┌─────────────────────────────────────┐
│            <header />               │  ← Top bar (logo, nav)
├─────────────────────────┬───────────┤
│                         │           │
│  <body />               │           │
│  ┌───────────────────┐  │           │
│  │   <section />     │  │           │
│  │                   │  │ <aside /> │  ← Sidebar
│  └───────────────────┘  │           │
│  ┌───────────────────┐  │           │
│  │   <section />     │  │           │
│  │                   │  │           │
│  └───────────────────┘  │           │
│  ┌───────────────────┐  │           │
│  │   <section />     │  │           │
│  │                   │  │           │
│  └───────────────────┘  │           │
├─────────────────────────┴───────────┤
│            <footer />               │  ← Bottom bar
└─────────────────────────────────────┘
```

## Basic HTML Skeleton (from PDF Page 3)

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Hello World!</title>
    </head>
    <body>
        <p>I am loving HTML</p>
    </body>
</html>
```

## Each Part Explained (PDF + Extended)

| Tag | Description (from PDF) | Extra Details |
|-----|----------------------|---------------|
| `<!DOCTYPE html>` | It is used to tell the browser the type of document | Must be the very first line. Tells browser this is HTML5 |
| `<html>` | This tag is container for all other HTML tags | Root element. Add `lang="en"` for accessibility |
| `<head>` | Tag to define the head portion of the document | Contains metadata — NOT visible on page |
| `<title>` | It is used to set title of the document shown on the browser's tab | Important for SEO. Shows in browser tab & search results |
| `<body>` | Contains all content of HTML document that is shown to the user | Everything visible goes here |
| `<p>` | `<p>` is used to define the paragraph | Block element, adds spacing automatically |

## Modern Complete Skeleton

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Character encoding — supports all languages -->
    <meta charset="UTF-8">
    
    <!-- Responsive design on mobile devices -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Page description for search engines -->
    <meta name="description" content="A brief description of the page">
    
    <!-- Title shown in browser tab -->
    <title>My First Web Page</title>
    
    <!-- External CSS stylesheet -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Hello, World!</h1>
    <p>This is my first web page.</p>
    
    <!-- JavaScript at bottom for performance -->
    <script src="script.js"></script>
</body>
</html>
```

> ⚠️ **Note from PDF:** In HTML every tag must have an end tag. For example, if you are inserting a paragraph with `<p>` it should have an end tag `</p>`. There are some exception tags that don't have an end tag like `<!DOCTYPE html>`, `<br>`.

---

<a name="part-d"></a>
# 🅳 PART D: HTML ELEMENTS, TAGS & ATTRIBUTES

## What is a Tag? (from PDF)

> - HTML instructions are known as **tags**
> - An HTML tag acts as a **container for content or other HTML tags**
> - Tags are words enclosed within `<` and `>` angle brackets

## Types of Tags (from PDF)

### 1. Open Tags / Container Tags
- Has a range (opening + closing)
- Example: `<p></p>`, `<h1></h1>`, `<div></div>`

### 2. Close Tags / Empty Tags (Self-Closing / Void)
- Does NOT have a range — no closing tag needed
- Examples: `<br>`, `<hr>`, `<img>`, `<input>`, `<meta>`, `<link>`

```html
<!-- Container tags (have opening + closing) -->
<p>This has content inside</p>
<h1>This is a heading</h1>
<div>This is a container</div>

<!-- Empty/Void tags (self-closing, no content) -->
<br>          <!-- Line break -->
<hr>          <!-- Horizontal rule -->
<img src="photo.jpg" alt="A photo">
<input type="text">
<meta charset="UTF-8">
```

## What is an HTML Element? (from PDF)

> An HTML element is a **complete set** that consists of a **start tag** (opening tag), **content**, and an **end tag** (closing tag).

```
HTML Element = Start Tag + Content + End Tag
```

```html
<!-- Anatomy of an element -->
  <h1>Content</h1>
   ↑       ↑       ↑
Opening  Content  Closing
  Tag              Tag
```

```html
<!-- Detailed anatomy -->
  <p class="intro">Hello World!</p>
   ↑    ↑              ↑         ↑
  Tag  Attribute     Content   Closing Tag
```

## What is an Attribute? (from PDF)

> - Attributes define the **properties or characteristics** of an HTML element
> - Attributes modify the **behavior, functionality, or appearance** of an element
> - They allow you to **customize** the behavior of HTML elements
> - Attributes are always specified in **the start tag**
> - Attributes usually come in **name/value pairs** like: `name="value"`

```html
<!-- Example from PDF -->
<a href="https://www.example.com">Go to Example</a>
     ↑          ↑
  Attribute   Value
    Name
```

## Global Attributes (Available on ALL Tags)

| Attribute | Description | Example |
|-----------|-------------|---------|
| `id` | Unique identifier (one per page) | `<div id="header">` |
| `class` | CSS class name(s) | `<p class="intro highlight">` |
| `style` | Inline CSS styles | `<p style="color: red;">` |
| `title` | Tooltip text on hover | `<abbr title="HTML">HTML</abbr>` |
| `hidden` | Hides element | `<p hidden>Secret</p>` |
| `lang` | Language of content | `<html lang="en">` |
| `dir` | Text direction | `<p dir="rtl">Arabic</p>` |
| `tabindex` | Tab order for keyboard | `<input tabindex="1">` |
| `contenteditable` | Makes editable | `<div contenteditable="true">` |
| `draggable` | Enables drag | `<img draggable="true">` |
| `data-*` | Custom data attributes | `<div data-user-id="42">` |
| `spellcheck` | Spell checking | `<textarea spellcheck="true">` |
| `accesskey` | Keyboard shortcut | `<button accesskey="s">Save</button>` |

---

<a name="part-e"></a>
# 🅴 PART E: HEADING TAGS

## 📖 Theory (from PDF)

> - Heading tags define headings
> - Displayed in **larger and bolder** font
> - There are **6 levels** of heading tags: `<h1>` to `<h6>`

## Code & Visual

```html
<h1>Heading 1</h1>   <!-- Largest — Main page heading -->
<h2>Heading 2</h2>   <!-- Sub heading -->
<h3>Heading 3</h3>   <!-- Sub-sub heading -->
<h4>Heading 4</h4>   <!-- Level 4 -->
<h5>Heading 5</h5>   <!-- Level 5 -->
<h6>Heading 6</h6>   <!-- Smallest heading -->
```

### Visual Size Comparison:
```
<h1> ████████████████████████████  (Largest, ~32px)
<h2> ██████████████████████        (~24px)
<h3> ████████████████              (~18.7px)
<h4> ██████████████                (~16px)
<h5> ████████████                  (~13.3px)
<h6> ██████████                    (~10.7px, Smallest)
```

## ⚠️ Important Rules

```
✅ DO:
  • Use only ONE <h1> per page (most important for SEO)
  • Follow heading hierarchy: h1 → h2 → h3 (don't skip levels)
  • Use headings for structure, not for making text big

❌ DON'T:
  • Use multiple <h1> tags
  • Skip from <h1> to <h4> (missing h2, h3)
  • Use <h1> just because you want big text (use CSS instead)
```

> 💡 **SEO Tip:** Search engines like Google use headings to understand page structure. Your `<h1>` should contain your main keyword.

---

<a name="part-f"></a>
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

<a name="part-g"></a>
# 🅶 PART G: TEXT FORMATTING — PHYSICAL & LOGICAL TAGS

## 📖 Theory (from PDF)

### Physical Tags
> Physical tags describe the **physical appearance** of the content. They indicate exactly how specific characters are to be formatted.

### Logical Tags
> Logical tags indicate the **purpose of text**, such as whether it's a heading, code, or an address.

## Complete Text Formatting Reference (from PDF + Extended)

### Physical Tags (Appearance Only)

| Tag | Description (from PDF) | Code Example | Result |
|-----|----------------------|--------------|--------|
| `<b>` | To make a text **bold** | `<b>Bold Text</b>` | **Bold Text** |
| `<i>` | To make a text *italic* | `<i>Italic Text</i>` | *Italic Text* |
| `<big>` | Defines big text | `<big>Big text</big>` | (Larger) |
| `<small>` | Defines small text | `<small>Small text</small>` | (Smaller) |
| `<sup>` | Defines superscripted text | `x<sup>2</sup>` | x² |
| `<sub>` | Defines subscripted text | `H<sub>2</sub>O` | H₂O |
| `<u>` | Underlined text | `<u>Underlined</u>` | (Underlined) |
| `<s>` | Strikethrough text (from PDF) | `<s>Striked out</s>` | ~~Striked~~ |

### Logical/Semantic Tags (Meaning + Appearance)

| Tag | Description (from PDF) | Code Example |
|-----|----------------------|--------------|
| `<strong>` | Used to show important text, makes text bold | `<strong>Important!</strong>` |
| `<em>` | Used to define emphasised text | `<em>Emphasised</em>` |
| `<mark>` | Used to highlight the text | `<mark>Highlighted</mark>` |
| `<code>` | Used to insert source code in document | `<code>console.log()</code>` |
| `<cite>` | To insert title of creative work | `<cite>Book Title</cite>` |
| `<time>` | Used to insert the date and time | `<time>14-4-2022 17:20</time>` |
| `<address>` | Used to insert the address | `<address>Earth</address>` |
| `<blockquote>` | Block quote from another source | `<blockquote>Quote</blockquote>` |
| `<pre>` | Defines preformatted text | `<pre>  spaces  kept  </pre>` |
| `<abbr>` | Defines abbreviation (from PDF) | `<abbr title="World Health Organization">WHO</abbr>` |
| `<del>` | Text deleted from document (from PDF) | `<del>deleted text</del>` |
| `<ins>` | Text inserted into document (from PDF) | `<ins>inserted text</ins>` |
| `<dfn>` | Marks term being defined (from PDF) | `<dfn>Java</dfn> is a language.` |
| `<kbd>` | Defines keyboard input (from PDF) | `<kbd>Ctrl+S</kbd>` |
| `<samp>` | Sample output from computer (from PDF) | `<samp>Error 404</samp>` |
| `<var>` | Variable in math/programming (from PDF) | `<var>x</var> = 5` |
| `<q>` | Short inline quotation | `<q>To be or not to be</q>` |

## Complete Text Formatting Example (from PDF Page 5)

```html
<!DOCTYPE html>
<html>
<head>
    <title>Text Formatting</title>
</head>
<body>
    <!-- Headings Section -->
    <section>
        <h1>Heading 1</h1>
        <h2>Heading 2</h2>
        <h3>Heading 3</h3>
        <h4>Heading 4</h4>
        <h5>Heading 5</h5>
        <h6>Heading 6</h6>
    </section>
    
    <!-- Text Formatting Section -->
    <section>
        <p><b>Bold Text</b></p>
        <p><i>Italic Text</i></p>
        <p>Hello, <strong>This text is important.</strong></p>
        <p><em>This text is emphasised text.</em></p>
        <p><mark>This is highlighted text</mark></p>
        <p><s>This is striked out text</s></p>
        <p><code>console.log("Hello World, This is a source code!");</code></p>
        <p><cite>This eBook is created by @richwebdeveloper</cite></p>
        <p>The time is: <time>14-4-2022 17:20</time></p>
        <p>My Address:
            <address>Earth</address>
        </p>
        <p><sub>This is subscript text</sub></p>
        <p><sup>This is superscript text</sup></p>
        <p><blockquote>This is a blockquote text</blockquote></p>
        <p><pre>This is a preformatted    text.</pre></p>
    </section>
</body>
</html>
```

### Additional Logical Tags from PDF (Page 31):

```html
<!-- Abbreviation tag -->
<abbr title="World Health Organization">WHO</abbr>

<!-- Address tag — displays in italic -->
<address>Shant Niwas, Pune</address>

<!-- Blockquote with citation -->
<blockquote>
    <p>Google is an American multinational corporation technology 
       company that offers a variety of products and services</p>
    <cite>http://www.google.com</cite>
</blockquote>

<!-- Delete + Insert together -->
<p><del>Old price: $50</del> <ins>New price: $30</ins></p>

<!-- Definition -->
<p><dfn>Java</dfn> is a programming language.</p>

<!-- Strong importance -->
<strong>Java is a high level programming language</strong>

<!-- Variable -->
<p>The area is <var>l</var> × <var>w</var></p>
```

> 💡 **Tip from PDF:** Use `<strong>` over `<b>` and `<em>` over `<i>` because screen readers interpret semantic tags differently — they convey **meaning**, not just appearance.

---

<a name="part-h"></a>
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

<a name="part-i"></a>
# 🅸 PART I: IMAGES

## 📖 Theory (from PDF)

> Images make websites beautiful and easy to process information. To add images to HTML pages **`<img>` tag is used**. The `<img>` tag is an **empty tag**, meaning it doesn't have a closing tag, and it uses attributes.

## Image Attributes (from PDF)

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `src` | Specifies the path of image file (can be relative or absolute URL) |
| `alt` | Shows an alternative name to the image if the image is not loaded and helpful for SEO |
| `height` | Used to specify the height of the image |
| `width` | Used to specify the width of the image |
| `title` | Displays a tooltip when user hovers over the image |
| `loading` | Specifies whether to load immediately (eager) or defer until visible (lazy) |

## Code Examples

```html
<!-- Basic image (from PDF) -->
<img src="/HTML_image.jpg" alt="HTML Image" width="100%" height="500">

<!-- Image with all attributes (from PDF) -->
<img src="home.jpg" 
     width="100" 
     height="100" 
     alt="loading" 
     title="some info" 
     loading="lazy">

<!-- Modern best practices -->
<img src="photo.jpg" 
     alt="A beautiful sunset over mountains" 
     width="600" 
     height="400"
     loading="lazy"
     decoding="async">

<!-- High priority hero image (above fold) -->
<img src="hero.jpg" 
     alt="Hero banner" 
     loading="eager" 
     fetchpriority="high">
```

## Image as Link (from PDF)

```html
<!-- When users click on the image, they will be redirected to the URL -->
<a href="https://www.google.com">
    <img src="icon.jpg" alt="Go to Google">
</a>
```

## Responsive Images

```html
<!-- srcset: Different sizes for different screens -->
<img src="photo-800.jpg"
     srcset="photo-400.jpg 400w,
             photo-800.jpg 800w,
             photo-1200.jpg 1200w"
     sizes="(max-width: 600px) 400px,
            (max-width: 1000px) 800px,
            1200px"
     alt="Responsive image">

<!-- Picture element: Different images for different conditions -->
<picture>
    <source media="(min-width: 1200px)" srcset="hero-large.webp" type="image/webp">
    <source media="(min-width: 800px)" srcset="hero-medium.webp" type="image/webp">
    <img src="hero-small.jpg" alt="Hero image" loading="lazy">
</picture>
```

## Figure & Caption

```html
<figure>
    <img src="chart.png" alt="Sales chart showing 50% growth in Q4">
    <figcaption>Figure 1: Q4 Sales Growth Report 2024</figcaption>
</figure>
```

## Alt Text Best Practices

```html
<!-- ✅ Good alt text -->
<img src="chart.png" alt="Bar chart showing sales increased 40% from Q3 to Q4">
<img src="team.jpg" alt="Our development team of 5 people at annual retreat">

<!-- ✅ Decorative images (empty alt) -->
<img src="divider.png" alt="">

<!-- ❌ Bad alt text -->
<img src="photo.jpg" alt="image">
<img src="photo.jpg" alt="photo.jpg">
<img src="photo.jpg">  <!-- Missing alt entirely! -->
```

> 💡 **Tip:** Always use **WebP** or **AVIF** format for images — they're 30-50% smaller than JPEG/PNG with same quality. Use `<picture>` for fallback.

---

<a name="part-j"></a>
# 🅹 PART J: LISTS

## 📖 Theory (from PDF)

> Using HTML it's possible to display information in a list. This makes it easier to understand the data. HTML provides **3 ways** to specify the information.

| List Type | Description (from PDF) |
|-----------|----------------------|
| `<ol>` | To insert **ordered list** in the web page |
| `<ul>` | To insert **unordered list** in the web page |
| `<dl>` | To insert **description list** in the web page, arranged in key-value pair |

> In the examples, `<li>` is used to insert a list item, `<dt>` means **data term** (key) and `<dd>` means **data description** (value).

## 1. Unordered List (from PDF)

> An unordered list displays items in **bullets** format. Type attribute specifies the type of bullet:
> - **disc** – solid circle
> - **square** – solid square
> - **circle** – hollow circle

```html
<ul type="disc">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>

<ul type="square">
    <li>Square bullet</li>
</ul>

<ul type="circle">
    <li>Hollow circle bullet</li>
</ul>
```

## 2. Ordered List (from PDF)

> An ordered list displays items in **numbered format**. Type attribute specifies type of sequence:
> - Type: `1`, `A`, `a`, `I`, `i`

```html
<!-- Default numbered (1, 2, 3...) -->
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>

<!-- Different types -->
<ol type="A"><li>Uppercase letters (A, B, C)</li></ol>
<ol type="a"><li>Lowercase letters (a, b, c)</li></ol>
<ol type="I"><li>Roman numerals (I, II, III)</li></ol>
<ol type="i"><li>Lowercase roman (i, ii, iii)</li></ol>

<!-- Start from specific number -->
<ol start="5">
    <li>This is item 5</li>
    <li>This is item 6</li>
</ol>

<!-- Reverse order -->
<ol reversed>
    <li>Third (shows as 3)</li>
    <li>Second (shows as 2)</li>
    <li>First (shows as 1)</li>
</ol>
```

## 3. Description List (from PDF)

> Definition list is not a list of items. It's a list of **term and explanation** of term.

```html
<dl>
    <dt>HTML</dt>
    <dd>A markup language for creating web pages</dd>
    
    <dt>CSS</dt>
    <dd>A style sheet language for designing web pages</dd>
</dl>
```

## 4. Nested List (from PDF)

> The list inside another list is known as a **nested list**.

```html
<ul>
    <li>Fruits
        <ul>
            <li>Apple</li>
            <li>Banana</li>
            <li>Orange</li>
        </ul>
    </li>
    <li>Vegetables
        <ul>
            <li>Carrot</li>
            <li>Broccoli</li>
            <li>Spinach</li>
        </ul>
    </li>
</ul>
```

## Complete List Example (from PDF Page 10)

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Lists</title>
</head>
<body>
    <section>
        <h3>Ordered List</h3>
        <ol>
            <li>One</li>
            <li>Two</li>
            <li>Three</li>
        </ol>
    </section>
    <section>
        <h3>Unordered List</h3>
        <ul>
            <li>One</li>
            <li>Two</li>
            <li>Three</li>
        </ul>
    </section>
    <section>
        <h3>Description List</h3>
        <dl>
            <dt>One</dt>
            <dd>One Description</dd>
            <dt>Two</dt>
            <dd>Two Description</dd>
            <dt>Three</dt>
            <dd>Three Description</dd>
        </dl>
    </section>
</body>
</html>
```

> 💡 **When to use which:** Use `<ul>` for unrelated items, `<ol>` when order matters (steps, rankings), `<dl>` for term-definition pairs (glossaries, FAQs).

---

<a name="part-k"></a>
# 🅺 PART K: TABLES

## 📖 Theory (from PDF)

> HTML table is used to display data in **tabular format** (rows and columns).

| Tag | Description (from PDF) |
|-----|----------------------|
| `<table>` | Define a table. It is container for entire table |
| `<thead>` | Used to group table header content. Groups table heading rows |
| `<tbody>` | Container for table content. Groups table data rows |
| `<tfoot>` | Footer section of table |
| `<th>` | To insert header cell within row (usually bold and centered) |
| `<tr>` | To insert a row within table |
| `<td>` | To insert a table cell within row |

## Attributes (from PDF)

### Table Attributes:
| Attribute | Description (from PDF) |
|-----------|----------------------|
| `border` | Add the border around the table and its cells |
| `cellpadding` | Add space between content and cell wall |
| `cellspacing` | Add the space between cells |
| `width` | Sets width of table |
| `align` | Align the table (center, left, right) |
| `bgColor` | Background color |

### Cell Attributes (`<td>` and `<th>`):
| Attribute | Description (from PDF) |
|-----------|----------------------|
| `colspan` | Makes a cell span across **multiple columns** (horizontally) |
| `rowspan` | Makes a cell span across **multiple rows** (vertically) |

## Basic Table Example (from PDF Page 7)

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Table</title>
</head>
<body>
    <section>
        <table border="1">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Age</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>John</td>
                    <td>25</td>
                </tr>
                <tr>
                    <td>Jane</td>
                    <td>24</td>
                </tr>
                <tr>
                    <td>Jack</td>
                    <td>23</td>
                </tr>
            </tbody>
        </table>
    </section>
</body>
</html>
```

## Table with All Attributes (from PDF Page 39)

```html
<table border="2" cellpadding="10" cellspacing="10" 
       width="300" align="center" bgColor="white">
    <thead>
        <tr>
            <th>Id</th>
            <th>Name</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>101</td>
            <td>Satyajit</td>
        </tr>
        <tr>
            <td>102</td>
            <td>Pranav</td>
        </tr>
        <tr>
            <td colspan="2" rowspan="2">Spanning cell</td>
            <td>Extra</td>
        </tr>
    </tbody>
</table>
```

## Complete Semantic Table (Modern Best Practice)

```html
<table>
    <caption>Employee Directory 2025</caption>
    
    <colgroup>
        <col style="background-color: #f0f0f0">
        <col span="2">
        <col style="background-color: #e0ffe0">
    </colgroup>
    
    <thead>
        <tr>
            <th scope="col">ID</th>
            <th scope="col">Name</th>
            <th scope="col">Department</th>
            <th scope="col">Salary</th>
        </tr>
    </thead>
    
    <tbody>
        <tr>
            <td>001</td>
            <td>Alice Johnson</td>
            <td>Engineering</td>
            <td>$95,000</td>
        </tr>
        <tr>
            <td>002</td>
            <td>Bob Smith</td>
            <td>Marketing</td>
            <td>$75,000</td>
        </tr>
    </tbody>
    
    <tfoot>
        <tr>
            <td colspan="3"><strong>Total</strong></td>
            <td><strong>$170,000</strong></td>
        </tr>
    </tfoot>
</table>
```

## Spanning Rows & Columns

```html
<table border="1">
    <tr>
        <th colspan="3">Student Schedule</th>  <!-- Spans 3 columns -->
    </tr>
    <tr>
        <th>Time</th>
        <th>Monday</th>
        <th>Tuesday</th>
    </tr>
    <tr>
        <td>9:00</td>
        <td rowspan="2">Math (Double Period)</td>  <!-- Spans 2 rows -->
        <td>English</td>
    </tr>
    <tr>
        <td>10:00</td>
        <!-- Math continues from above -->
        <td>Science</td>
    </tr>
</table>
```

> ⚠️ **Important:** Don't use tables for page layout! Tables are for **tabular data only**. Use CSS Grid/Flexbox for layouts.

---

<a name="part-l"></a>
# 🅻 PART L: FORMS & ALL INPUT TYPES

## 📖 Theory (from PDF)

> HTML form is used to **collect user input** in the webpage and can then be sent to the server for processing. To add the form we use the `<form>` element.

## Form Attributes (from PDF)

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `name` | Defines name of the form, it should be unique. Useful for accessing form in JavaScript |
| `action` | Specifies URL where the form data will be sent when submitted. Path to backend script which processes the data |
| `method` | Used to set HTTP method: **GET** (sends data as URL parameter, visible) or **POST** (sends in request body, more secure) |
| `enctype` | Defines how browser should encode data: **application/x-www-form-urlencoded** (default), **multipart/form-data** (for file uploads), **text/plain** (debugging) |

## Form Field Types (from PDF)

The PDF lists these field types:
- Text Fields
- Buttons
- Checkbox
- Radiobox
- Select options control
- File select
- Hidden inputs
- Labels

## All Input Types (from PDF + Extended)

### Text Inputs

```html
<!-- Text (from PDF): A single line text field (Default) -->
<input type="text" name="username">

<!-- Password (from PDF): Characters are masked/hidden -->
<input type="password" name="password">

<!-- Email (from PDF): Includes basic validation -->
<input type="email" name="email">

<!-- Tel (from PDF): For telephone numbers -->
<input type="tel" name="phone">

<!-- Search (from PDF): Designed for search inputs -->
<input type="search" name="search">

<!-- URL -->
<input type="url" name="website" placeholder="https://example.com">
```

### Number & Range Inputs

```html
<!-- Number (from PDF): Accepts integers with optional min, max, step -->
<input type="number" name="age" min="1" max="100">

<!-- Range (from PDF): A slider to select value between specified range -->
<input type="range" name="volume" min="0" max="100" step="10">
```

### Date/Time Inputs (HTML5 — from PDF)

```html
<!-- Date (from PDF): Select date from drop-down calendar -->
<input type="date" name="date">

<!-- DateTime (from PDF): Select date and time at same time -->
<input type="datetime-local" name="DateTime">

<!-- Time (from PDF): Select time -->
<input type="time" name="time">

<!-- Month -->
<input type="month" name="birth-month">

<!-- Week -->
<input type="week" name="project-week">
```

### Selection Inputs

```html
<!-- Radio (from PDF): Select one option from group -->
<!-- For grouping, use same name for all radio buttons -->
<input type="radio" name="gender" id="male" value="male">
<label for="male">Male</label>
<input type="radio" name="gender" id="female" value="female">
<label for="female">Female</label>

<!-- Checkbox (from PDF): Select one or more options from group -->
<!-- For grouping, use same name for all checkboxes -->
<input type="checkbox" name="subscribe" id="sub" value="yes">
<label for="sub">Subscribe to Newsletter</label>
```

### Checkbox Attributes (from PDF)

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `type` | Set to `checkbox` |
| `name` | Name of the checkbox |
| `id` | ID of the checkbox |
| `onChange` | JavaScript function when user checks/unchecks |
| `value` | Value of checkbox (e.g., food name) |
| `checked` | If added, checkbox is selected by default |

### Radio Button Attributes (from PDF)

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `type` | Set to `radio` |
| `name` | Name of the radio button (same name = same group) |
| `id` | ID of the radio button |
| `onChange` | JavaScript function when checked/unchecked |
| `value` | Value of the radio button |
| `checked` | If added, radio button is selected by default |

### Other Input Types

```html
<!-- Color (from PDF): Color picker -->
<input type="color" name="favcolor">

<!-- File (from PDF): File upload -->
<input type="file" name="myfile">
<input type="file" name="avatar" accept="image/*" multiple>

<!-- Hidden (from PDF): Stores data without displaying to user -->
<input type="hidden" name="userID" value="12345">

<!-- Submit (from PDF): Button to submit form data -->
<input type="submit" value="Login">

<!-- Reset (from PDF): Resets all fields to initial value -->
<input type="reset" value="Reset">

<!-- Image (from PDF): Graphical version of submit button -->
<input type="image" src="icon.jpg" alt="Submit">
```

## File Input Important Note (from PDF)

> While adding file input control, **never forget** to set `enctype="multipart/form-data"` attribute in the form element.

## Labels (from PDF)

> We can use `<label>` to set a label for the input field. When users click on the label, the form field **automatically gets selected**. For this feature, set the `for` attribute in the label and it should match with the input field `id`.

```html
<!-- Explicit label (recommended — from PDF) -->
<label for="name">Name:</label>
<input type="text" name="name" id="name">

<!-- Implicit label (wrapping) -->
<label>
    Email:
    <input type="email" name="email">
</label>
```

> ⚠️ **Always use labels!** They improve accessibility and increase click target area.

## Textarea (from PDF)

> Creates multi-line text input area. Useful for larger blocks of text like user address and description.

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `name` | Name of the field |
| `id` | ID of the field |
| `rows` | Number of rows for text area |
| `cols` | Number of columns for text area |

```html
<label for="address">Address:</label>
<textarea name="address" id="address" cols="30" rows="10"></textarea>
```

## Select Dropdown (from PDF)

> If you have a long list of options and you want to allow select only one option, use **select input** type instead of radio buttons.

```html
<label for="country">Country:</label>
<select name="country" id="country">
    <option value="" disabled selected>-- Select --</option>
    <option value="india">India</option>
    <option value="usa">USA</option>
</select>
```

## Optgroup (from PDF)

> Used to **group options** inside a select dropdown list for easier navigation.

```html
<select name="tech">
    <optgroup label="Front-End">
        <option value="-1">Select tech</option>
        <option value="html">HTML</option>
        <option value="css">CSS</option>
    </optgroup>
    <optgroup label="Back-end">
        <option value="java">Java</option>
        <option value="php">PHP</option>
    </optgroup>
</select>
```

## Button (from PDF)

> Creates clickable buttons. Used to submit form data and also to perform actions with JavaScript.

| Attribute | Description (from PDF) |
|-----------|----------------------|
| `type` | Type: `submit`, `reset`, `button` |
| `name` | Name of the button |
| `id` | ID of the button |
| `onClick` | JavaScript function when clicked |

```html
<button type="submit">Submit</button>
<button type="reset">Reset</button>
<button type="button" onclick="alert('Hi!')">Click Me</button>
```

## Fieldset & Legend (from PDF)

> Fieldset **groups related fields** in the form. Legend provides a **caption** to the group.

```html
<fieldset>
    <legend>Personal Information</legend>
    <label for="fname">First Name:</label>
    <input type="text" id="fname" name="fname">
</fieldset>
```

## Datalist (from PDF)

> Provides list of **predefined options** to input field.

```html
<input list="mylist" name="city">
<datalist id="mylist">
    <option value="Pune"></option>
    <option value="Mumbai"></option>
    <option value="Delhi"></option>
</datalist>
```

## Hidden Input Explained (from PDF)

> If you want to add/set a value in the form that can be used later or sent to the server **without showing it to the user**, hidden fields are used. For example, you need a user ID for front-end operations but don't want to show it.

```html
<input type="hidden" name="user-id" value="12345">
```

## Additional Input Attributes

| Attribute | Description |
|-----------|-------------|
| `required` | Must be filled before submit |
| `readonly` | Can't be edited (still submitted) |
| `disabled` | Can't be edited (NOT submitted) |
| `placeholder` | Hint text inside input (from PDF) |
| `value` | Initial value of field (from PDF) |
| `autofocus` | Auto-focus on page load |
| `autocomplete` | Browser auto-fill |
| `pattern` | Regex validation |
| `min` / `max` | Minimum/maximum value |
| `minlength` / `maxlength` | Character limits |
| `step` | Number increment value |
| `multiple` | Allow multiple values (email, file) |
| `accept` | File types accepted |
| `inputmode` | Virtual keyboard hint (`numeric`, `tel`, `email`, `url`) |
| `enterkeyhint` | Label for Enter key (`search`, `send`, `go`, `next`, `done`) |

## Complete Form Example (from PDF Page 18)

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Forms</title>
</head>
<body>
    <section>
        <form name="user_form" method="post" action="/my_action">
            <label for="name">Name:</label> 
            <input type="text" name="name" id="name" value=""><br>
            
            <label for="password">Password:</label> 
            <input type="password" name="password" id="password" value=""><br>
            
            <label for="address">Address:</label> 
            <textarea name="address" id="address" cols="30" rows="10"></textarea><br>
            
            <label for="checkbox">Checkbox:</label> 
            <input type="checkbox" name="checkbox" id="checkbox" value="checkbox_1"><br>
            
            <label for="checkbox_2">Checkbox 2:</label> 
            <input type="checkbox" name="checkbox" id="checkbox_2" value="checkbox_2"><br>
            
            <label for="radio">Radio:</label> 
            <input type="radio" name="radio" id="radio" value="radio"><br>
            
            <label for="radio_2">Radio:</label> 
            <input type="radio" name="radio" id="radio_2" value="radio_2"><br>
            
            <label for="select">Select:</label> 
            <select name="select" id="select">
                <option value="option_1">Option 1</option>
                <option value="option_2">Option 2</option>
                <option value="option_3">Option 3</option>
            </select><br>
            
            <label for="file">File:</label> 
            <input type="file" name="file" id="file" value=""><br>
            
            <label for="hidden">Hidden:</label> 
            <input type="hidden" name="hidden" id="hidden" value="12"><br>
            
            <input type="submit" value="Submit">
        </form>
    </section>
</body>
</html>
```

## HTML5 New Input Types Example (from PDF Page 19)

```html
<form name="user_form" method="post" action="/my_action">
    <label for="date">Date</label> 
    <input type="date" name="date" id="date" value=""><br>
    
    <label for="time">Time</label> 
    <input type="time" name="time" id="time" value=""><br>
    
    <label for="DateTime">DateTime</label> 
    <input type="datetime-local" name="DateTime" id="DateTime" value=""><br>
    
    <label for="email">Email</label> 
    <input type="email" name="email" id="email" value=""><br>
    
    <label for="url">URL</label> 
    <input type="url" name="url" id="url" value=""><br>
    
    <label for="number">Number</label> 
    <input type="number" name="number" id="number" value=""><br>
    
    <label for="range">Range</label> 
    <input type="range" name="range" id="range" value=""><br>
    
    <label for="tel">Telephone</label> 
    <input type="tel" name="tel" id="tel" value=""><br>
    
    <label for="color">Color</label> 
    <input type="color" name="color" id="color" value=""><br>
</form>
```

## Output & Progress Elements

```html
<!-- Output element -->
<form oninput="result.value = parseInt(a.value) + parseInt(b.value)">
    <input type="number" id="a" name="a" value="10"> +
    <input type="number" id="b" name="b" value="20"> =
    <output name="result" for="a b">30</output>
</form>

<!-- Progress bar -->
<label for="upload">Upload progress:</label>
<progress id="upload" value="70" max="100">70%</progress>

<!-- Meter (gauge) -->
<label for="disk">Disk usage:</label>
<meter id="disk" value="0.7" min="0" max="1" 
       low="0.3" high="0.7" optimum="0.2">70%</meter>
```

---

<a name="part-m"></a>
# 🅼 PART M: SEMANTIC vs NON-SEMANTIC ELEMENTS

## 📖 Theory (from PDF)

### Semantic Elements
> Semantic elements clearly describe the **purpose of content** they contain to both **browser and developer**.

### Non-Semantic Elements
> A non-semantic element **doesn't have any meaning**. They don't tell anything about the content they contain. Used for **grouping purpose only**.

## Semantic Elements (from PDF)

| Tag | Description (from PDF) | Code |
|-----|----------------------|------|
| `<article>` | Used to define an article | `<article></article>` |
| `<section>` | Represents thematic grouping. Defines sections like chapters, headers | `<section></section>` |
| `<mark>` | Used to mark or highlight content | `<mark>highlighted</mark>` |
| `<figure>` | Used to add self-contained content like illustrations, diagrams, photos | See below |
| `<figcaption>` | Used to set caption for image | Used inside `<figure>` |
| `<details>` | Content initially hidden but can be displayed if user wants to see it | See below |
| `<summary>` | Used with details tag to specify visible heading | Inside `<details>` |
| `<header>` | Used to define introductory content. Contains headings, logos, navigation | `<header></header>` |
| `<main>` | Used to encapsulate the main content | `<main></main>` |
| `<footer>` | Defines footer section. Contains copyright, contact details, social links | `<footer></footer>` |
| `<nav>` | Navigation section | `<nav></nav>` |
| `<aside>` | Content not essential to page, displayed beside main content | `<aside></aside>` |
| `<time>` | Date/time | `<time datetime="2025-01-15">` |
| `<address>` | Contact information | `<address></address>` |

## Figure & Figcaption (from PDF)

```html
<figure>
    <img src="photo.jpg" alt="Nature scene">
    <figcaption>A beautiful nature photograph</figcaption>
</figure>
```

## Details & Summary (from PDF)

> Used for content or information which is initially **hidden** but could be displayed if user wants to see it.

```html
<details>
    <summary>More Info</summary>
    <p>This is the additional information that can be revealed 
       by clicking the summary.</p>
</details>

<!-- Open by default -->
<details open>
    <summary>Already expanded</summary>
    <p>Visible from the start</p>
</details>

<!-- Exclusive accordion (NEW 2024 — only one open at a time) -->
<details name="faq">
    <summary>Question 1?</summary>
    <p>Answer 1</p>
</details>
<details name="faq">
    <summary>Question 2?</summary>
    <p>Answer 2</p>
</details>
```

## Non-Semantic Elements (from PDF)

### 1. Div (from PDF)
> It's a **generic container** for grouping other HTML elements together. It does not provide any specific meaning or structure on its own but is commonly used for **layout and styling purposes**.

```html
<div class="card">
    <h3>Card Title</h3>
    <p>Card content</p>
</div>
```

### 2. Span (from PDF)
> The `<span>` tag in HTML is an **inline, non-semantic element** used to group and style a portion of text or other inline elements. It does not provide any meaning or structure but is useful for applying **CSS styles** or **JavaScript functions** to a specific part of content.

```html
<p>My favorite color is <span style="color: blue;">blue</span>.</p>
<p>The price is <span class="price">$29.99</span></p>
```

## Semantic vs Non-Semantic Comparison

```html
<!-- ❌ Non-semantic (div soup) — No meaning! -->
<div class="header">
    <div class="nav">
        <div class="nav-item">Home</div>
    </div>
</div>
<div class="main">
    <div class="article">
        <div class="title">My Article</div>
    </div>
    <div class="sidebar">...</div>
</div>
<div class="footer">Copyright 2025</div>

<!-- ✅ Semantic — Meaningful to browser, search engines, screen readers! -->
<header>
    <nav>
        <a href="/">Home</a>
    </nav>
</header>
<main>
    <article>
        <h1>My Article</h1>
        <p>Content here...</p>
    </article>
    <aside>...</aside>
</main>
<footer>Copyright 2025</footer>
```

> 💡 **Rule:** Always prefer semantic tags over `<div>` and `<span>`. Only use generic containers when **no semantic alternative exists**.

---

<a name="part-n"></a>
# 🅽 PART N: HTML LAYOUT & PAGE STRUCTURE

## 📖 Theory (from PDF)

> To make a good website experience for the user, HTML provides elements to design an **HTML layout** to make a website look awesome.

## Layout Tags (from PDF Page 21)

| Tag | Description (from PDF) |
|-----|----------------------|
| `<div>` | Most used tag for designing HTML pages. Container for HTML elements. Using div we can divide pages into different blocks and add style to each div |
| `<section>` | Allows us to divide page in sections |
| `<p>` | Allows us to define paragraph |
| `<header>` | Allows us to add header in the webpage |
| `<footer>` | Allows us to add footer in the webpage |
| `<aside>` | Identifies content not essential to the page, displayed in separate box or beside main content |
| `<hr>` | Used to add horizontal line between two elements |
| `<br>` | Used to add line break |

## Layout Example (from PDF Page 22)

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Layout</title>
    <style>
        .header, .footer {
            background-color: #003366;
            color: white;
            text-align: center;
            padding: 10px;
        }
        .section {
            padding: 50px;
        }
        html {
            font-family: Arial, Helvetica, sans-serif;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <img width="50" height="50" src="logo.svg" alt="HTML Logo">
        This is an HTML Header
    </header>
    
    <!-- Main Content -->
    <section class="section">
        <div><h1>Title of the Page</h1></div>
        <hr>
        <div>HTML stands for HyperText Markup Language. It is a 
             markup language used to create web pages...</div>
        <p>This is sample paragraph text</p>
    </section>
    
    <!-- Footer -->
    <footer class="footer">
        This is an HTML Footer
    </footer>
</body>
</html>
```

## Complete Modern Semantic Layout

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semantic Blog Layout</title>
</head>
<body>
    <header>
        <h1>My Tech Blog</h1>
        <nav aria-label="Primary Navigation">
            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="/blog">Blog</a></li>
                <li><a href="/about">About</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <article>
            <header>
                <h2>Understanding HTML5 Semantics</h2>
                <p>By <address style="display:inline">Jane Doe</address>
                   on <time datetime="2025-01-15">January 15, 2025</time></p>
            </header>
            
            <section>
                <h3>Introduction</h3>
                <p>Semantic HTML is the foundation of accessible web development...</p>
            </section>
            
            <section>
                <h3>Key Elements</h3>
                <figure>
                    <img src="semantic-layout.png" alt="Semantic HTML layout diagram">
                    <figcaption>Fig 1: A typical semantic HTML page structure</figcaption>
                </figure>
            </section>
            
            <footer>
                <p>Tags: <a href="/tag/html">HTML</a>, <a href="/tag/web-dev">Web Dev</a></p>
            </footer>
        </article>
    </main>

    <aside aria-label="Sidebar">
        <section>
            <h3>About the Author</h3>
            <p>Jane is a web developer with 10 years of experience.</p>
        </section>
    </aside>

    <footer>
        <p><small>&copy; 2025 My Tech Blog. All rights reserved.</small></p>
    </footer>
</body>
</html>
```

---

<a name="part-o"></a>
# 🅾️ PART O: MULTIMEDIA — AUDIO & VIDEO

## 📖 Theory (from PDF)

> The HTML `<audio>` and `<video>` tags are used to embed media (audio and video files) directly into a webpage. They provide a simple way to include multimedia content with **built-in controls** such as play, pause, volume, and more.

## Video (from PDF)

> If you want to add video in HTML page, use `<video>` tag. The **controls** attribute adds video controls like play, pause, and volume. **width** and **height** define video dimensions. **source** allows us to specify video files — we can add alternative files.

### Video Attributes (from PDF):
| Attribute | Description |
|-----------|-------------|
| `controls` | Adds play/pause/volume controls |
| `autoplay` | Starts playing automatically |
| `width/height` | Dimensions |
| `src` (via `<source>`) | Source of video |
| `type` (via `<source>`) | Type of source |

```html
<!-- Video example from PDF -->
<video width="320" height="240" controls>
    <source src="video.mp4" type="video/mp4">
    Your browser does not support the video element.
</video>

<!-- Advanced video with multiple sources -->
<video controls autoplay muted loop poster="thumbnail.jpg"
       width="640" height="360" preload="metadata">
    <source src="video.webm" type="video/webm">
    <source src="video.mp4" type="video/mp4">
    <source src="video.ogg" type="video/ogg">
    <track src="subtitles_en.vtt" kind="subtitles" srclang="en" 
           label="English" default>
    <p>Your browser doesn't support HTML5 video. 
       <a href="video.mp4">Download the video</a>.</p>
</video>
```

## Audio (from PDF)

> If you want to add audio in HTML page, use `<audio>` tag. The **controls** attribute adds audio controls like play, pause, and volume. **source** allows us to specify audio files. To add autoplay, add the `autoplay` attribute.

```html
<!-- Audio example from PDF -->
<audio width="320" height="240" controls>
    <source src="audiofile.mp3" type="audio/mpeg" autoplay>
    <source src="audiofile.ogg" type="audio/ogg">
    Your browser does not support the audio element.
</audio>

<!-- Clean audio example -->
<audio controls preload="metadata">
    <source src="song.ogg" type="audio/ogg">
    <source src="song.mp3" type="audio/mpeg">
    <p>Your browser doesn't support HTML5 audio.</p>
</audio>
```

## All Video/Audio Attributes

| Attribute | Description |
|-----------|-------------|
| `controls` | Show play/pause/volume controls |
| `autoplay` | Start playing automatically |
| `muted` | Mute audio (**required for autoplay** in most browsers) |
| `loop` | Loop the media |
| `poster` | (Video only) Image shown before video plays |
| `preload` | `none`, `metadata`, or `auto` |
| `playsinline` | Play inline on mobile (not fullscreen) |

> ⚠️ **Note from PDF:** To add the autoplay feature, add the `autoplay` attribute. But most modern browsers require `muted` along with `autoplay` for it to work.

---

<a name="part-p"></a>
# 🅿️ PART P: IFRAMES & EMBEDS

## 📖 Theory (from PDF)

> `<iframe>` tag specifies the **inline frame**. It is used to contain or embed another HTML document within the current HTML document. It's commonly used to display content from other websites, like **videos, maps, or other web pages**, inside a small section of the main page.

## Iframe Attributes (from PDF)

| Attribute | Description |
|-----------|-------------|
| `src` | Specifies the address of document to embed |
| `width` | Width of the iframe |
| `height` | Height of the iframe |

```html
<!-- Basic iframe (from PDF) -->
<iframe src="home.html" width="100" height="100"></iframe>

<!-- Embed YouTube video -->
<iframe width="560" height="315" 
        src="https://www.youtube.com/embed/VIDEO_ID" 
        title="YouTube video player"
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media" 
        allowfullscreen
        loading="lazy">
</iframe>

<!-- Embed Google Maps -->
<iframe src="https://www.google.com/maps/embed?..." 
        width="600" height="450" 
        style="border:0;" 
        allowfullscreen="" 
        loading="lazy" 
        title="Google Maps location">
</iframe>

<!-- Sandboxed iframe (security) -->
<iframe src="untrusted.html" 
        sandbox="allow-scripts allow-same-origin"
        title="Sandboxed content">
</iframe>
```

## Embed & Object

```html
<!-- Embed PDF -->
<embed src="document.pdf" type="application/pdf" width="800" height="600">

<!-- Object with fallback -->
<object data="document.pdf" type="application/pdf" width="800" height="600">
    <p>Unable to display PDF. <a href="document.pdf">Download it</a>.</p>
</object>
```

> ⚠️ **Security Warning:** Be cautious with iframes! Use `sandbox` attribute to prevent attacks.

---

<a name="part-q"></a>
# 🆀 PART Q: HTML ENTITIES & SPECIAL CHARACTERS

## 📖 Theory (from PDF)

> HTML character entities are **special codes** used in HTML to represent reserved or special characters. They are used when you want to display a character that might otherwise be interpreted as HTML code. Entities start with an **ampersand (&)** and end with a **semicolon (;)**.

## Common Entities

| Character | Entity Name | Entity Number | Description |
|-----------|------------|---------------|-------------|
| `<` | `&lt;` | `&#60;` | Less than |
| `>` | `&gt;` | `&#62;` | Greater than |
| `&` | `&amp;` | `&#38;` | Ampersand |
| `"` | `&quot;` | `&#34;` | Double quote |
| `'` | `&apos;` | `&#39;` | Apostrophe |
| ` ` | `&nbsp;` | `&#160;` | Non-breaking space |
| `©` | `&copy;` | `&#169;` | Copyright |
| `®` | `&reg;` | `&#174;` | Registered |
| `™` | `&trade;` | `&#8482;` | Trademark |
| `€` | `&euro;` | `&#8364;` | Euro |
| `£` | `&pound;` | `&#163;` | Pound |
| `₹` | | `&#8377;` | Indian Rupee |
| `→` | `&rarr;` | `&#8594;` | Right arrow |
| `♥` | `&hearts;` | `&#9829;` | Heart |
| `—` | `&mdash;` | `&#8212;` | Em dash |
| `°` | `&deg;` | `&#176;` | Degree |

```html
<!-- Use entities to display HTML code as text -->
<p>The &lt;p&gt; tag defines a paragraph.</p>
<!-- Renders: The <p> tag defines a paragraph. -->

<!-- Non-breaking space for multiple spaces -->
<p>Word&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Word</p>

<!-- Emojis work directly in HTML5! -->
<p>🚀 Rocket ❤️ Heart ⭐ Star</p>
```

---

<a name="part-r"></a>
# 🆁 PART R: META TAGS & SEO

## Essential Meta Tags

```html
<head>
    <!-- Character encoding -->
    <meta charset="UTF-8">
    
    <!-- Responsive design (MUST HAVE) -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Page description (shown in search results) -->
    <meta name="description" content="Learn HTML from zero to advanced. Best guide 2025.">
    
    <!-- Author -->
    <meta name="author" content="Your Name">
    
    <!-- Robots -->
    <meta name="robots" content="index, follow">
    
    <!-- Page title (most important SEO element!) -->
    <title>Learn HTML: Complete Guide 2025 | YourSite</title>
    
    <!-- Theme color (mobile browser) -->
    <meta name="theme-color" content="#007bff">
</head>
```

## Open Graph (Social Media Sharing)

```html
<meta property="og:title" content="Complete HTML Guide 2025">
<meta property="og:description" content="Learn HTML from zero to advanced">
<meta property="og:image" content="https://yoursite.com/og-image.jpg">
<meta property="og:url" content="https://yoursite.com/html-guide">
<meta property="og:type" content="article">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Complete HTML Guide 2025">
```

## Favicon

```html
<link rel="icon" type="image/x-icon" href="/favicon.ico">
<link rel="icon" type="image/svg+xml" href="/favicon.svg">
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
```

## Performance Hints

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preload" href="critical-font.woff2" as="font" type="font/woff2" crossorigin>
<link rel="prefetch" href="/next-page.html">
```

---

<a name="part-s"></a>
# 🆂 PART S: BLOCK vs INLINE ELEMENTS

## Block Elements
- Take **full width** available
- Start on a **new line**
- Can contain other block and inline elements

```
Block: <div> <h1>-<h6> <p> <ul>/<ol> <li> <table> <form>
       <header> <footer> <main> <section> <article> <aside>
       <nav> <figure> <details> <blockquote> <pre> <hr>
       <fieldset> <address> <dialog>
```

## Inline Elements
- Take only the **space they need**
- **Don't** start on a new line
- Should NOT contain block elements

```
Inline: <span> <a> <strong> <em> <code> <img> <input>
        <button> <select> <textarea> <label> <br> <b> <i>
        <u> <small> <mark> <sub> <sup> <abbr> <cite> <q>
        <time> <kbd> <samp> <var>
```

> 💡 **Tip:** `<div>` = generic **block** container. `<span>` = generic **inline** container.

---

<a name="part-t"></a>
# 🆃 PART T: ADDING CSS & JAVASCRIPT TO HTML

## Adding CSS (from PDF)

> The Cascading Style Sheets (CSS) is code used to format the layout of your website. CSS helps you make changes to appearance — text, fonts, colors, images, spacing. You can create and add custom fonts.

### Three Ways to Add CSS (from PDF)

| Way | Description (from PDF) | Priority |
|-----|----------------------|----------|
| **External** | Add external CSS file using `<link>` tag | Lowest |
| **Internal** | Add CSS in head section using `<style>` tag | Medium |
| **Inline** | Add CSS inside HTML tag using `style` attribute | Highest |

```html
<!DOCTYPE html>
<html>
<head>
    <title>Adding CSS</title>
    
    <!-- External CSS file -->
    <link rel="stylesheet" type="text/css" href="../css/styles.css">
    
    <!-- Internal CSS -->
    <style>
        .section {
            background-color: aqua;
        }
    </style>
</head>
<body>
    <section class="section">
        <div>
            <!-- Inline style -->
            <h1 style="font-size: 20px;">Adding CSS</h1>
        </div>
    </section>
</body>
</html>
```

## Adding JavaScript (from PDF)

> JavaScript is a language widely used for creating **interactive web pages**. You can add menus, popup windows, photo galleries, and dynamic elements. JavaScript is executed in the **user's web browser**.

```html
<!-- Internal JavaScript -->
<script>
    alert("Hello World!");
</script>

<!-- External JavaScript (place at bottom of body for performance) -->
<script src="script.js"></script>

<!-- Defer: Downloads in parallel, executes AFTER HTML parsing -->
<script src="app.js" defer></script>

<!-- Async: Downloads in parallel, executes IMMEDIATELY when ready -->
<script src="analytics.js" async></script>

<!-- Module: Deferred by default -->
<script type="module" src="app.mjs"></script>
```

### Script Loading Visualization:

```
REGULAR:   HTML ——[pause]—— Script ——[resume]—— HTML
DEFER:     HTML ————————————————————HTML  →  Script
ASYNC:     HTML ————Script———————HTML (interrupts when ready)
MODULE:    HTML ————————————————————HTML  →  Module
```

---

<a name="part-u"></a>
# 🆄 PART U: HTML COMMENTS

## From PDF (Page 20)

> To comment the code in HTML the following syntax is used.

```html
<!-- This is HTML Comment -->
<h1>Hello World</h1>

<!-- Single line comment -->

<!--
    Multi-line
    comment
    block
-->

<!-- 
    Comments are NOT shown in the browser.
    Use them to:
    1. Document your code
    2. Temporarily disable code
    3. Leave notes for other developers
-->

<!-- <p>This paragraph is commented out — won't render</p> -->
```

> 💡 **VS Code Shortcut:** `Ctrl + /` (Windows) or `Cmd + /` (Mac) toggles comments.

---

<a name="part-v"></a>
# 🆅 PART V: PREFORMATTED TEXT & CODE TAGS

## Pre Tag (from PDF)

> The `<pre>` tag in HTML is used to display **preformatted text**. It preserves both **spaces and line breaks** as they appear in the HTML code, meaning the text is displayed exactly as it is written inside the tag.

```html
<pre>
    This text will appear
    exactly as written, 
    with line breaks and
    multiple    spaces.
</pre>
```

## Code Tags

```html
<!-- Inline code -->
<p>Use the <code>console.log()</code> function to debug.</p>

<!-- Code block (pre + code) -->
<pre><code>
function greet(name) {
    return `Hello, ${name}!`;
}
</code></pre>

<!-- Keyboard input -->
<p>Press <kbd>Ctrl</kbd> + <kbd>S</kbd> to save.</p>

<!-- Sample output -->
<samp>Error: File not found</samp>

<!-- Variable -->
<p>The area is <var>l</var> × <var>w</var></p>
```

---

<a name="part-w"></a>
# 🆆 PART W: IMAGE MAPS

## 📖 Theory (from PDF)

> An image map in HTML allows you to define **clickable areas (hotspots)** on an image that link to different destinations. You can create interactive images where different parts of the image lead to different URLs.

## Image Map Code (from PDF)

```html
<img src="image.jpg" alt="Image with map" usemap="#mapname">

<map name="mapname">
    <area shape="rect" coords="34,44,270,350" 
          href="https://example.com/page1" alt="Link 1">
    <area shape="circle" coords="337,300,44" 
          href="https://example.com/page2" alt="Link 2">
    <area shape="poly" coords="220,210,300,250,260,300" 
          href="https://example.com/page3" alt="Link 3">
</map>
```

### Shape Types:
| Shape | `coords` Format | Description |
|-------|----------------|-------------|
| `rect` | x1,y1,x2,y2 | Rectangle (top-left, bottom-right) |
| `circle` | x,y,radius | Circle (center x, center y, radius) |
| `poly` | x1,y1,x2,y2,... | Polygon (series of x,y points) |

---

<a name="part-x"></a>
# 🆇 PART X: HTML5 APIS & MODERN FEATURES

## Dialog Element (Native Modal)

```html
<dialog id="myDialog">
    <h2>Confirm Action</h2>
    <p>Are you sure?</p>
    <form method="dialog">
        <button value="cancel">Cancel</button>
        <button value="confirm">Confirm</button>
    </form>
</dialog>

<button onclick="myDialog.showModal()">Open Dialog</button>
```

## Popover API (NEW 2024!)

```html
<!-- No JavaScript needed! -->
<button popovertarget="mypopover">Toggle Popover</button>
<div id="mypopover" popover>
    <h3>Popover Content</h3>
    <p>Click outside to close.</p>
</div>
```

## Content Editable

```html
<div contenteditable="true" style="border: 1px solid #ccc; padding: 15px;">
    <h2>Click and edit this heading!</h2>
    <p>You can type here directly in the browser.</p>
</div>
```

## Web Storage

```html
<script>
// localStorage — persists even after browser closes
localStorage.setItem('username', 'John');
console.log(localStorage.getItem('username')); // "John"

// sessionStorage — cleared when tab closes
sessionStorage.setItem('tempData', 'Temporary');
</script>
```

## Geolocation API

```html
<button onclick="getLocation()">📍 Get My Location</button>
<p id="location"></p>

<script>
function getLocation() {
    if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition((pos) => {
            document.getElementById('location').innerHTML = 
                `Lat: ${pos.coords.latitude}, Lng: ${pos.coords.longitude}`;
        });
    }
}
</script>
```

## Search Element (NEW 2023!)

```html
<search>
    <form action="/search" method="GET">
        <input type="search" name="q" placeholder="Search...">
        <button type="submit">🔍</button>
    </form>
</search>
```

## Inert Attribute (NEW!)

```html
<!-- Makes entire section non-interactive -->
<div inert>
    <button>Can't click me</button>
    <input type="text" placeholder="Can't type here">
</div>
```

---

<a name="part-y"></a>
# 🆈 PART Y: ACCESSIBILITY (a11y)

## ARIA Attributes

```html
<!-- Landmarks -->
<nav role="navigation" aria-label="Main Menu">...</nav>

<!-- Labels for screen readers -->
<button aria-label="Close dialog">✕</button>

<!-- Live regions (announce dynamic changes) -->
<div aria-live="polite" id="status">Ready</div>

<!-- Hidden from screen readers (decorative) -->
<span aria-hidden="true">🎨</span>

<!-- Skip navigation -->
<a href="#main-content" class="skip-link">Skip to main content</a>

<!-- Current page in navigation -->
<a href="/" aria-current="page">Home</a>
```

## Accessibility Checklist

```
✅ All images have descriptive alt text
✅ All form inputs have labels
✅ Color is NOT the only way to convey information
✅ Sufficient color contrast (4.5:1 for text)
✅ Page navigable with keyboard only
✅ Focus indicators are visible
✅ Heading hierarchy is logical (h1 → h2 → h3)
✅ Language declared (<html lang="en">)
✅ Page has descriptive <title>
✅ Links have descriptive text (not "click here")
✅ Media has captions/transcripts
```

---

<a name="part-z"></a>
# 🆉 PART Z: GRAPHICS — CANVAS & SVG

## SVG

```html
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
    <circle cx="100" cy="100" r="80" fill="#007bff"/>
    <text x="100" y="108" text-anchor="middle" fill="white" font-size="20">SVG</text>
</svg>
```

## Canvas

```html
<canvas id="myCanvas" width="400" height="200"></canvas>
<script>
const ctx = document.getElementById('myCanvas').getContext('2d');
ctx.fillStyle = '#007bff';
ctx.fillRect(20, 20, 150, 100);
ctx.font = 'bold 20px Arial';
ctx.fillText('Hello Canvas!', 200, 80);
</script>
```

## SVG vs Canvas

| Feature | SVG | Canvas |
|---------|-----|--------|
| Type | Vector | Raster (pixels) |
| Scalability | Infinite | Pixelates on zoom |
| Best for | Icons, logos, charts | Games, image editing |
| Accessibility | Better (text readable) | Poor |

---

<a name="all-tags"></a>
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

<a name="data-attr"></a>
# 📊 DATA ATTRIBUTES

```html
<!-- Store custom data on elements -->
<div data-user-id="123" data-role="admin" data-active="true">
    <h3>John Doe</h3>
</div>

<script>
const el = document.querySelector('[data-user-id]');
console.log(el.dataset.userId);   // "123" (camelCase)
console.log(el.dataset.role);     // "admin"
</script>

<style>
[data-role="admin"] { border-left: 4px solid red; }
[data-active]::after { content: " ✓"; color: green; }
</style>
```

---

<a name="web-comp"></a>
# 🧩 WEB COMPONENTS & TEMPLATES

```html
<template id="greeting-template">
    <style>
        .greeting { padding: 20px; background: #f0f8ff; border-radius: 10px; }
    </style>
    <div class="greeting">
        <slot name="title"><h2>Hello!</h2></slot>
        <slot>Default content here</slot>
    </div>
</template>

<script>
class GreetingCard extends HTMLElement {
    constructor() {
        super();
        const shadow = this.attachShadow({ mode: 'open' });
        const template = document.getElementById('greeting-template');
        shadow.appendChild(template.content.cloneNode(true));
    }
}
customElements.define('greeting-card', GreetingCard);
</script>

<greeting-card>
    <h2 slot="title">Welcome!</h2>
    <p>Custom content goes here.</p>
</greeting-card>
```

---

<a name="performance"></a>
# ⚡ PERFORMANCE & BEST PRACTICES

```html
<!-- 1. Lazy load images below the fold -->
<img src="photo.jpg" alt="..." loading="lazy" decoding="async">

<!-- 2. Specify dimensions to prevent layout shift -->
<img src="photo.jpg" alt="..." width="800" height="600">

<!-- 3. Modern image formats with fallback -->
<picture>
    <source srcset="image.avif" type="image/avif">
    <source srcset="image.webp" type="image/webp">
    <img src="image.jpg" alt="..." loading="lazy">
</picture>

<!-- 4. Preconnect to external domains -->
<link rel="preconnect" href="https://fonts.googleapis.com">

<!-- 5. Defer non-critical JS -->
<script src="app.js" defer></script>

<!-- 6. Fetchpriority for critical resources -->
<img src="hero.jpg" alt="..." fetchpriority="high">
```

## Do's and Don'ts

```
✅ DO:
  • Use semantic HTML tags
  • Always include alt text
  • Use <label> for all form inputs
  • Validate HTML (validator.w3.org)
  • Use responsive images
  • Include lang attribute
  • Use meta viewport for mobile

❌ DON'T:
  • Use tables for layout
  • Skip heading levels
  • Use <br> for spacing (use CSS)
  • Use deprecated tags
  • Forget to close tags
  • Autoplay video with sound
  • Use div when semantic tag exists
```

---

<a name="tips"></a>
# 💡 TIPS & TRICKS

### 1. VS Code Emmet Power Shortcuts
```
!                          → Full boilerplate
nav>ul>li*5>a{Item $}      → Nav with 5 numbered links
.container>.row>.col*3     → Nested divs with classes
lorem                      → Lorem ipsum text
```

### 2. Input Mode for Better Mobile Keyboards
```html
<input inputmode="numeric">   <!-- Number pad -->
<input inputmode="tel">       <!-- Phone pad -->
<input inputmode="email">     <!-- @ and .com keys -->
```

### 3. Custom Enter Key Label (Mobile)
```html
<input enterkeyhint="search">  <!-- 🔍 -->
<input enterkeyhint="send">    <!-- ➤ -->
<input enterkeyhint="go">      <!-- Go -->
```

### 4. Native Accordion Without JS
```html
<details name="accordion"><summary>Section 1</summary><p>Content</p></details>
<details name="accordion"><summary>Section 2</summary><p>Content</p></details>
```

### 5. Make Any Element Editable
```html
<div contenteditable="true">Edit me directly!</div>
```

### 6. HTML Validation
```
Online: https://validator.w3.org/
VS Code: W3C Web Validator extension
```

---

<a name="projects"></a>
# 🏗️ MINI PROJECTS

## 🟢 Project 1: Personal Bio Page (Beginner)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Me</title>
    <style>
        body { font-family: Arial, sans-serif; max-width: 600px; margin: 50px auto; 
               padding: 20px; background: #f5f5f5; }
        .card { background: white; padding: 30px; border-radius: 15px; 
                box-shadow: 0 2px 10px rgba(0,0,0,0.1); text-align: center; }
        img { border-radius: 50%; width: 150px; height: 150px; object-fit: cover; }
        h1 { color: #333; margin: 15px 0 5px; }
        .subtitle { color: #667; font-style: italic; }
        .skills { display: flex; flex-wrap: wrap; gap: 8px; justify-content: center; margin: 20px 0; }
        .skill { background: #e7f1ff; color: #007bff; padding: 5px 15px; border-radius: 20px; font-size: 14px; }
        a { color: #007bff; text-decoration: none; }
        a:hover { text-decoration: underline; }
    </style>
</head>
<body>
    <div class="card">
        <img src="https://via.placeholder.com/150" alt="My Photo">
        <h1>Your Name</h1>
        <p class="subtitle">Web Developer & Designer</p>
        <hr>
        <h3>About Me</h3>
        <p>I'm a passionate web developer learning HTML, CSS, and JavaScript. 
           I love building beautiful and accessible websites.</p>
        <h3>Skills</h3>
        <div class="skills">
            <span class="skill">HTML5</span>
            <span class="skill">CSS3</span>
            <span class="skill">JavaScript</span>
            <span class="skill">React</span>
            <span class="skill">Git</span>
        </div>
        <h3>Contact</h3>
        <p>
            📧 <a href="mailto:you@example.com">you@example.com</a><br>
            🔗 <a href="https://github.com/you" target="_blank">GitHub</a>
        </p>
    </div>
</body>
</html>
```

## 🟡 Project 2: FAQ Accordion (Intermediate — No JS!)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FAQ</title>
    <style>
        body { font-family: 'Segoe UI', sans-serif; background: #f0f2f5; 
               display: flex; justify-content: center; padding: 40px 20px; }
        .faq { max-width: 700px; width: 100%; }
        h1 { text-align: center; color: #1a1a2e; }
        details { background: white; margin-bottom: 10px; border-radius: 10px;
                  box-shadow: 0 2px 5px rgba(0,0,0,0.05); overflow: hidden; }
        details[open] { border-left: 4px solid #e94560; }
        summary { padding: 20px; cursor: pointer; font-weight: 600;
                  font-size: 1.1em; list-style: none; }
        summary::-webkit-details-marker { display: none; }
        summary::after { content: '+'; float: right; font-size: 1.5em; color: #e94560; }
        details[open] summary::after { content: '−'; }
        details p { padding: 0 20px 20px; color: #555; line-height: 1.8; }
    </style>
</head>
<body>
    <div class="faq">
        <h1>❓ Frequently Asked Questions</h1>
        
        <details name="faq">
            <summary>What is HTML?</summary>
            <p>HTML (HyperText Markup Language) is the standard language for 
               creating web pages. It describes the structure and content.</p>
        </details>
        <details name="faq">
            <summary>Is HTML a programming language?</summary>
            <p>No, HTML is a markup language, not a programming language. 
               It doesn't have logic, loops, or conditions.</p>
        </details>
        <details name="faq">
            <summary>What's new in HTML5?</summary>
            <p>HTML5 introduced semantic elements, multimedia support, 
               canvas, new form input types, and many APIs.</p>
        </details>
        <details name="faq">
            <summary>How do I make my website responsive?</summary>
            <p>Start with the viewport meta tag, then use CSS media queries, 
               flexible grids, and responsive images.</p>
        </details>
    </div>
</body>
</html>
```

## 🔴 Project 3: Registration Form (Advanced)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { font-family: 'Segoe UI', sans-serif; background: #667eea; 
               min-height: 100vh; display: flex; align-items: center; justify-content: center; padding: 20px; }
        form { max-width: 500px; width: 100%; background: white; padding: 40px; 
               border-radius: 15px; box-shadow: 0 10px 40px rgba(0,0,0,0.2); }
        h2 { text-align: center; margin-bottom: 25px; color: #333; }
        fieldset { border: 1px solid #eee; padding: 15px; margin-bottom: 15px; border-radius: 8px; }
        legend { font-weight: bold; color: #667eea; padding: 0 10px; }
        label { display: block; margin: 10px 0 5px; font-weight: 600; color: #555; }
        input, select, textarea { width: 100%; padding: 10px; border: 2px solid #eee; 
                                   border-radius: 8px; font-size: 14px; transition: 0.3s; }
        input:focus, select:focus, textarea:focus { outline: none; border-color: #667eea; }
        input:valid:not(:placeholder-shown) { border-color: #28a745; }
        .checkbox-row { display: flex; align-items: center; gap: 10px; margin: 15px 0; }
        .checkbox-row input { width: auto; }
        button { width: 100%; padding: 12px; background: #667eea; color: white; 
                 border: none; border-radius: 8px; font-size: 16px; cursor: pointer; font-weight: 600; }
        button:hover { background: #5a6fd6; }
    </style>
</head>
<body>
    <form action="/register" method="POST">
        <h2>🚀 Create Account</h2>
        
        <fieldset>
            <legend>👤 Personal Info</legend>
            <label for="name">Full Name *</label>
            <input type="text" id="name" name="name" placeholder="John Doe" required minlength="2">
            
            <label for="email">Email *</label>
            <input type="email" id="email" name="email" placeholder="john@example.com" required>
            
            <label for="phone">Phone</label>
            <input type="tel" id="phone" name="phone" placeholder="123-456-7890" inputmode="tel">
            
            <label for="dob">Date of Birth</label>
            <input type="date" id="dob" name="dob">
        </fieldset>
        
        <fieldset>
            <legend>🔐 Account</legend>
            <label for="username">Username *</label>
            <input type="text" id="username" name="username" placeholder="johndoe" required minlength="3">
            
            <label for="password">Password *</label>
            <input type="password" id="password" name="password" placeholder="Min 8 characters" required minlength="8">
            
            <label for="country">Country</label>
            <select id="country" name="country">
                <option value="">-- Select --</option>
                <optgroup label="Asia">
                    <option value="in">🇮🇳 India</option>
                    <option value="jp">🇯🇵 Japan</option>
                </optgroup>
                <optgroup label="Americas">
                    <option value="us">🇺🇸 United States</option>
                    <option value="ca">🇨🇦 Canada</option>
                </optgroup>
            </select>
            
            <label>Favorite Language</label>
            <input list="languages" name="language" placeholder="Start typing...">
            <datalist id="languages">
                <option value="JavaScript">
                <option value="Python">
                <option value="Java">
                <option value="C++">
            </datalist>
            
            <label for="bio">Bio</label>
            <textarea id="bio" name="bio" rows="3" placeholder="Tell us about yourself..." maxlength="300"></textarea>
        </fieldset>
        
        <div class="checkbox-row">
            <input type="checkbox" id="terms" name="terms" required>
            <label for="terms" style="display:inline; font-weight:normal;">
                I agree to the Terms & Conditions *
            </label>
        </div>
        
        <button type="submit">Create Account</button>
    </form>
</body>
</html>
```

---

<a name="trends"></a>
# 🔮 2024–2025 TRENDS & NEW FEATURES

| Feature | Status | Description |
|---------|--------|-------------|
| **Popover API** | ✅ Supported | Native popovers without JS |
| **Exclusive Accordion** | ✅ Chrome 120+ | `<details name="group">` — only one open |
| **`<search>` Element** | ✅ All browsers | Semantic search wrapper |
| **`fetchpriority`** | ✅ Supported | Priority hints for resources |
| **`inert` Attribute** | ✅ Supported | Makes content non-interactive |
| **`blocking="render"`** | ✅ Supported | Block rendering until resource loads |
| **Invoker Commands** | 🧪 Experimental | Declarative JS-free interactivity |
| **Speculation Rules** | 🧪 Chrome | Prerender next pages |
| **View Transitions** | 🧪 Shipping | Animated page transitions |
| **Custom `<select>`** | 🧪 Experimental | Fully customizable select elements |

---

# 🎯 LEARNING PATH

```
WEEK 1-2: BEGINNER
├── Parts A-F: Basics, Structure, Headings, Text
├── Parts G-I: Formatting, Links, Images
├── Part J: Lists
├── Part U: Comments
└── 🏗️ Project: Personal Bio Page

WEEK 3-4: INTERMEDIATE
├── Parts K-L: Tables, Forms (all types)
├── Parts M-N: Semantic HTML, Layouts
├── Parts O-P: Audio, Video, Iframes
├── Parts Q-T: Entities, Meta, CSS/JS integration
└── 🏗️ Project: FAQ Accordion + Registration Form

WEEK 5-6: ADVANCED
├── Parts X-Z: HTML5 APIs, Accessibility, Graphics
├── Data Attributes, Web Components, Templates
├── Performance Optimization
├── SEO, Structured Data
├── New 2024-2025 Features
└── 🏗️ Project: Multi-page Portfolio Website
```

---

# 📚 RESOURCES

- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)
- [HTML Living Standard](https://html.spec.whatwg.org/)
- [Can I Use](https://caniuse.com/) — Browser support checker
- [W3C Validator](https://validator.w3.org/)
- [web.dev by Google](https://web.dev/)

---

> 📝 **Credits:** PDF reference notes by **Atul Kumar** (Coding Bugs / Notes Gallery) have been integrated throughout this guide with proper attribution. Additional content from the second PDF section (Java By Satyajit) has also been incorporated.

*Made with ❤️ — Complete HTML Guide 2025*


# 📋 COVERAGE AUDIT & ADDITIONS

Let me first check what's covered and what's missing, then add everything remaining plus a massive practice section.

---

# ✅ COVERAGE CHECKLIST

| Topic | Covered? | Notes |
|-------|----------|-------|
| What is HTML, History | ✅ | |
| Tags, Elements, Attributes | ✅ | |
| Document Structure | ✅ | |
| Headings h1-h6 | ✅ | |
| Paragraphs, br, hr | ✅ | |
| Text Formatting (all) | ✅ | |
| Physical vs Logical Tags | ✅ | |
| Links/Anchor Tag | ✅ | |
| Images | ✅ | |
| Lists (ul, ol, dl, nested) | ✅ | |
| Tables | ✅ | |
| Forms (all input types) | ✅ | |
| Semantic vs Non-Semantic | ✅ | |
| Layout Tags | ✅ | |
| Audio & Video | ✅ | |
| Iframes | ✅ | |
| HTML Entities | ✅ | |
| Meta Tags & SEO | ✅ | |
| Block vs Inline | ✅ | |
| CSS Integration | ✅ | |
| JavaScript Integration | ✅ | |
| Comments | ✅ | |
| Pre & Code Tags | ✅ | |
| Image Maps | ✅ | |
| HTML5 APIs | ✅ | |
| Accessibility | ✅ | |
| Canvas & SVG | ✅ | |
| All Tags Reference | ✅ | |
| Data Attributes | ✅ | |
| Web Components | ✅ | |
| Performance | ✅ | |
| Projects | ✅ | |
| Trends 2024-25 | ✅ | |
| **Global Attributes (detail)** | ⚠️ Partial | Adding below |
| **URL Types (absolute/relative)** | ❌ Missing | Adding below |
| **File Paths** | ❌ Missing | Adding below |
| **Responsive Web Design HTML** | ❌ Missing | Adding below |
| **Favicon complete guide** | ⚠️ Partial | Adding below |
| **Character Encoding deep** | ❌ Missing | Adding below |
| **HTML vs XHTML** | ❌ Missing | Adding below |
| **HTML Validation** | ⚠️ Partial | Adding below |
| **Drag & Drop complete** | ⚠️ Partial | Adding below |
| **Web Workers mention** | ❌ Missing | Adding below |
| **Service Workers / PWA** | ⚠️ Partial | Adding below |
| **Microdata** | ❌ Missing | Adding below |
| **Content Security Policy** | ❌ Missing | Adding below |
| **Print Styles** | ❌ Missing | Adding below |
| **Common Mistakes** | ❌ Missing | Adding below |
| **Interview Questions** | ❌ Missing | Adding below |
| **Practice Tasks** | ❌ Missing | Adding below |

---

# 🆕 MISSING TOPICS — COMPLETE ADDITIONS

---

## 1️⃣ URL TYPES & FILE PATHS

### Absolute vs Relative URLs

```
ABSOLUTE URL (Full path — works from anywhere):
https://www.example.com/images/photo.jpg

RELATIVE URL (Relative to current file location):
images/photo.jpg        → Same folder → subfolder "images"
./images/photo.jpg      → Same (explicit current directory)
../images/photo.jpg     → Go UP one folder → then "images"
../../styles/main.css   → Go UP two folders → then "styles"
/images/photo.jpg       → From ROOT of the website
```

### File Path Examples

```
📁 my-website/
├── index.html          ← You are HERE
├── about.html
├── 📁 images/
│   ├── logo.png
│   └── hero.jpg
├── 📁 css/
│   └── style.css
├── 📁 pages/
│   ├── contact.html
│   └── 📁 blog/
│       └── post1.html
```

```html
<!-- FROM index.html -->
<img src="images/logo.png" alt="Logo">
<link rel="stylesheet" href="css/style.css">
<a href="about.html">About</a>
<a href="pages/contact.html">Contact</a>

<!-- FROM pages/contact.html -->
<img src="../images/logo.png" alt="Logo">      <!-- Go UP then into images -->
<link rel="stylesheet" href="../css/style.css"> <!-- Go UP then into css -->
<a href="../index.html">Home</a>               <!-- Go UP to root -->
<a href="blog/post1.html">Blog Post</a>        <!-- Go DOWN into blog -->

<!-- FROM pages/blog/post1.html -->
<img src="../../images/logo.png" alt="Logo">    <!-- Go UP twice -->
<a href="../../index.html">Home</a>
<a href="../contact.html">Contact</a>           <!-- Go UP once -->
```

### Protocol-Relative URLs
```html
<!-- Matches current protocol (http or https) — AVOID this now -->
<img src="//cdn.example.com/image.jpg">

<!-- ALWAYS use https:// instead -->
<img src="https://cdn.example.com/image.jpg">
```

### Special URL Schemes
```html
<a href="https://example.com">Website</a>
<a href="mailto:hi@example.com">Email</a>
<a href="tel:+1234567890">Phone</a>
<a href="sms:+1234567890">SMS</a>
<a href="javascript:void(0)">Do Nothing</a>  <!-- ❌ Bad practice -->
<a href="#section1">Same Page Anchor</a>
<a href="#">Back to Top</a>
<a href="file.pdf" download>Download</a>
```

---

## 2️⃣ RESPONSIVE WEB DESIGN (HTML Part)

### From the PDF:
> Responsive Web Design is about using HTML and CSS to automatically resize, hide, shrink, or enlarge a website, to make it look good on all devices (desktops, tablets, and phones).

### The Viewport Meta Tag (CRITICAL)

```html
<!-- WITHOUT this — mobile shows tiny desktop version -->
<!-- WITH this — mobile shows properly sized content -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Viewport Parameters

| Parameter | Description |
|-----------|-------------|
| `width=device-width` | Match screen width |
| `initial-scale=1.0` | Default zoom level |
| `maximum-scale=1.0` | Prevent zoom (NOT recommended for accessibility) |
| `user-scalable=no` | Disable pinch zoom (NOT recommended) |

### Responsive Images in HTML

```html
<!-- Method 1: Simple — max-width via CSS -->
<img src="photo.jpg" alt="..." style="max-width: 100%; height: auto;">

<!-- Method 2: srcset — browser picks best size -->
<img src="photo-800.jpg"
     srcset="photo-400.jpg 400w,
             photo-800.jpg 800w,
             photo-1200.jpg 1200w"
     sizes="(max-width: 600px) 400px,
            (max-width: 1000px) 800px,
            1200px"
     alt="Responsive photo">

<!-- Method 3: picture — different images per condition -->
<picture>
    <source media="(max-width: 600px)" srcset="mobile.jpg">
    <source media="(max-width: 1024px)" srcset="tablet.jpg">
    <img src="desktop.jpg" alt="Responsive">
</picture>

<!-- Method 4: Art direction — different crops -->
<picture>
    <source media="(max-width: 600px)" srcset="portrait-crop.jpg">
    <source media="(min-width: 601px)" srcset="landscape-full.jpg">
    <img src="landscape-full.jpg" alt="Photo">
</picture>
```

### Responsive Video
```html
<!-- Responsive video container -->
<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden;">
    <iframe src="https://www.youtube.com/embed/VIDEO_ID"
            style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
            frameborder="0" allowfullscreen loading="lazy">
    </iframe>
</div>
```

---

## 3️⃣ HTML vs XHTML

| Feature | HTML5 | XHTML |
|---------|-------|-------|
| Syntax | Lenient/forgiving | Strict XML rules |
| Case | Case-insensitive tags | Must be lowercase |
| Closing tags | Optional for some | ALL must be closed |
| Self-closing | `<br>` is fine | Must be `<br />` |
| Attributes | Can be unquoted | Must be quoted |
| Boolean attrs | `<input required>` OK | Must be `required="required"` |
| Error handling | Browser fixes errors | Must be well-formed |
| MIME type | `text/html` | `application/xhtml+xml` |

```html
<!-- Valid HTML5 (lenient) -->
<p>Unclosed paragraph
<br>
<img src=photo.jpg alt=Photo>
<input type=text required>

<!-- Valid XHTML (strict) -->
<p>Must be closed</p>
<br />
<img src="photo.jpg" alt="Photo" />
<input type="text" required="required" />
```

> 💡 **Modern Practice:** Write HTML5 but follow XHTML-style discipline — close all tags, use lowercase, quote attributes. Best of both worlds.

---

## 4️⃣ CHARACTER ENCODING

```html
<!-- UTF-8: Universal — supports ALL languages and symbols -->
<meta charset="UTF-8">

<!-- MUST be within first 1024 bytes of document -->
<!-- MUST appear before any content-containing elements -->
```

### Why UTF-8?
```
ASCII   → Only English (128 characters)
Latin-1 → Western European languages
UTF-8   → ALL languages + emojis + symbols (1,112,064 characters)
          Hindi: हिन्दी
          Chinese: 中文
          Arabic: العربية
          Emoji: 🚀❤️⭐
```

### Language & Direction
```html
<html lang="en">           <!-- English -->
<html lang="hi">           <!-- Hindi -->
<html lang="ar" dir="rtl"> <!-- Arabic, right-to-left -->
<html lang="ja">           <!-- Japanese -->

<!-- Mix languages in same page -->
<p>The word <span lang="fr">bonjour</span> means hello.</p>
```

---

## 5️⃣ HTML VALIDATION

### Common Validation Errors

```html
<!-- ❌ ERROR: Unclosed tag -->
<p>This paragraph is never closed
<p>Another one

<!-- ✅ FIX: -->
<p>This paragraph is closed</p>
<p>Another one</p>

<!-- ❌ ERROR: Nested incorrectly -->
<strong><em>Bold and italic</strong></em>

<!-- ✅ FIX: Close in reverse order -->
<strong><em>Bold and italic</em></strong>

<!-- ❌ ERROR: Duplicate ID -->
<div id="header">First</div>
<div id="header">Second</div>

<!-- ✅ FIX: Unique IDs -->
<div id="header">First</div>
<div id="sub-header">Second</div>

<!-- ❌ ERROR: Block inside inline -->
<span><div>Block inside inline</div></span>

<!-- ✅ FIX: -->
<div><span>Inline inside block</span></div>

<!-- ❌ ERROR: Missing alt on img -->
<img src="photo.jpg">

<!-- ✅ FIX: -->
<img src="photo.jpg" alt="Description of photo">

<!-- ❌ ERROR: Interactive inside interactive -->
<a href="#"><button>Click</button></a>

<!-- ✅ FIX: Use one or the other -->
<a href="#">Click</a>
<!-- OR -->
<button onclick="location.href='#'">Click</button>
```

### Validation Tools
```
🌐 Online:  https://validator.w3.org/
📦 VS Code: W3C Web Validator extension
🔧 CLI:     html-validate (npm package)
🌐 Browser: DevTools → Console (shows some HTML errors)
```

---

## 6️⃣ COMPLETE GLOBAL ATTRIBUTES

Every HTML element can use these attributes:

| Attribute | Description | Example |
|-----------|-------------|---------|
| `id` | Unique identifier (one per page) | `id="main-header"` |
| `class` | One or more CSS class names | `class="btn btn-primary"` |
| `style` | Inline CSS styles | `style="color: red;"` |
| `title` | Tooltip text on hover | `title="More information"` |
| `hidden` | Hides element completely | `hidden` |
| `lang` | Language of content | `lang="fr"` |
| `dir` | Text direction: `ltr`, `rtl`, `auto` | `dir="rtl"` |
| `tabindex` | Tab navigation order | `tabindex="1"` |
| `accesskey` | Keyboard shortcut | `accesskey="s"` |
| `contenteditable` | Makes content editable | `contenteditable="true"` |
| `draggable` | Makes element draggable | `draggable="true"` |
| `spellcheck` | Enable/disable spell check | `spellcheck="true"` |
| `translate` | Should be translated? | `translate="no"` |
| `data-*` | Custom data storage | `data-user-id="42"` |
| `autofocus` | Focus on page load | `autofocus` |
| `enterkeyhint` | Enter key label (mobile) | `enterkeyhint="search"` |
| `inputmode` | Virtual keyboard type | `inputmode="numeric"` |
| `is` | Custom element extension | `is="my-button"` |
| `slot` | Web component slot name | `slot="header"` |
| `part` | Shadow DOM part name | `part="button"` |
| `popover` | Popover behavior | `popover` |
| `inert` | Makes non-interactive | `inert` |
| `nonce` | Security nonce for CSP | `nonce="abc123"` |

### Event Attributes (Common)

```html
<!-- Mouse Events -->
onclick="handleClick()"
ondblclick="handleDblClick()"
onmousedown / onmouseup / onmousemove
onmouseover / onmouseout / onmouseenter / onmouseleave
oncontextmenu="handleRightClick()"

<!-- Keyboard Events -->
onkeydown / onkeyup / onkeypress

<!-- Form Events -->
onsubmit / onreset / oninput / onchange
onfocus / onblur / oninvalid

<!-- Window Events (on <body>) -->
onload / onunload / onresize / onscroll
onerror / onhashchange

<!-- Drag Events -->
ondrag / ondragstart / ondragend
ondragenter / ondragover / ondragleave / ondrop

<!-- Media Events -->
onplay / onpause / onended / onvolumechange
ontimeupdate / onloadeddata

<!-- Clipboard Events -->
oncopy / oncut / onpaste
```

---

## 7️⃣ DRAG AND DROP (Complete)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Drag & Drop</title>
    <style>
        .dropzone {
            width: 300px; height: 200px;
            border: 3px dashed #ccc;
            border-radius: 10px;
            display: flex; align-items: center; justify-content: center;
            margin: 20px; transition: 0.3s;
            font-size: 1.2em; color: #999;
        }
        .dropzone.over { border-color: #007bff; background: #e7f1ff; }
        .draggable {
            padding: 15px 25px; background: #007bff; color: white;
            border-radius: 8px; cursor: grab; display: inline-block;
            margin: 10px; font-weight: bold;
        }
        .draggable:active { cursor: grabbing; }
    </style>
</head>
<body>
    <h2>Drag the items into the box</h2>
    
    <div class="draggable" draggable="true" id="item1"
         ondragstart="event.dataTransfer.setData('text', event.target.id)">
        🎯 Item 1
    </div>
    <div class="draggable" draggable="true" id="item2"
         ondragstart="event.dataTransfer.setData('text', event.target.id)">
        ⭐ Item 2
    </div>
    
    <div class="dropzone"
         ondragover="event.preventDefault(); this.classList.add('over')"
         ondragleave="this.classList.remove('over')"
         ondrop="event.preventDefault(); this.classList.remove('over');
                 var id = event.dataTransfer.getData('text');
                 this.appendChild(document.getElementById(id));">
        📥 Drop Here
    </div>
</body>
</html>
```

---

## 8️⃣ WEB WORKERS & SERVICE WORKERS (Mention)

```html
<!-- Web Worker: Run JS in background thread (won't freeze UI) -->
<script>
    if (window.Worker) {
        const worker = new Worker('worker.js');
        worker.postMessage('Start heavy calculation');
        worker.onmessage = function(e) {
            console.log('Result:', e.data);
        };
    }
</script>

<!-- Service Worker: Offline support, push notifications, caching -->
<script>
    if ('serviceWorker' in navigator) {
        navigator.serviceWorker.register('/sw.js')
            .then(reg => console.log('SW registered'))
            .catch(err => console.log('SW failed', err));
    }
</script>
```

---

## 9️⃣ PWA (Progressive Web App) HTML Setup

```html
<head>
    <!-- Web App Manifest -->
    <link rel="manifest" href="/manifest.json">
    
    <!-- Theme Color -->
    <meta name="theme-color" content="#007bff">
    
    <!-- Apple-specific -->
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="apple-mobile-web-app-title" content="MyApp">
    <link rel="apple-touch-icon" href="/icon-192.png">
    
    <!-- Microsoft-specific -->
    <meta name="msapplication-TileColor" content="#007bff">
</head>
```

### manifest.json
```json
{
    "name": "My Progressive Web App",
    "short_name": "MyApp",
    "start_url": "/",
    "display": "standalone",
    "background_color": "#ffffff",
    "theme_color": "#007bff",
    "icons": [
        { "src": "/icon-192.png", "sizes": "192x192", "type": "image/png" },
        { "src": "/icon-512.png", "sizes": "512x512", "type": "image/png" }
    ]
}
```

---

## 🔟 MICRODATA & STRUCTURED DATA

```html
<!-- Microdata (inline) -->
<div itemscope itemtype="https://schema.org/Person">
    <h2 itemprop="name">John Doe</h2>
    <p itemprop="jobTitle">Web Developer</p>
    <a itemprop="email" href="mailto:john@example.com">john@example.com</a>
    <p itemprop="address" itemscope itemtype="https://schema.org/PostalAddress">
        <span itemprop="addressLocality">San Francisco</span>,
        <span itemprop="addressRegion">CA</span>
    </p>
</div>

<!-- JSON-LD (recommended by Google) -->
<script type="application/ld+json">
{
    "@context": "https://schema.org",
    "@type": "Article",
    "headline": "Complete HTML Guide",
    "author": { "@type": "Person", "name": "Your Name" },
    "datePublished": "2025-01-15",
    "description": "Learn HTML from zero to advanced"
}
</script>
```

---

## 1️⃣1️⃣ CONTENT SECURITY POLICY

```html
<!-- Restrict where resources can load from -->
<meta http-equiv="Content-Security-Policy" 
      content="default-src 'self'; 
               img-src 'self' https://cdn.example.com; 
               script-src 'self' 'nonce-abc123';
               style-src 'self' 'unsafe-inline';">

<!-- Nonce-based script loading -->
<script nonce="abc123">
    console.log('This script is allowed by CSP');
</script>
```

---

## 1️⃣2️⃣ PRINT STYLES IN HTML

```html
<head>
    <!-- Print-specific stylesheet -->
    <link rel="stylesheet" href="print.css" media="print">
    
    <!-- OR inline -->
    <style>
        @media print {
            /* Hide navigation, ads, buttons */
            nav, .sidebar, .ads, button, .no-print { display: none !important; }
            
            /* Remove backgrounds, use black text */
            body { background: white; color: black; font-size: 12pt; }
            
            /* Show URLs after links */
            a[href]::after { content: " (" attr(href) ")"; font-size: 0.8em; }
            
            /* Avoid page breaks inside elements */
            article, section { page-break-inside: avoid; }
            
            /* Always start new page */
            h1 { page-break-before: always; }
        }
    </style>
</head>

<!-- Print button -->
<button class="no-print" onclick="window.print()">🖨️ Print Page</button>
```

---

## 1️⃣3️⃣ COMMON HTML MISTAKES & FIXES

### Mistake 1: Missing DOCTYPE
```html
<!-- ❌ Browser enters "quirks mode" — inconsistent rendering -->
<html>
<body>...</body>
</html>

<!-- ✅ Always include DOCTYPE -->
<!DOCTYPE html>
<html lang="en">
<body>...</body>
</html>
```

### Mistake 2: Using `<br>` for spacing
```html
<!-- ❌ Wrong way to add space -->
<p>Paragraph 1</p>
<br><br><br>
<p>Paragraph 2</p>

<!-- ✅ Use CSS margin/padding -->
<p style="margin-bottom: 30px;">Paragraph 1</p>
<p>Paragraph 2</p>
```

### Mistake 3: Using tables for layout
```html
<!-- ❌ Tables are for DATA, not layout -->
<table>
    <tr>
        <td>Navigation</td>
        <td>Main Content</td>
        <td>Sidebar</td>
    </tr>
</table>

<!-- ✅ Use semantic HTML + CSS -->
<nav>Navigation</nav>
<main>Main Content</main>
<aside>Sidebar</aside>
```

### Mistake 4: Inline styles everywhere
```html
<!-- ❌ Hard to maintain -->
<p style="color: red; font-size: 16px; margin: 10px;">Text</p>

<!-- ✅ Use classes and CSS -->
<p class="error-text">Text</p>
<style>
    .error-text { color: red; font-size: 16px; margin: 10px; }
</style>
```

### Mistake 5: Missing form labels
```html
<!-- ❌ No label — bad for accessibility -->
Name: <input type="text" name="name">

<!-- ✅ Always use label -->
<label for="name">Name:</label>
<input type="text" name="name" id="name">
```

### Mistake 6: Wrong heading hierarchy
```html
<!-- ❌ Skipping levels -->
<h1>Title</h1>
<h4>Should be h2</h4>
<h6>Should be h3</h6>

<!-- ✅ Sequential hierarchy -->
<h1>Title</h1>
<h2>Section</h2>
<h3>Sub-section</h3>
```

### Mistake 7: Not specifying image dimensions
```html
<!-- ❌ Causes layout shift (CLS) -->
<img src="photo.jpg" alt="Photo">

<!-- ✅ Specify width and height -->
<img src="photo.jpg" alt="Photo" width="800" height="600">
```

---

# 📝 COMPLETE PRACTICE SECTION

---

## 🟢 LEVEL 1: ABSOLUTE BEGINNER TASKS (20 Tasks)

### Task 1: Hello World
Create your first HTML page that displays "Hello World" as a heading and your name as a paragraph.

```
Expected output:
- A large heading saying "Hello World"
- A paragraph with your name below it
```

### Task 2: Heading Hierarchy
Create a page showing all 6 heading levels with the text "Heading Level X" where X is the level number.

### Task 3: About Me Page
Create a page with:
- Your name as h1
- A paragraph about yourself
- Your hobbies in a paragraph
- A horizontal rule between sections

### Task 4: Text Formatting Showcase
Create a page demonstrating ALL text formatting tags:
- Bold, Italic, Underline, Strikethrough
- Strong, Emphasis, Mark, Small
- Subscript (H₂O) and Superscript (x²)

### Task 5: Simple Navigation Links
Create a page with 5 links:
- One to Google (opens in new tab)
- One to an email address
- One to a phone number
- One to another HTML file (about.html)
- One to a section on the same page

### Task 6: Image Gallery
Create a page with 3-5 images displayed vertically. Each image must have:
- `src`, `alt`, `width`, `height` attributes
- A title that shows on hover

### Task 7: Favorite Things Lists
Create a page with:
- An unordered list of 5 favorite foods
- An ordered list of 5 favorite movies (ranked)
- A description list of 3 vocabulary words with definitions

### Task 8: Simple Table
Create a table with your class schedule:
- 5 columns: Time, Monday, Tuesday, Wednesday, Thursday
- At least 4 rows of data
- Include thead and tbody

### Task 9: Basic Contact Form
Create a form with:
- Name (text input)
- Email (email input)
- Message (textarea)
- Submit button
- All inputs must have labels

### Task 10: Multi-Page Website
Create 3 HTML files that link to each other:
- index.html (Home)
- about.html (About)
- contact.html (Contact)
- Each page should have navigation links to the other two

### Task 11: Poetry Page
Use `<pre>` tag to display a poem preserving its formatting. Add the author using `<cite>`.

### Task 12: Abbreviation Page
Create a page explaining 10 tech abbreviations using `<abbr>` tag (HTML, CSS, JS, API, URL, HTTP, DNS, FTP, SQL, DOM).

### Task 13: Address Card
Create a business card using `<address>`, `<strong>`, `<a>` tags showing name, title, email, phone, and physical address.

### Task 14: Blockquote Page
Create a page with 3 famous quotes using `<blockquote>` with `cite` attribute and `<cite>` for the author.

### Task 15: Comments Practice
Take any of your previous pages and add meaningful HTML comments explaining each section.

### Task 16: Line Break Art
Use `<br>` and text/symbols to create simple ASCII art (like a house, tree, or smiley face).

### Task 17: Nested Lists
Create a nested list showing:
- Countries → States/Provinces → Cities (3 levels deep)

### Task 18: Special Characters Page
Create a page displaying 15+ HTML entities with their entity names and what they look like.

### Task 19: Favicon Setup
Add a favicon to any of your pages (use an emoji or simple icon).

### Task 20: Title & Meta Tags
Add proper `<title>`, `<meta description>`, `<meta charset>`, and `<meta viewport>` to all your pages.

---

## 🟡 LEVEL 2: INTERMEDIATE TASKS (20 Tasks)

### Task 21: Complete Registration Form
Build a registration form with ALL these field types:
- Text, Email, Password, Tel, URL
- Date, Number, Range, Color
- Radio buttons (gender)
- Checkboxes (interests)
- Select dropdown with optgroups (country → grouped by continent)
- Textarea (bio)
- File upload (profile picture)
- Hidden field (user_id)
- Datalist (skills)
- Fieldset + Legend grouping
- Submit and Reset buttons
- All fields have proper labels and validation (required, minlength, pattern)

### Task 22: Complex Table
Create a school report card table with:
- Caption
- Column spanning (subject groups)
- Row spanning (semester grouping)
- thead, tbody, tfoot
- Footer showing total/average
- Proper scope attributes on th

### Task 23: Semantic Blog Page
Create a full blog post page using ONLY semantic tags (no `<div>` allowed):
- header (with nav)
- main containing article
- article with: header, multiple sections, figure+figcaption, footer
- aside (sidebar with related posts)
- footer

### Task 24: Video & Audio Player Page
Create a multimedia page with:
- A video player with multiple source formats, poster, controls, subtitles track
- An audio player with multiple source formats
- Proper fallback text for unsupported browsers

### Task 25: FAQ Accordion
Build an FAQ page with 10 questions using `<details>` and `<summary>` — styled with CSS. Use `name` attribute for exclusive accordion.

### Task 26: Responsive Image Gallery
Create an image gallery using `<picture>` element with different images for mobile/tablet/desktop. Use `loading="lazy"` on all images.

### Task 27: Data Attributes Page
Create a product catalog where each product card uses data attributes:
- `data-product-id`, `data-price`, `data-category`, `data-rating`
- Use JavaScript to filter products by category
- Use CSS attribute selectors to style based on data values

### Task 28: Iframe Embed Page
Create a page that embeds:
- A YouTube video via iframe
- A Google Map via iframe
- Another HTML page via iframe
- Add proper title, loading="lazy", and sandbox attributes

### Task 29: Print-Friendly Page
Create a page that looks great on screen AND when printed:
- Hide navigation and buttons in print
- Show link URLs in print
- Use proper page break rules

### Task 30: Image Map
Create an interactive image map of a floor plan or world map with at least 5 clickable areas of different shapes (rect, circle, poly).

### Task 31: Multi-Step Form
Create a 3-step form using fieldsets:
- Step 1: Personal Info
- Step 2: Account Details
- Step 3: Preferences
- Each step is a separate fieldset

### Task 32: Table with Sorting
Create a data table with at least 10 rows. Add data attributes for values and a JavaScript sort function.

### Task 33: CSS Integration Practice
Create ONE page demonstrating all 3 ways of adding CSS:
- External stylesheet (link)
- Internal stylesheet (style tag)
- Inline styles (style attribute)
Show how specificity works.

### Task 34: SEO Optimized Page
Create a page with COMPLETE SEO setup:
- All meta tags (description, robots, canonical)
- Open Graph tags
- Twitter Card tags
- Structured data (JSON-LD)
- Semantic headings hierarchy
- Descriptive title
- Alt text on all images

### Task 35: Accessibility Audit Page
Create a page and make it 100% accessible:
- Skip navigation link
- ARIA labels on interactive elements
- Proper heading hierarchy
- All images have alt text
- All forms have labels
- Focus indicators visible
- Color is not the only indicator
- Keyboard navigable

### Task 36: Entity Art Page
Create a decorative page using ONLY HTML entities and special characters — no images. Make patterns, borders, and designs.

### Task 37: Resume/CV
Create a printable resume using semantic HTML:
- Structured with sections
- Education timeline
- Skills with progress bars (using `<progress>` or `<meter>`)
- Contact links (email, phone, LinkedIn)
- Print button

### Task 38: Product Comparison Table
Create a feature comparison table for 3 products with:
- Checkmarks (✓) and crosses (✗) using entities
- Column highlighting
- Footer with pricing
- Colspan for category headers

### Task 39: Form Validation
Create a form that uses HTML5 built-in validation:
- required fields
- min/max length
- email validation
- URL validation
- pattern (regex for phone number)
- Custom validation messages using CSS :valid/:invalid

### Task 40: Navigation Patterns
Create a page demonstrating 4 types of navigation:
- Top horizontal nav bar
- Side vertical nav
- Breadcrumb navigation
- Footer navigation
Each with proper `<nav>` and `aria-label`.

---

## 🔴 LEVEL 3: ADVANCED TASKS (15 Tasks)

### Task 41: Complete Portfolio Website (Multi-page)
Build a 5-page portfolio website:
- Home (hero section, intro, skills)
- About (bio, education, experience timeline)
- Projects (grid of project cards with images)
- Blog (list of blog post previews)
- Contact (complete form)
- Shared navigation on all pages
- All semantic HTML
- Fully accessible
- SEO optimized
- Print-friendly

### Task 42: Dashboard Layout
Create a data dashboard page with:
- Header with logo and user info
- Sidebar navigation
- Main content area with cards/widgets
- Canvas or SVG charts
- Data tables with stats
- Progress indicators

### Task 43: Web Component
Create a custom HTML element using Web Components:
- Template with slots
- Shadow DOM for encapsulation
- Custom element class
- Make it reusable across pages

### Task 44: SVG Artwork
Create a page with hand-coded SVG graphics:
- At least 5 different shapes
- Gradients and patterns
- Animated SVG elements
- Interactive (hover effects)

### Task 45: Canvas Drawing App
Create a simple drawing application using `<canvas>`:
- Color picker (using `<input type="color">`)
- Brush size slider (using `<input type="range">`)
- Clear button
- Mouse event handling for drawing

### Task 46: Drag and Drop Task Manager
Build a Kanban-style task board with 3 columns:
- To Do, In Progress, Done
- Cards that can be dragged between columns
- Use HTML5 Drag and Drop API

### Task 47: Offline-Ready Page
Create a page that works offline:
- Web App Manifest
- Service Worker registration
- Proper meta tags for PWA
- Add to Home Screen support

### Task 48: Geolocation Map
Create a page that:
- Gets user's location via Geolocation API
- Displays coordinates
- Embeds a map showing the location

### Task 49: Local Storage Notes App
Build a notes app that:
- Uses `contenteditable` for editing
- Saves notes to localStorage
- Persists across page reloads
- Has delete functionality

### Task 50: Content Security Policy
Create a page with a strict CSP meta tag. Test that:
- Inline scripts are blocked
- External scripts from unauthorized domains are blocked
- Only whitelisted resources load

### Task 51: Dialog & Popover
Create a page demonstrating:
- Native `<dialog>` modal (showModal)
- Popover API (auto and manual)
- Form inside dialog with method="dialog"
- Backdrop styling

### Task 52: Structured Data
Add complete Schema.org structured data to a:
- Blog article page (Article schema)
- Product page (Product schema)
- FAQ page (FAQPage schema)
- Validate with Google Rich Results Test

### Task 53: Performance Optimized Page
Create a page that scores 95+ on Lighthouse:
- Preconnect to external domains
- Preload critical resources
- Lazy load all images
- Use fetchpriority
- Defer non-critical JS
- Use modern image formats (WebP/AVIF)
- Specify all image dimensions

### Task 54: Accessible Form with ARIA
Create a complex form that is fully accessible:
- ARIA labels and descriptions
- Error messages linked with aria-describedby
- Live region for form status updates
- Proper focus management
- Works 100% with keyboard only

### Task 55: Complete Email Template
Create an HTML email template (tables-based layout since emails don't support modern CSS):
- Header with logo
- Content section with images
- CTA button
- Footer with unsubscribe link
- All inline styles (email requirement)

---

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

## 🟡 INTERMEDIATE QUESTIONS (30 Questions)

**Q51.** What is the difference between `<section>`, `<article>`, and `<div>`?
> **A:** `<section>` = thematic grouping with a heading. `<article>` = self-contained, independently distributable content. `<div>` = no semantic meaning, just grouping.

**Q52.** When should you use `<figure>` and `<figcaption>`?
> **A:** When content (image, diagram, code block) is self-contained and referenced from the main content. `<figcaption>` provides its caption.

**Q53.** What's the difference between `<details>` and a JavaScript accordion?
> **A:** `<details>` is native HTML — works without JS, is accessible by default, semantic. JS accordion requires custom code for accessibility and functionality.

**Q54.** Explain the difference between `<del>` and `<s>`.
> **A:** `<del>` represents content that was deleted/edited (has `cite` and `datetime` attributes). `<s>` represents content no longer relevant but not a document edit.

**Q55.** What is the `enctype` attribute on forms?
> **A:** Specifies how form data is encoded. `application/x-www-form-urlencoded` (default), `multipart/form-data` (for file uploads), `text/plain` (debugging).

**Q56.** How do radio buttons work in groups?
> **A:** All radio buttons with the same `name` attribute form a group — only one can be selected at a time.

**Q57.** What is a `<datalist>` and how does it differ from `<select>`?
> **A:** `<datalist>` provides autocomplete suggestions but users can type any value. `<select>` restricts users to only the predefined options.

**Q58.** What is `contenteditable`?
> **A:** A global attribute that makes any HTML element editable directly in the browser by the user. Example: `<div contenteditable="true">Edit me</div>`

**Q59.** What are `data-*` attributes?
> **A:** Custom attributes for storing extra data on HTML elements. Accessed via JavaScript's `element.dataset` property. Example: `data-user-id="42"` → `dataset.userId`

**Q60.** What is the `<output>` element?
> **A:** Represents the result of a calculation or user action. Used with forms: `<output name="result" for="a b">30</output>`

**Q61.** Explain `colspan` and `rowspan`.
> **A:** `colspan` makes a cell span multiple columns horizontally. `rowspan` makes a cell span multiple rows vertically.

**Q62.** What's the difference between `<meter>` and `<progress>`?
> **A:** `<progress>` shows completion of a task (loading bar). `<meter>` shows a scalar measurement within a known range (disk usage, fuel gauge).

**Q63.** What is the `scope` attribute on `<th>`?
> **A:** Specifies whether a header cell relates to a `col` (column), `row`, `colgroup`, or `rowgroup`. Improves table accessibility for screen readers.

**Q64.** How does the `<picture>` element work?
> **A:** Contains multiple `<source>` elements with different images for different conditions (screen size, format). Browser picks the first matching source. `<img>` inside acts as fallback.

**Q65.** What is `srcset` on images?
> **A:** Lets the browser choose the best image size based on device screen width/pixel density. Example: `srcset="small.jpg 400w, large.jpg 800w"`

**Q66.** What is the `<template>` element?
> **A:** Holds HTML that is NOT rendered on page load. Content is invisible and inert until cloned via JavaScript. Used as a blueprint for dynamic content.

**Q67.** What is the purpose of `<wbr>`?
> **A:** Word Break Opportunity — suggests where a browser MAY break a long word or URL if needed for wrapping. Doesn't force a break.

**Q68.** What are ARIA roles and when should you use them?
> **A:** ARIA (Accessible Rich Internet Applications) roles provide semantic meaning to elements for screen readers. Use them when HTML semantic tags aren't sufficient.

**Q69.** Explain `defer` vs `async` on `<script>`.
> **A:** `defer` downloads in parallel, executes AFTER HTML parsing, maintains order. `async` downloads in parallel, executes IMMEDIATELY when ready, no guaranteed order.

**Q70.** What is the `<dialog>` element?
> **A:** Native HTML modal/popup. Use `.showModal()` to open as modal, `.show()` as non-modal. Supports backdrop styling, form method="dialog" for closing.

**Q71.** What is the Popover API?
> **A:** Native HTML feature for creating popovers without JavaScript. Use `popover` attribute on target and `popovertarget` on the trigger button.

**Q72.** What's the difference between absolute and relative URLs?
> **A:** Absolute = full path (`https://example.com/page.html`). Relative = path relative to current file (`../images/photo.jpg`).

**Q73.** What is the `sandbox` attribute on `<iframe>`?
> **A:** Restricts iframe capabilities for security. Empty = maximum restrictions. Add values to allow specific features: `allow-scripts`, `allow-same-origin`, `allow-forms`.

**Q74.** How do you make a form field read-only vs disabled?
> **A:** `readonly` — can't edit but value IS submitted. `disabled` — can't edit and value is NOT submitted.

**Q75.** What is `inputmode`?
> **A:** Hints to mobile browsers which virtual keyboard to show. Values: `numeric`, `tel`, `email`, `url`, `search`, `decimal`, `none`.

**Q76.** What is the `<search>` element?
> **A:** New semantic element (2023) that wraps search functionality. Replaces `<div role="search">`.

**Q77.** What is the `inert` attribute?
> **A:** Makes an element and all its children completely non-interactive — can't click, focus, or select anything inside.

**Q78.** What is `fetchpriority`?
> **A:** Hints to the browser about the priority of a resource fetch. Values: `high`, `low`, `auto`. Use `high` for hero images, `low` for below-fold content.

**Q79.** How do you prevent layout shift with images?
> **A:** Always specify `width` and `height` attributes on `<img>` tags. This lets the browser reserve space before the image loads.

**Q80.** What is JSON-LD structured data?
> **A:** A script block (`type="application/ld+json"`) containing Schema.org structured data in JSON format. Helps search engines understand page content for rich results.

---

## 🔴 ADVANCED QUESTIONS (20 Questions)

**Q81.** Explain the difference between HTML5 semantic elements and ARIA roles. When would you use ARIA over semantic HTML?
> **A:** Semantic elements have built-in accessibility. ARIA is for cases where HTML doesn't have a suitable element or for dynamic content (custom widgets, live regions, state changes). Rule: use semantic HTML first, ARIA only when needed.

**Q82.** What is Shadow DOM and how does it relate to HTML?
> **A:** Shadow DOM encapsulates a component's HTML and CSS so it's isolated from the main document. Used with Web Components via `element.attachShadow()`.

**Q83.** Explain the Content Security Policy and how it's set via HTML.
> **A:** CSP restricts which resources (scripts, styles, images) can load. Set via `<meta http-equiv="Content-Security-Policy" content="...">` or HTTP headers.

**Q84.** What are Speculation Rules and how do they improve performance?
> **A:** A `<script type="speculationrules">` block that tells the browser to prerender or prefetch specific pages the user is likely to visit next.

**Q85.** How does the View Transitions API work with HTML?
> **A:** CSS `@view-transition { navigation: auto; }` enables animated transitions between page navigations. Elements can be named with `view-transition-name` for matched animations.

**Q86.** What is the difference between `preload`, `prefetch`, `preconnect`, and `prerender`?
> **A:** `preload` = current page critical resource. `prefetch` = next page resource (low priority). `preconnect` = establish connection to external domain. `prerender` = fully render a page in background.

**Q87.** Explain microdata vs JSON-LD vs RDFa for structured data.
> **A:** Microdata = inline attributes (`itemscope`, `itemprop`). JSON-LD = separate script block (Google's recommendation). RDFa = inline attributes (more complex). JSON-LD is preferred.

**Q88.** How do custom elements work? Show the lifecycle callbacks.
> **A:** Extend `HTMLElement`, define with `customElements.define()`. Callbacks: `connectedCallback()`, `disconnectedCallback()`, `attributeChangedCallback()`, `adoptedCallback()`.

**Q89.** What is the `blocking="render"` attribute?
> **A:** Tells the browser to not render ANY content until the specified resource is loaded. Used for critical CSS/JS that must be available before first paint.

**Q90.** How does the `<slot>` element work in Web Components?
> **A:** `<slot>` is a placeholder in Shadow DOM where external (light DOM) content is projected. Named slots (`<slot name="title">`) allow multiple insertion points.

**Q91.** What is the difference between `loading="lazy"` and Intersection Observer?
> **A:** `loading="lazy"` is native HTML attribute for deferred loading. Intersection Observer is a JavaScript API that gives more control over when elements become visible. Native lazy loading is simpler; IO is more flexible.

**Q92.** How would you implement an accessible modal dialog?
> **A:** Use `<dialog>` with `showModal()`. Trap focus inside. Close on Escape. Return focus to trigger on close. Use `aria-labelledby` for title. Backdrop prevents background interaction.

**Q93.** What is the `<base>` tag and what are its risks?
> **A:** Sets base URL for all relative links. Risk: affects ALL relative URLs on the page including anchors, form actions, and CSS paths. Can cause unexpected behavior.

**Q94.** How do you make an HTML email? Why can't you use modern CSS?
> **A:** Use table-based layouts with inline styles. Email clients strip `<head>` styles, don't support flexbox/grid, and have inconsistent CSS support. Test with Litmus/Email on Acid.

**Q95.** Explain the importance of the `lang` attribute.
> **A:** Tells browsers and screen readers the language. Affects text-to-speech pronunciation, spell checking, translation tools, search engine language detection, and hyphenation.

**Q96.** What is the `nonce` attribute used for?
> **A:** A one-time-use token for Content Security Policy. Allows specific inline scripts/styles to execute while blocking all others. Must be unique per page load.

**Q97.** How does the `translate` attribute work?
> **A:** `translate="no"` tells translation tools (Google Translate) to skip that element. Useful for brand names, code, and identifiers.

**Q98.** What is the `enterkeyhint` attribute?
> **A:** Changes the label on the Enter/Return key on mobile virtual keyboards. Values: `enter`, `done`, `go`, `next`, `previous`, `search`, `send`.

**Q99.** Explain how the exclusive accordion works with `<details name="...">`
> **A:** All `<details>` elements with the same `name` attribute form a group where only one can be open at a time. Opening one automatically closes others.

**Q100.** What will HTML look like in the future?
> **A:** HTML is now a Living Standard (continuous updates). Key trends: more native interactive elements (popover, dialog), declarative JS-free interactions (invoker commands), better form customization (customizable select), enhanced security features, and deeper integration with CSS (anchor positioning, scroll-driven animations).

---

## 🎯 TRUE/FALSE QUIZ (25 Questions)

| # | Statement | Answer |
|---|-----------|--------|
| 1 | HTML is a programming language | ❌ FALSE — It's a markup language |
| 2 | `<br>` needs a closing tag | ❌ FALSE — It's a void/self-closing element |
| 3 | You should use only one `<h1>` per page | ✅ TRUE — For SEO |
| 4 | `<strong>` and `<b>` are exactly the same | ❌ FALSE — `<strong>` has semantic meaning |
| 5 | The `<head>` section is visible on the page | ❌ FALSE — Only metadata, not visible |
| 6 | `<main>` can be used multiple times per page | ❌ FALSE — Only ONE `<main>` per page |
| 7 | `alt` attribute on images is optional | ❌ FALSE — Required for accessibility/SEO |
| 8 | `<table>` should be used for page layout | ❌ FALSE — Tables are for tabular data only |
| 9 | HTML5 is the final version of HTML | ❌ FALSE — It's now a Living Standard |
| 10 | `<div>` is a semantic element | ❌ FALSE — It has no semantic meaning |
| 11 | All form inputs should have labels | ✅ TRUE — For accessibility |
| 12 | `<em>` renders text in italic | ✅ TRUE — But its purpose is emphasis |
| 13 | HTML ignores extra whitespace | ✅ TRUE — Multiple spaces collapse to one |
| 14 | `<article>` must contain a heading | ✅ TRUE (recommended) — Should have heading |
| 15 | `defer` and `async` do the same thing | ❌ FALSE — Different loading strategies |
| 16 | `<!DOCTYPE html>` is an HTML tag | ❌ FALSE — It's a declaration/instruction |
| 17 | You can nest `<a>` tags inside each other | ❌ FALSE — Interactive elements can't be nested |
| 18 | `<header>` can only be used once per page | ❌ FALSE — Can be used multiple times |
| 19 | `loading="lazy"` improves page performance | ✅ TRUE — Defers loading off-screen images |
| 20 | `<span>` is a block-level element | ❌ FALSE — It's inline |
| 21 | UTF-8 supports emojis | ✅ TRUE |
| 22 | `<select>` allows custom text input | ❌ FALSE — Only predefined options (use `<datalist>` for custom) |
| 23 | `<details>` requires JavaScript to work | ❌ FALSE — Pure HTML, no JS needed |
| 24 | `<dialog>` is supported in all modern browsers | ✅ TRUE (since 2022) |
| 25 | `id` attribute values can be reused on a page | ❌ FALSE — Must be unique |

---

## 🧩 FILL IN THE BLANKS (15 Questions)

1. HTML stands for ________ ________ ________ ________
> HyperText Markup Language

2. The ________ tag is the root element of an HTML document.
> `<html>`

3. To add an image, use the ________ tag with ________ and ________ attributes.
> `<img>` with `src` and `alt`

4. The ________ attribute on a form specifies the HTTP method (GET or POST).
> `method`

5. ________ elements take full width and start on a new line.
> Block

6. ________ elements take only the space they need and stay in line.
> Inline

7. The ________ tag creates a dropdown selection list.
> `<select>`

8. To group related form fields, use ________ with ________ for the caption.
> `<fieldset>` with `<legend>`

9. The ________ meta tag is essential for responsive design on mobile devices.
> `viewport`

10. ________ tags describe the purpose of content, while ________ tags only describe appearance.
> Semantic; Physical (or non-semantic)

11. The ________ attribute on `<ol>` makes the list count backwards.
> `reversed`

12. To lazy load an image, add ________="________" attribute.
> `loading`=`"lazy"`

13. The ________ tag provides autocomplete suggestions for an input field.
> `<datalist>`

14. ________ are special codes starting with & and ending with ; to display reserved characters.
> HTML entities

15. The ________ element is used to create native modal dialogs without JavaScript libraries.
> `<dialog>`

---

## 🏆 CODING CHALLENGES (10 Challenges)

### Challenge 1: Build this layout using ONLY HTML
```
┌──────────────────────────────┐
│          LOGO    NAV LINKS   │ ← header
├────────────────────┬─────────┤
│                    │         │
│   MAIN CONTENT     │ SIDEBAR │
│   - Article 1      │ - Ad    │
│   - Article 2      │ - Links │
│                    │         │
├────────────────────┴─────────┤
│     FOOTER WITH LINKS        │ ← footer
└──────────────────────────────┘
```
Requirements: Use only semantic tags. No `<div>` allowed.

### Challenge 2: Create a form that collects ALL possible data types
Must include: text, email, password, number, date, time, color, range, file, radio, checkbox, select, datalist, textarea, hidden, search, tel, url, month, week, datetime-local.

### Challenge 3: Build a comparison table
Create a feature comparison table for 3 smartphones with:
- At least 8 features
- Use colspan for category groupings
- Use entities for ✓ and ✗
- Include a price row in tfoot

### Challenge 4: Accessible Navigation
Create a navigation that:
- Has skip link
- Uses `<nav>` with aria-label
- Highlights current page with `aria-current`
- Is fully keyboard navigable
- Has proper focus styles

### Challenge 5: SEO Perfect Page
Create a blog post page with ALL SEO elements:
- Title, meta description, canonical
- Open Graph tags (5+)
- Structured data (JSON-LD)
- Semantic headings
- Alt text on all images
- Internal and external links

### Challenge 6: Multi-format Media Player
Create a page with:
- Video with 3 source formats + subtitles track + poster
- Audio with 3 source formats
- Responsive YouTube embed
- All with proper fallback text

### Challenge 7: Interactive FAQ (Pure HTML)
Create 15 questions using `<details>` with:
- Exclusive accordion groups (by category)
- Search filter (hint: use `<input>` with JS)
- Categories separated by headings

### Challenge 8: Complete Email Template
Build an HTML email template using only tables and inline styles:
- Header with logo
- Hero section with image
- 2-column content area
- CTA button
- Footer with social icons and unsubscribe

### Challenge 9: Print-Optimized Resume
Create a resume that:
- Looks great on screen
- Prints beautifully (hide non-essential elements)
- Uses `@media print` styles
- Has a print button that hides in print

### Challenge 10: Progressive Web App Setup
Create a page with complete PWA setup:
- manifest.json
- Service worker registration
- All required meta tags
- Proper icons
- Theme color
- Offline fallback page

---

## 📊 MATCHING EXERCISE

Match the tag to its purpose:

| # | Tag | | Purpose |
|---|-----|-|---------|
| 1 | `<nav>` | | A. Self-contained distributable content |
| 2 | `<article>` | | B. Side content/sidebar |
| 3 | `<aside>` | | C. Main navigation links |
| 4 | `<figure>` | | D. Expandable/collapsible content |
| 5 | `<details>` | | E. Self-contained media with caption |
| 6 | `<time>` | | F. Definition of a term |
| 7 | `<dfn>` | | G. Machine-readable date/time |
| 8 | `<mark>` | | H. Keyboard input representation |
| 9 | `<kbd>` | | I. Highlighted/marked text |
| 10 | `<dialog>` | | J. Native modal popup |

**Answers:** 1-C, 2-A, 3-B, 4-E, 5-D, 6-G, 7-F, 8-I, 9-H, 10-J

---

## 🔍 SPOT THE ERROR (10 Exercises)

### Error 1:
```html
<h1>Title<h1>
<p>Paragraph<p>
```
> **Error:** Missing forward slashes in closing tags. Should be `</h1>` and `</p>`.

### Error 2:
```html
<ul>
    <p>Item 1</p>
    <p>Item 2</p>
</ul>
```
> **Error:** `<ul>` can only contain `<li>` children, not `<p>`. Use `<li>` tags.

### Error 3:
```html
<img src="photo.jpg" width="300" height="200">
```
> **Error:** Missing required `alt` attribute.

### Error 4:
```html
<a href="page.html">
    <a href="other.html">Nested Link</a>
</a>
```
> **Error:** Cannot nest interactive elements (`<a>` inside `<a>`).

### Error 5:
```html
<label>Name</label>
<input type="text" id="name">
```
> **Error:** Label missing `for` attribute to connect it to the input. Add `for="name"`.

### Error 6:
```html
<table>
    <td>Cell 1</td>
    <td>Cell 2</td>
</table>
```
> **Error:** Missing `<tr>` (table row). `<td>` must be inside `<tr>`.

### Error 7:
```html
<form method="post" action="/upload">
    <input type="file" name="doc">
    <button type="submit">Upload</button>
</form>
```
> **Error:** Missing `enctype="multipart/form-data"` (required for file uploads).

### Error 8:
```html
<div id="header">...</div>
<div id="header">...</div>
```
> **Error:** Duplicate `id` values. IDs must be unique on a page.

### Error 9:
```html
<span>
    <h2>Heading</h2>
    <p>Paragraph</p>
</span>
```
> **Error:** Block elements (`<h2>`, `<p>`) inside an inline element (`<span>`). Use `<div>` instead.

### Error 10:
```html
<input type=text name=user placeholder=Enter name>
```
> **Error:** While technically valid in HTML5, attribute values with spaces MUST be quoted. `placeholder` value would be truncated to just "Enter". Use quotes: `placeholder="Enter name"`.

---

# 🏁 FINAL CHECKLIST — EVERYTHING COVERED

```
✅ What is HTML (definition, history, creator)
✅ HTML Document (file extension, structure)
✅ Tags (what they are, open vs close/void)
✅ Elements (start tag + content + end tag)
✅ Attributes (definition, global attributes, event attributes)
✅ DOCTYPE declaration
✅ html, head, title, body tags
✅ Meta tags (charset, viewport, description, robots)
✅ Heading tags (h1-h6, hierarchy rules)
✅ Paragraph tag
✅ Line break (br) and Horizontal rule (hr)
✅ Text Formatting — Physical tags (b, i, u, s, big, small, sup, sub)
✅ Text Formatting — Logical tags (strong, em, mark, code, cite, time, 
   address, blockquote, pre, abbr, del, ins, dfn, kbd, samp, var, q)
✅ Links/Anchor tag (href, target, download, title, all link types)
✅ Images (src, alt, width, height, loading, title, responsive)
✅ Image as link
✅ Image maps (map, area, shapes)
✅ Lists (ul, ol, dl, li, dt, dd, nested, type attribute)
✅ Tables (table, thead, tbody, tfoot, tr, th, td, caption, 
   colspan, rowspan, scope, colgroup, col)
✅ Forms (form, action, method, enctype, name)
✅ All Input Types (text, password, email, tel, search, url, number, 
   range, date, time, datetime-local, month, week, radio, checkbox, 
   color, file, hidden, submit, reset, button, image)
✅ Form Elements (textarea, select, option, optgroup, datalist, 
   button, label, fieldset, legend, output, progress, meter)
✅ Input Attributes (required, readonly, disabled, placeholder, 
   autofocus, autocomplete, pattern, min, max, minlength, maxlength, 
   step, multiple, accept, value, checked, form, list)
✅ Semantic Elements (header, nav, main, article, section, aside, 
   footer, figure, figcaption, details, summary, dialog, search, 
   time, mark, address, hgroup, menu)
✅ Non-Semantic Elements (div, span)
✅ Block vs Inline elements
✅ HTML Layout structure
✅ Multimedia — Video (video, source, track, all attributes)
✅ Multimedia — Audio (audio, source, all attributes)
✅ Iframes (src, width, height, sandbox, loading)
✅ Embed and Object tags
✅ HTML Entities & Special Characters
✅ Adding CSS (external, internal, inline)
✅ Adding JavaScript (inline, external, defer, async, module)
✅ HTML Comments
✅ Preformatted text (pre, code, kbd, samp, var)
✅ URL Types (absolute, relative, protocol-relative)
✅ File Paths (relative navigation)
✅ Responsive Web Design (viewport, srcset, picture)
✅ HTML vs XHTML
✅ Character Encoding (UTF-8)
✅ HTML Validation (common errors, tools)
✅ Global Attributes (complete list)
✅ Event Attributes (mouse, keyboard, form, window)
✅ SEO (title, description, canonical, OG, Twitter, structured data)
✅ Open Graph & Social Media meta tags
✅ Favicons (all formats)
✅ Accessibility (ARIA, roles, labels, checklist)
✅ Alt text best practices
✅ Canvas (2D context, shapes, text)
✅ SVG (shapes, text, animation)
✅ SVG vs Canvas comparison
✅ Data Attributes (data-*, dataset, CSS selectors)
✅ Web Components (template, slot, shadow DOM, custom elements)
✅ Drag and Drop (HTML5 API)
✅ Geolocation API
✅ Web Storage (localStorage, sessionStorage)
✅ Content Editable
✅ Dialog element (showModal, method="dialog")
✅ Popover API (popover, popovertarget)
✅ Search element
✅ Inert attribute
✅ Fetchpriority
✅ Lazy loading (native)
✅ Web Workers & Service Workers
✅ PWA setup (manifest, meta tags)
✅ Microdata & JSON-LD structured data
✅ Content Security Policy
✅ Print styles
✅ Script loading strategies (defer, async, module)
✅ Performance optimization (preload, preconnect, prefetch)
✅ Speculation Rules API
✅ View Transitions API
✅ Common mistakes & fixes
✅ Deprecated tags list
✅ All 110+ HTML tags with theory + code
✅ Complete projects (5 projects)
✅ 55 Practice Tasks (beginner to advanced)
✅ 100 Questions (theory + code + quiz)
✅ True/False quiz (25 questions)
✅ Fill in the blanks (15 questions)
✅ Matching exercise (10 items)
✅ Spot the Error (10 exercises)
✅ Coding Challenges (10 challenges)
✅ 2024-2025 Trends & New Features
✅ Learning Path roadmap
```

---

> 🎯 **This guide now covers EVERYTHING in HTML — from the absolute basics to the cutting edge. Complete the tasks in order, answer all questions, and you'll have mastered HTML completely.**

*Total Coverage: 110+ tags × Theory + Code + Practice = Complete HTML Mastery* 🚀