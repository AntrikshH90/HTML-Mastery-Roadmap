# 🆆 PART W: IMAGE MAPS

## 📖 Theory (from PDF)

> An image map in HTML allows you to define **clickable areas (hotspots)** on an image that link to different destinations. You can create interactive images where different parts of the image lead to different URLs.

## Image Map Code (from PDF)

```html
<img src="image.jpg" alt="Image with map" usemap="#mapname">

<map name="mapname">
    <area shape="rect" coords="34,44,270,350" 
          href="https://example.com/page1" alt="Link 1">
    <area shape="circle" coords="337,300,44" 
          href="https://example.com/page2" alt="Link 2">
    <area shape="poly" coords="220,210,300,250,260,300" 
          href="https://example.com/page3" alt="Link 3">
</map>
```

### Shape Types:
| Shape | `coords` Format | Description |
|-------|----------------|-------------|
| `rect` | x1,y1,x2,y2 | Rectangle (top-left, bottom-right) |
| `circle` | x,y,radius | Circle (center x, center y, radius) |
| `poly` | x1,y1,x2,y2,... | Polygon (series of x,y points) |

---

