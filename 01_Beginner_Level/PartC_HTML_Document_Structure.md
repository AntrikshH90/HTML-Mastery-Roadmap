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

