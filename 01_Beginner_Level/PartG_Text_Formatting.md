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

