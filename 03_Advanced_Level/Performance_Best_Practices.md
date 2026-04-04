# ⚡ PERFORMANCE & BEST PRACTICES

```html
<!-- 1. Lazy load images below the fold -->
<img src="photo.jpg" alt="..." loading="lazy" decoding="async">

<!-- 2. Specify dimensions to prevent layout shift -->
<img src="photo.jpg" alt="..." width="800" height="600">

<!-- 3. Modern image formats with fallback -->
<picture>
    <source srcset="image.avif" type="image/avif">
    <source srcset="image.webp" type="image/webp">
    <img src="image.jpg" alt="..." loading="lazy">
</picture>

<!-- 4. Preconnect to external domains -->
<link rel="preconnect" href="https://fonts.googleapis.com">

<!-- 5. Defer non-critical JS -->
<script src="app.js" defer></script>

<!-- 6. Fetchpriority for critical resources -->
<img src="hero.jpg" alt="..." fetchpriority="high">
```

## Do's and Don'ts

```
✅ DO:
  • Use semantic HTML tags
  • Always include alt text
  • Use <label> for all form inputs
  • Validate HTML (validator.w3.org)
  • Use responsive images
  • Include lang attribute
  • Use meta viewport for mobile

❌ DON'T:
  • Use tables for layout
  • Skip heading levels
  • Use <br> for spacing (use CSS)
  • Use deprecated tags
  • Forget to close tags
  • Autoplay video with sound
  • Use div when semantic tag exists
```

---

