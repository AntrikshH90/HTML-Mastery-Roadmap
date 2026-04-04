# 🆇 PART X: HTML5 APIS & MODERN FEATURES

## Dialog Element (Native Modal)

```html
<dialog id="myDialog">
    <h2>Confirm Action</h2>
    <p>Are you sure?</p>
    <form method="dialog">
        <button value="cancel">Cancel</button>
        <button value="confirm">Confirm</button>
    </form>
</dialog>

<button onclick="myDialog.showModal()">Open Dialog</button>
```

## Popover API (NEW 2024!)

```html
<!-- No JavaScript needed! -->
<button popovertarget="mypopover">Toggle Popover</button>
<div id="mypopover" popover>
    <h3>Popover Content</h3>
    <p>Click outside to close.</p>
</div>
```

## Content Editable

```html
<div contenteditable="true" style="border: 1px solid #ccc; padding: 15px;">
    <h2>Click and edit this heading!</h2>
    <p>You can type here directly in the browser.</p>
</div>
```

## Web Storage

```html
<script>
// localStorage — persists even after browser closes
localStorage.setItem('username', 'John');
console.log(localStorage.getItem('username')); // "John"

// sessionStorage — cleared when tab closes
sessionStorage.setItem('tempData', 'Temporary');
</script>
```

## Geolocation API

```html
<button onclick="getLocation()">📍 Get My Location</button>
<p id="location"></p>

<script>
function getLocation() {
    if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition((pos) => {
            document.getElementById('location').innerHTML = 
                `Lat: ${pos.coords.latitude}, Lng: ${pos.coords.longitude}`;
        });
    }
}
</script>
```

## Search Element (NEW 2023!)

```html
<search>
    <form action="/search" method="GET">
        <input type="search" name="q" placeholder="Search...">
        <button type="submit">🔍</button>
    </form>
</search>
```

## Inert Attribute (NEW!)

```html
<!-- Makes entire section non-interactive -->
<div inert>
    <button>Can't click me</button>
    <input type="text" placeholder="Can't type here">
</div>
```

---

