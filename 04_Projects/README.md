# 🛠️ Hand-Coded HTML Projects

Welcome to the ultimate practical section. To truly master HTML, you must build pages without relying on massive frontend frameworks. These two projects are designed to be built in pure `index.html` files. Follow the steps exactly.

---

## 🏆 Project 1: The Semantic SEO-Optimized Blog Post
**Goal:** Build a complete blog post layout utilizing every single HTML5 semantic tag correctly to ensure 100% Lighthouse SEO and Accessibility scores.

### Step 1: The Boilerplate & Meta Tags
1. Create a file named `blog.html`.
2. Generate the HTML5 boilerplate (`!`).
3. Add a `<meta name="description" content="...">` tag summarizing your blog post.
4. Add a `<meta name="author" content="Your Name">` tag.

### Step 2: Site Header & Navigation
1. Open the `<body>` tag.
2. Create a `<header>` element.
3. Inside the `<header>`, add an `<h1>` for your blog's main title (e.g., "Tech Today").
4. Add a `<nav>` element containing an unordered list `<ul>` of three links: Home, About, Contact.

### Step 3: The Main Content Area
1. Below the `<header>`, open a `<main>` tag. This strictly holds the primary content.
2. Inside `<main>`, create an `<article>` tag to enclose your actual blog post.
3. Add an `<h2>` for the post title, followed by a `<p>` tag indicating the author and publication `<time datetime="2026-03-20">March 20, 2026</time>`.
4. Write three paragraphs of placeholder text. 
5. Add a responsive `<img>` tag with a highly descriptive `alt` attribute.

### Step 4: The Aside (Sidebar)
1. Below the `<article>`, but STILL inside the `<main>` tag, add an `<aside>` element.
2. This will act as your "Related Posts" sidebar. Add an `<h3>` and an unordered list of three links to fake articles.

### Step 5: The Footer
1. Close the `<main>` tag.
2. Create a `<footer>` containing a paragraph with your copyright info using the special `&copy;` entity: `<p>&copy; 2026 Antriksh Yadav</p>`.

**Interview Value:** When asked "How do you structure an SEO-friendly application?", you can directly reference this exact Semantic architecture.

---

## 🏆 Project 2: The Ultra-Secure Registration Interface
**Goal:** Build a web form utilizing advanced HTML5 validation API, ARIA accessibility features, and data grouping.

### Step 1: Form Scaffold & Fieldset
1. Create `register.html`.
2. Open a `<form action="/submit" method="POST">`.
3. Wrap the primary inputs inside a `<fieldset>`, and give it a `<legend>Personal Information</legend>`. This natively groups the data for screen readers!

### Step 2: Advanced Inputs & Validation
1. Create an Email field (`<input type="email">`). Add the `required` and `autocomplete="email"` attributes.
2. Create a secure Password field (`<input type="password">`). 
   - Add `required`
   - Add `minlength="12"`
   - Add `pattern="(?=.*\d)(?=.*[a-z])(?=.*[A-Z]).{12,}"` (Forces 1 capital, 1 lowercase, 1 number).
   - Add `title="Must contain at least one number and one uppercase and lowercase letter, and at least 12 or more characters"` so the browser natively warns the user if they fail!

### Step 3: Accessibility Enhancements
1. Ensure EVERY single `<input>` has a perfectly matched `<label for="id">`.
2. Below the password input, add a `<span>` saying "Password must be 12 chars". Give it `id="pwd-hint"`.
3. Go back to your password `<input>` and add the ARIA attribute: `aria-describedby="pwd-hint"`. This magically forces assistive readers to read the hint out loud when focusing the password box!

### Step 4: Submit & Reset
1. Add a `<button type="submit">Register Workspace</button>`.
2. Add an input `<input type="reset" value="Clear Form">`.

**Interview Value:** Mastering `pattern` regex validation and `aria-describedby` entirely natively without using JavaScript proves you are a highly seasoned UI/UX structural engineer.
