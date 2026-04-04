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

