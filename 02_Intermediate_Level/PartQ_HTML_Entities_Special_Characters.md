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

