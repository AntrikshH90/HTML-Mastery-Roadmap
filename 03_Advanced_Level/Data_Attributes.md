# 📊 DATA ATTRIBUTES

```html
<!-- Store custom data on elements -->
<div data-user-id="123" data-role="admin" data-active="true">
    <h3>John Doe</h3>
</div>

<script>
const el = document.querySelector('[data-user-id]');
console.log(el.dataset.userId);   // "123" (camelCase)
console.log(el.dataset.role);     // "admin"
</script>

<style>
[data-role="admin"] { border-left: 4px solid red; }
[data-active]::after { content: " ✓"; color: green; }
</style>
```

---

