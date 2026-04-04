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

