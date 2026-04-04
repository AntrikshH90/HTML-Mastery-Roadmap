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

