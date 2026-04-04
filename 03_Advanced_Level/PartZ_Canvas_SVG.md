# 🆉 PART Z: GRAPHICS — CANVAS & SVG

## SVG

```html
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
    <circle cx="100" cy="100" r="80" fill="#007bff"/>
    <text x="100" y="108" text-anchor="middle" fill="white" font-size="20">SVG</text>
</svg>
```

## Canvas

```html
<canvas id="myCanvas" width="400" height="200"></canvas>
<script>
const ctx = document.getElementById('myCanvas').getContext('2d');
ctx.fillStyle = '#007bff';
ctx.fillRect(20, 20, 150, 100);
ctx.font = 'bold 20px Arial';
ctx.fillText('Hello Canvas!', 200, 80);
</script>
```

## SVG vs Canvas

| Feature | SVG | Canvas |
|---------|-----|--------|
| Type | Vector | Raster (pixels) |
| Scalability | Infinite | Pixelates on zoom |
| Best for | Icons, logos, charts | Games, image editing |
| Accessibility | Better (text readable) | Poor |

---
