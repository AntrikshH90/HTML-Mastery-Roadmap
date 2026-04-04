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
