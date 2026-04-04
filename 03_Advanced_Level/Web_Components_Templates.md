# 🧩 WEB COMPONENTS & TEMPLATES

```html
<template id="greeting-template">
    <style>
        .greeting { padding: 20px; background: #f0f8ff; border-radius: 10px; }
    </style>
    <div class="greeting">
        <slot name="title"><h2>Hello!</h2></slot>
        <slot>Default content here</slot>
    </div>
</template>

<script>
class GreetingCard extends HTMLElement {
    constructor() {
        super();
        const shadow = this.attachShadow({ mode: 'open' });
        const template = document.getElementById('greeting-template');
        shadow.appendChild(template.content.cloneNode(true));
    }
}
customElements.define('greeting-card', GreetingCard);
</script>

<greeting-card>
    <h2 slot="title">Welcome!</h2>
    <p>Custom content goes here.</p>
</greeting-card>
```

---

