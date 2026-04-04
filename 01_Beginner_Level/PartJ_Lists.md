# 🅹 PART J: LISTS

## 📖 Theory (from PDF)

> Using HTML it's possible to display information in a list. This makes it easier to understand the data. HTML provides **3 ways** to specify the information.

| List Type | Description (from PDF) |
|-----------|----------------------|
| `<ol>` | To insert **ordered list** in the web page |
| `<ul>` | To insert **unordered list** in the web page |
| `<dl>` | To insert **description list** in the web page, arranged in key-value pair |

> In the examples, `<li>` is used to insert a list item, `<dt>` means **data term** (key) and `<dd>` means **data description** (value).

## 1. Unordered List (from PDF)

> An unordered list displays items in **bullets** format. Type attribute specifies the type of bullet:
> - **disc** – solid circle
> - **square** – solid square
> - **circle** – hollow circle

```html
<ul type="disc">
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>

<ul type="square">
    <li>Square bullet</li>
</ul>

<ul type="circle">
    <li>Hollow circle bullet</li>
</ul>
```

## 2. Ordered List (from PDF)

> An ordered list displays items in **numbered format**. Type attribute specifies type of sequence:
> - Type: `1`, `A`, `a`, `I`, `i`

```html
<!-- Default numbered (1, 2, 3...) -->
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>

<!-- Different types -->
<ol type="A"><li>Uppercase letters (A, B, C)</li></ol>
<ol type="a"><li>Lowercase letters (a, b, c)</li></ol>
<ol type="I"><li>Roman numerals (I, II, III)</li></ol>
<ol type="i"><li>Lowercase roman (i, ii, iii)</li></ol>

<!-- Start from specific number -->
<ol start="5">
    <li>This is item 5</li>
    <li>This is item 6</li>
</ol>

<!-- Reverse order -->
<ol reversed>
    <li>Third (shows as 3)</li>
    <li>Second (shows as 2)</li>
    <li>First (shows as 1)</li>
</ol>
```

## 3. Description List (from PDF)

> Definition list is not a list of items. It's a list of **term and explanation** of term.

```html
<dl>
    <dt>HTML</dt>
    <dd>A markup language for creating web pages</dd>
    
    <dt>CSS</dt>
    <dd>A style sheet language for designing web pages</dd>
</dl>
```

## 4. Nested List (from PDF)

> The list inside another list is known as a **nested list**.

```html
<ul>
    <li>Fruits
        <ul>
            <li>Apple</li>
            <li>Banana</li>
            <li>Orange</li>
        </ul>
    </li>
    <li>Vegetables
        <ul>
            <li>Carrot</li>
            <li>Broccoli</li>
            <li>Spinach</li>
        </ul>
    </li>
</ul>
```

## Complete List Example (from PDF Page 10)

```html
<!DOCTYPE html>
<html>
<head>
    <title>HTML Lists</title>
</head>
<body>
    <section>
        <h3>Ordered List</h3>
        <ol>
            <li>One</li>
            <li>Two</li>
            <li>Three</li>
        </ol>
    </section>
    <section>
        <h3>Unordered List</h3>
        <ul>
            <li>One</li>
            <li>Two</li>
            <li>Three</li>
        </ul>
    </section>
    <section>
        <h3>Description List</h3>
        <dl>
            <dt>One</dt>
            <dd>One Description</dd>
            <dt>Two</dt>
            <dd>Two Description</dd>
            <dt>Three</dt>
            <dd>Three Description</dd>
        </dl>
    </section>
</body>
</html>
```

> 💡 **When to use which:** Use `<ul>` for unrelated items, `<ol>` when order matters (steps, rankings), `<dl>` for term-definition pairs (glossaries, FAQs).

---

