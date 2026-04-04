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

