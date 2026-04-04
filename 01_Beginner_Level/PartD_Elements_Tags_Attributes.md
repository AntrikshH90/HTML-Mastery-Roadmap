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

