## 🔴 ADVANCED QUESTIONS (20 Questions)

**Q81.** Explain the difference between HTML5 semantic elements and ARIA roles. When would you use ARIA over semantic HTML?
> **A:** Semantic elements have built-in accessibility. ARIA is for cases where HTML doesn't have a suitable element or for dynamic content (custom widgets, live regions, state changes). Rule: use semantic HTML first, ARIA only when needed.

**Q82.** What is Shadow DOM and how does it relate to HTML?
> **A:** Shadow DOM encapsulates a component's HTML and CSS so it's isolated from the main document. Used with Web Components via `element.attachShadow()`.

**Q83.** Explain the Content Security Policy and how it's set via HTML.
> **A:** CSP restricts which resources (scripts, styles, images) can load. Set via `<meta http-equiv="Content-Security-Policy" content="...">` or HTTP headers.

**Q84.** What are Speculation Rules and how do they improve performance?
> **A:** A `<script type="speculationrules">` block that tells the browser to prerender or prefetch specific pages the user is likely to visit next.

**Q85.** How does the View Transitions API work with HTML?
> **A:** CSS `@view-transition { navigation: auto; }` enables animated transitions between page navigations. Elements can be named with `view-transition-name` for matched animations.

**Q86.** What is the difference between `preload`, `prefetch`, `preconnect`, and `prerender`?
> **A:** `preload` = current page critical resource. `prefetch` = next page resource (low priority). `preconnect` = establish connection to external domain. `prerender` = fully render a page in background.

**Q87.** Explain microdata vs JSON-LD vs RDFa for structured data.
> **A:** Microdata = inline attributes (`itemscope`, `itemprop`). JSON-LD = separate script block (Google's recommendation). RDFa = inline attributes (more complex). JSON-LD is preferred.

**Q88.** How do custom elements work? Show the lifecycle callbacks.
> **A:** Extend `HTMLElement`, define with `customElements.define()`. Callbacks: `connectedCallback()`, `disconnectedCallback()`, `attributeChangedCallback()`, `adoptedCallback()`.

**Q89.** What is the `blocking="render"` attribute?
> **A:** Tells the browser to not render ANY content until the specified resource is loaded. Used for critical CSS/JS that must be available before first paint.

**Q90.** How does the `<slot>` element work in Web Components?
> **A:** `<slot>` is a placeholder in Shadow DOM where external (light DOM) content is projected. Named slots (`<slot name="title">`) allow multiple insertion points.

**Q91.** What is the difference between `loading="lazy"` and Intersection Observer?
> **A:** `loading="lazy"` is native HTML attribute for deferred loading. Intersection Observer is a JavaScript API that gives more control over when elements become visible. Native lazy loading is simpler; IO is more flexible.

**Q92.** How would you implement an accessible modal dialog?
> **A:** Use `<dialog>` with `showModal()`. Trap focus inside. Close on Escape. Return focus to trigger on close. Use `aria-labelledby` for title. Backdrop prevents background interaction.

**Q93.** What is the `<base>` tag and what are its risks?
> **A:** Sets base URL for all relative links. Risk: affects ALL relative URLs on the page including anchors, form actions, and CSS paths. Can cause unexpected behavior.

**Q94.** How do you make an HTML email? Why can't you use modern CSS?
> **A:** Use table-based layouts with inline styles. Email clients strip `<head>` styles, don't support flexbox/grid, and have inconsistent CSS support. Test with Litmus/Email on Acid.

**Q95.** Explain the importance of the `lang` attribute.
> **A:** Tells browsers and screen readers the language. Affects text-to-speech pronunciation, spell checking, translation tools, search engine language detection, and hyphenation.

**Q96.** What is the `nonce` attribute used for?
> **A:** A one-time-use token for Content Security Policy. Allows specific inline scripts/styles to execute while blocking all others. Must be unique per page load.

**Q97.** How does the `translate` attribute work?
> **A:** `translate="no"` tells translation tools (Google Translate) to skip that element. Useful for brand names, code, and identifiers.

**Q98.** What is the `enterkeyhint` attribute?
> **A:** Changes the label on the Enter/Return key on mobile virtual keyboards. Values: `enter`, `done`, `go`, `next`, `previous`, `search`, `send`.

**Q99.** Explain how the exclusive accordion works with `<details name="...">`
> **A:** All `<details>` elements with the same `name` attribute form a group where only one can be open at a time. Opening one automatically closes others.

**Q100.** What will HTML look like in the future?
> **A:** HTML is now a Living Standard (continuous updates). Key trends: more native interactive elements (popover, dialog), declarative JS-free interactions (invoker commands), better form customization (customizable select), enhanced security features, and deeper integration with CSS (anchor positioning, scroll-driven animations).

---
