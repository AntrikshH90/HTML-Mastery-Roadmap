# 🆈 PART Y: ACCESSIBILITY (a11y)

## ARIA Attributes

```html
<!-- Landmarks -->
<nav role="navigation" aria-label="Main Menu">...</nav>

<!-- Labels for screen readers -->
<button aria-label="Close dialog">✕</button>

<!-- Live regions (announce dynamic changes) -->
<div aria-live="polite" id="status">Ready</div>

<!-- Hidden from screen readers (decorative) -->
<span aria-hidden="true">🎨</span>

<!-- Skip navigation -->
<a href="#main-content" class="skip-link">Skip to main content</a>

<!-- Current page in navigation -->
<a href="/" aria-current="page">Home</a>
```

## Accessibility Checklist

```
✅ All images have descriptive alt text
✅ All form inputs have labels
✅ Color is NOT the only way to convey information
✅ Sufficient color contrast (4.5:1 for text)
✅ Page navigable with keyboard only
✅ Focus indicators are visible
✅ Heading hierarchy is logical (h1 → h2 → h3)
✅ Language declared (<html lang="en">)
✅ Page has descriptive <title>
✅ Links have descriptive text (not "click here")
✅ Media has captions/transcripts
```

---

