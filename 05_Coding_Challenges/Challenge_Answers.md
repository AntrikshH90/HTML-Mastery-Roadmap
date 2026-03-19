# 💻 HTML Coding Challenges: Detailed Answer Key

Here are the precise, structurally perfect solutions to the coding challenges. This highlights extremely advanced uses of elements like `rowspan`, `<dl>`, and semantic multimedia formatting!

---

## 🛠️ Challenge 1: The Complex Data Table
**Answer:**
```html
<table border="1">
    <caption>Semester 1 Results</caption>
    <thead>
        <tr>
            <th>Subject</th>
            <th>Midterms</th>
            <th>Finals</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Math</td>
            <td>85</td>
            <td>90</td>
        </tr>
        <tr>
            <!-- Here is the rowspan magic! It merges two rows in the Subject column! -->
            <td rowspan="2">Science</td>
            <td>Lab: 95</td>
            <td>Lab: 98</td>
        </tr>
        <tr>
            <!-- Notice we skip the first <td> because 'Science' above claimed this space using rowspan -->
            <td>Theory: 80</td>
            <td>Theory: 85</td>
        </tr>
        <tr>
            <td>History</td>
            <td>75</td>
            <td>80</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="3" style="text-align: center;">Status: PASS 🚀</td>
        </tr>
    </tfoot>
</table>
```
💡 **Interview Tip:** Always explain to the recruiter that `<thead>`, `<tbody>`, and `<tfoot>` do not exist merely for visual styling (since CSS handles that). They exist strictly so developers can isolate data loops (like React `.map()`) safely inside the `<tbody>` without breaking headers or footers!

---

## 🛠️ Challenge 2: Embedded Multi-Media Article
**Answer:**
```html
<article>
    <h1>The Power of Lazy Loading</h1>
    
    <!-- Using the loading="lazy" attribute dramatically boosts Core Web Vitals (SEO) -->
    <img src="placeholder.jpg" alt="A developer lazy loading images" loading="lazy" width="800" height="400">
    
    <p>In this post, we discuss the importance of native media rendering.</p>
    
    <!-- Embedding audio natively without third-party scripts. 'controls' displays play/pause natively. -->
    <audio controls>
        <source src="podcast-episode.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>

    <!-- Semantic quoting is heavily tested in basic interviews -->
    <figure>
        <blockquote cite="https://example.com/source">
            <p>"Building performant frontends starts with semantic HTML, not JavaScript."</p>
        </blockquote>
        <figcaption>
            — <cite>Senior CSS Developer</cite>
        </figcaption>
    </figure>
</article>
```

---

## 🛠️ Challenge 3: Advanced Form Layout
**Answer:**
```html
<form action="/submit-data" method="POST">
    <fieldset>
        <legend>User Details</legend>
        
        <!-- Date specifically blocked via 'min' -->
        <label for="birthdate">Date of Birth (Post 2026):</label>
        <input type="date" id="birthdate" name="bday" min="2026-01-01" required>

        <!-- Dropdown menu -->
        <label for="country">Country:</label>
        <select id="country" name="country">
            <option value="in">India</option>
            <option value="us">United States</option>
            <option value="uk">United Kingdom</option>
        </select>

        <!-- Radio buttons logically grouped by the 'name' attribute overlapping -->
        <p>Gender:</p>
        <label>
            <input type="radio" name="genderOptions" value="male"> Male
        </label>
        <label>
            <!-- Clicking the word 'Female' cleanly toggles the radio button because it's wrapped in the label -->
            <input type="radio" name="genderOptions" value="female"> Female
        </label>

        <br>
        
        <!-- Checkbox with linked clickability -->
        <label for="terms">
            <input type="checkbox" id="terms" name="agree" required> I intensely agree to the Terms of Service.
        </label>

    </fieldset>
</form>
```

---

## 🛠️ Challenge 4: The Description List (Dictionary)
**Answer:**
```html
<dl>
    <dt>HTML (HyperText Markup Language)</dt>
    <dd>The standard markup language strictly used to build the skeleton of web pages.</dd>
    
    <dt>DOM (Document Object Model)</dt>
    <dd>An application programming interface (API) describing HTML or XML web documents natively loaded into the browser.</dd>
    
    <dt>CSS (Cascading Style Sheets)</dt>
    <dd>The styling language entirely responsible for altering the visual aesthetics constructed by HTML tags.</dd>
</dl>
```
💡 **Trick:** Think of `<dl>` as a literal Dictionary List! `<dt>` stands for Dictionary Term, and `<dd>` is the Dictionary Definition! Use this anywhere there is a paired key-value text listing instead of a standard `<ul>`.
