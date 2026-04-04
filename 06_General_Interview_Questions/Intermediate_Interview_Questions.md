## 🟡 INTERMEDIATE QUESTIONS (30 Questions)

**Q51.** What is the difference between `<section>`, `<article>`, and `<div>`?
> **A:** `<section>` = thematic grouping with a heading. `<article>` = self-contained, independently distributable content. `<div>` = no semantic meaning, just grouping.

**Q52.** When should you use `<figure>` and `<figcaption>`?
> **A:** When content (image, diagram, code block) is self-contained and referenced from the main content. `<figcaption>` provides its caption.

**Q53.** What's the difference between `<details>` and a JavaScript accordion?
> **A:** `<details>` is native HTML — works without JS, is accessible by default, semantic. JS accordion requires custom code for accessibility and functionality.

**Q54.** Explain the difference between `<del>` and `<s>`.
> **A:** `<del>` represents content that was deleted/edited (has `cite` and `datetime` attributes). `<s>` represents content no longer relevant but not a document edit.

**Q55.** What is the `enctype` attribute on forms?
> **A:** Specifies how form data is encoded. `application/x-www-form-urlencoded` (default), `multipart/form-data` (for file uploads), `text/plain` (debugging).

**Q56.** How do radio buttons work in groups?
> **A:** All radio buttons with the same `name` attribute form a group — only one can be selected at a time.

**Q57.** What is a `<datalist>` and how does it differ from `<select>`?
> **A:** `<datalist>` provides autocomplete suggestions but users can type any value. `<select>` restricts users to only the predefined options.

**Q58.** What is `contenteditable`?
> **A:** A global attribute that makes any HTML element editable directly in the browser by the user. Example: `<div contenteditable="true">Edit me</div>`

**Q59.** What are `data-*` attributes?
> **A:** Custom attributes for storing extra data on HTML elements. Accessed via JavaScript's `element.dataset` property. Example: `data-user-id="42"` → `dataset.userId`

**Q60.** What is the `<output>` element?
> **A:** Represents the result of a calculation or user action. Used with forms: `<output name="result" for="a b">30</output>`

**Q61.** Explain `colspan` and `rowspan`.
> **A:** `colspan` makes a cell span multiple columns horizontally. `rowspan` makes a cell span multiple rows vertically.

**Q62.** What's the difference between `<meter>` and `<progress>`?
> **A:** `<progress>` shows completion of a task (loading bar). `<meter>` shows a scalar measurement within a known range (disk usage, fuel gauge).

**Q63.** What is the `scope` attribute on `<th>`?
> **A:** Specifies whether a header cell relates to a `col` (column), `row`, `colgroup`, or `rowgroup`. Improves table accessibility for screen readers.

**Q64.** How does the `<picture>` element work?
> **A:** Contains multiple `<source>` elements with different images for different conditions (screen size, format). Browser picks the first matching source. `<img>` inside acts as fallback.

**Q65.** What is `srcset` on images?
> **A:** Lets the browser choose the best image size based on device screen width/pixel density. Example: `srcset="small.jpg 400w, large.jpg 800w"`

**Q66.** What is the `<template>` element?
> **A:** Holds HTML that is NOT rendered on page load. Content is invisible and inert until cloned via JavaScript. Used as a blueprint for dynamic content.

**Q67.** What is the purpose of `<wbr>`?
> **A:** Word Break Opportunity — suggests where a browser MAY break a long word or URL if needed for wrapping. Doesn't force a break.

**Q68.** What are ARIA roles and when should you use them?
> **A:** ARIA (Accessible Rich Internet Applications) roles provide semantic meaning to elements for screen readers. Use them when HTML semantic tags aren't sufficient.

**Q69.** Explain `defer` vs `async` on `<script>`.
> **A:** `defer` downloads in parallel, executes AFTER HTML parsing, maintains order. `async` downloads in parallel, executes IMMEDIATELY when ready, no guaranteed order.

**Q70.** What is the `<dialog>` element?
> **A:** Native HTML modal/popup. Use `.showModal()` to open as modal, `.show()` as non-modal. Supports backdrop styling, form method="dialog" for closing.

**Q71.** What is the Popover API?
> **A:** Native HTML feature for creating popovers without JavaScript. Use `popover` attribute on target and `popovertarget` on the trigger button.

**Q72.** What's the difference between absolute and relative URLs?
> **A:** Absolute = full path (`https://example.com/page.html`). Relative = path relative to current file (`../images/photo.jpg`).

**Q73.** What is the `sandbox` attribute on `<iframe>`?
> **A:** Restricts iframe capabilities for security. Empty = maximum restrictions. Add values to allow specific features: `allow-scripts`, `allow-same-origin`, `allow-forms`.

**Q74.** How do you make a form field read-only vs disabled?
> **A:** `readonly` — can't edit but value IS submitted. `disabled` — can't edit and value is NOT submitted.

**Q75.** What is `inputmode`?
> **A:** Hints to mobile browsers which virtual keyboard to show. Values: `numeric`, `tel`, `email`, `url`, `search`, `decimal`, `none`.

**Q76.** What is the `<search>` element?
> **A:** New semantic element (2023) that wraps search functionality. Replaces `<div role="search">`.

**Q77.** What is the `inert` attribute?
> **A:** Makes an element and all its children completely non-interactive — can't click, focus, or select anything inside.

**Q78.** What is `fetchpriority`?
> **A:** Hints to the browser about the priority of a resource fetch. Values: `high`, `low`, `auto`. Use `high` for hero images, `low` for below-fold content.

**Q79.** How do you prevent layout shift with images?
> **A:** Always specify `width` and `height` attributes on `<img>` tags. This lets the browser reserve space before the image loads.

**Q80.** What is JSON-LD structured data?
> **A:** A script block (`type="application/ld+json"`) containing Schema.org structured data in JSON format. Helps search engines understand page content for rich results.

---
