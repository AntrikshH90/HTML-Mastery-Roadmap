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

