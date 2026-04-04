## 🔍 SPOT THE ERROR (10 Exercises)

### Error 1:
```html
<h1>Title<h1>
<p>Paragraph<p>
```
> **Error:** Missing forward slashes in closing tags. Should be `</h1>` and `</p>`.

### Error 2:
```html
<ul>
    <p>Item 1</p>
    <p>Item 2</p>
</ul>
```
> **Error:** `<ul>` can only contain `<li>` children, not `<p>`. Use `<li>` tags.

### Error 3:
```html
<img src="photo.jpg" width="300" height="200">
```
> **Error:** Missing required `alt` attribute.

### Error 4:
```html
<a href="page.html">
    <a href="other.html">Nested Link</a>
</a>
```
> **Error:** Cannot nest interactive elements (`<a>` inside `<a>`).

### Error 5:
```html
<label>Name</label>
<input type="text" id="name">
```
> **Error:** Label missing `for` attribute to connect it to the input. Add `for="name"`.

### Error 6:
```html
<table>
    <td>Cell 1</td>
    <td>Cell 2</td>
</table>
```
> **Error:** Missing `<tr>` (table row). `<td>` must be inside `<tr>`.

### Error 7:
```html
<form method="post" action="/upload">
    <input type="file" name="doc">
    <button type="submit">Upload</button>
</form>
```
> **Error:** Missing `enctype="multipart/form-data"` (required for file uploads).

### Error 8:
```html
<div id="header">...</div>
<div id="header">...</div>
```
> **Error:** Duplicate `id` values. IDs must be unique on a page.

### Error 9:
```html
<span>
    <h2>Heading</h2>
    <p>Paragraph</p>
</span>
```
> **Error:** Block elements (`<h2>`, `<p>`) inside an inline element (`<span>`). Use `<div>` instead.

### Error 10:
```html
<input type=text name=user placeholder=Enter name>
```
> **Error:** While technically valid in HTML5, attribute values with spaces MUST be quoted. `placeholder` value would be truncated to just "Enter". Use quotes: `placeholder="Enter name"`.

### Error 11:
```html
<button>
    <a href="/next-page">Continue</a>
</button>
```
> **Error:** Interactive elements should not be nested (`<a>` inside `<button>`). Use either a styled link OR a button, not both together.

### Error 12:
```html
<html>
<head>
    <title>My Page</title>
</head>
<body>...</body>
</html>
```
> **Error:** Missing `<!DOCTYPE html>` at the top, which can cause quirks mode rendering.

### Error 13:
```html
<img src="team.jpg" alt="image">
```
> **Error:** `alt="image"` is not meaningful. Alt text should describe the content/purpose, e.g. `alt="Development team standing in front of office"`.

### Error 14:
```html
<label for="email">Email</label>
<input type="email" id="user-email">
```
> **Error:** `for` and `id` values do not match, so the label is not correctly connected. Use `for="user-email"` or change `id` to `email`.

---
