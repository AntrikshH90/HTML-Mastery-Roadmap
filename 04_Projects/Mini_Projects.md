# 🏗️ MINI PROJECTS

## 🟢 Project 1: Personal Bio Page (Beginner)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Me</title>
    <style>
        body { font-family: Arial, sans-serif; max-width: 600px; margin: 50px auto; 
               padding: 20px; background: #f5f5f5; }
        .card { background: white; padding: 30px; border-radius: 15px; 
                box-shadow: 0 2px 10px rgba(0,0,0,0.1); text-align: center; }
        img { border-radius: 50%; width: 150px; height: 150px; object-fit: cover; }
        h1 { color: #333; margin: 15px 0 5px; }
        .subtitle { color: #667; font-style: italic; }
        .skills { display: flex; flex-wrap: wrap; gap: 8px; justify-content: center; margin: 20px 0; }
        .skill { background: #e7f1ff; color: #007bff; padding: 5px 15px; border-radius: 20px; font-size: 14px; }
        a { color: #007bff; text-decoration: none; }
        a:hover { text-decoration: underline; }
    </style>
</head>
<body>
    <div class="card">
        <img src="https://via.placeholder.com/150" alt="My Photo">
        <h1>Your Name</h1>
        <p class="subtitle">Web Developer & Designer</p>
        <hr>
        <h3>About Me</h3>
        <p>I'm a passionate web developer learning HTML, CSS, and JavaScript. 
           I love building beautiful and accessible websites.</p>
        <h3>Skills</h3>
        <div class="skills">
            <span class="skill">HTML5</span>
            <span class="skill">CSS3</span>
            <span class="skill">JavaScript</span>
            <span class="skill">React</span>
            <span class="skill">Git</span>
        </div>
        <h3>Contact</h3>
        <p>
            📧 <a href="mailto:you@example.com">you@example.com</a><br>
            🔗 <a href="https://github.com/you" target="_blank">GitHub</a>
        </p>
    </div>
</body>
</html>
```

## 🟡 Project 2: FAQ Accordion (Intermediate — No JS!)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FAQ</title>
    <style>
        body { font-family: 'Segoe UI', sans-serif; background: #f0f2f5; 
               display: flex; justify-content: center; padding: 40px 20px; }
        .faq { max-width: 700px; width: 100%; }
        h1 { text-align: center; color: #1a1a2e; }
        details { background: white; margin-bottom: 10px; border-radius: 10px;
                  box-shadow: 0 2px 5px rgba(0,0,0,0.05); overflow: hidden; }
        details[open] { border-left: 4px solid #e94560; }
        summary { padding: 20px; cursor: pointer; font-weight: 600;
                  font-size: 1.1em; list-style: none; }
        summary::-webkit-details-marker { display: none; }
        summary::after { content: '+'; float: right; font-size: 1.5em; color: #e94560; }
        details[open] summary::after { content: '−'; }
        details p { padding: 0 20px 20px; color: #555; line-height: 1.8; }
    </style>
</head>
<body>
    <div class="faq">
        <h1>❓ Frequently Asked Questions</h1>
        
        <details name="faq">
            <summary>What is HTML?</summary>
            <p>HTML (HyperText Markup Language) is the standard language for 
               creating web pages. It describes the structure and content.</p>
        </details>
        <details name="faq">
            <summary>Is HTML a programming language?</summary>
            <p>No, HTML is a markup language, not a programming language. 
               It doesn't have logic, loops, or conditions.</p>
        </details>
        <details name="faq">
            <summary>What's new in HTML5?</summary>
            <p>HTML5 introduced semantic elements, multimedia support, 
               canvas, new form input types, and many APIs.</p>
        </details>
        <details name="faq">
            <summary>How do I make my website responsive?</summary>
            <p>Start with the viewport meta tag, then use CSS media queries, 
               flexible grids, and responsive images.</p>
        </details>
    </div>
</body>
</html>
```

## 🔴 Project 3: Registration Form (Advanced)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration</title>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body { font-family: 'Segoe UI', sans-serif; background: #667eea; 
               min-height: 100vh; display: flex; align-items: center; justify-content: center; padding: 20px; }
        form { max-width: 500px; width: 100%; background: white; padding: 40px; 
               border-radius: 15px; box-shadow: 0 10px 40px rgba(0,0,0,0.2); }
        h2 { text-align: center; margin-bottom: 25px; color: #333; }
        fieldset { border: 1px solid #eee; padding: 15px; margin-bottom: 15px; border-radius: 8px; }
        legend { font-weight: bold; color: #667eea; padding: 0 10px; }
        label { display: block; margin: 10px 0 5px; font-weight: 600; color: #555; }
        input, select, textarea { width: 100%; padding: 10px; border: 2px solid #eee; 
                                   border-radius: 8px; font-size: 14px; transition: 0.3s; }
        input:focus, select:focus, textarea:focus { outline: none; border-color: #667eea; }
        input:valid:not(:placeholder-shown) { border-color: #28a745; }
        .checkbox-row { display: flex; align-items: center; gap: 10px; margin: 15px 0; }
        .checkbox-row input { width: auto; }
        button { width: 100%; padding: 12px; background: #667eea; color: white; 
                 border: none; border-radius: 8px; font-size: 16px; cursor: pointer; font-weight: 600; }
        button:hover { background: #5a6fd6; }
    </style>
</head>
<body>
    <form action="/register" method="POST">
        <h2>🚀 Create Account</h2>
        
        <fieldset>
            <legend>👤 Personal Info</legend>
            <label for="name">Full Name *</label>
            <input type="text" id="name" name="name" placeholder="John Doe" required minlength="2">
            
            <label for="email">Email *</label>
            <input type="email" id="email" name="email" placeholder="john@example.com" required>
            
            <label for="phone">Phone</label>
            <input type="tel" id="phone" name="phone" placeholder="123-456-7890" inputmode="tel">
            
            <label for="dob">Date of Birth</label>
            <input type="date" id="dob" name="dob">
        </fieldset>
        
        <fieldset>
            <legend>🔐 Account</legend>
            <label for="username">Username *</label>
            <input type="text" id="username" name="username" placeholder="johndoe" required minlength="3">
            
            <label for="password">Password *</label>
            <input type="password" id="password" name="password" placeholder="Min 8 characters" required minlength="8">
            
            <label for="country">Country</label>
            <select id="country" name="country">
                <option value="">-- Select --</option>
                <optgroup label="Asia">
                    <option value="in">🇮🇳 India</option>
                    <option value="jp">🇯🇵 Japan</option>
                </optgroup>
                <optgroup label="Americas">
                    <option value="us">🇺🇸 United States</option>
                    <option value="ca">🇨🇦 Canada</option>
                </optgroup>
            </select>
            
            <label>Favorite Language</label>
            <input list="languages" name="language" placeholder="Start typing...">
            <datalist id="languages">
                <option value="JavaScript">
                <option value="Python">
                <option value="Java">
                <option value="C++">
            </datalist>
            
            <label for="bio">Bio</label>
            <textarea id="bio" name="bio" rows="3" placeholder="Tell us about yourself..." maxlength="300"></textarea>
        </fieldset>
        
        <div class="checkbox-row">
            <input type="checkbox" id="terms" name="terms" required>
            <label for="terms" style="display:inline; font-weight:normal;">
                I agree to the Terms & Conditions *
            </label>
        </div>
        
        <button type="submit">Create Account</button>
    </form>
</body>
</html>
```

## 🟣 Project 4: Semantic Portfolio Landing Page (Intermediate/Advanced)

**What to build (short):**
- A one-page portfolio using semantic sections: `header`, `nav`, `main`, `section`, `article`, `footer`
- Hero section with intro + call-to-action button
- Projects section with 3 project cards (`figure` + `figcaption`)
- Contact section with form fields and proper labels

**Why this project is useful:**
- Combines real interview-ready structure in one page
- Practices semantics, accessibility, links, media, and form basics together
- Makes a clean starter template you can later enhance with CSS/JS

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio Landing Page</title>
</head>
<body>
    <header>
        <h1>Alex Developer</h1>
        <nav aria-label="Main navigation">
            <a href="#about">About</a>
            <a href="#projects">Projects</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <main>
        <section id="about">
            <h2>About Me</h2>
            <p>I build clean and accessible web pages using semantic HTML.</p>
            <a href="#projects">View Projects</a>
        </section>

        <section id="projects">
            <h2>Projects</h2>
            <article>
                <figure>
                    <img src="project1.jpg" alt="Screenshot of project one" loading="lazy" width="600" height="350">
                    <figcaption>Project 1: Product Page</figcaption>
                </figure>
            </article>
            <article>
                <figure>
                    <img src="project2.jpg" alt="Screenshot of project two" loading="lazy" width="600" height="350">
                    <figcaption>Project 2: Blog Layout</figcaption>
                </figure>
            </article>
            <article>
                <figure>
                    <img src="project3.jpg" alt="Screenshot of project three" loading="lazy" width="600" height="350">
                    <figcaption>Project 3: FAQ Page</figcaption>
                </figure>
            </article>
        </section>

        <section id="contact">
            <h2>Contact</h2>
            <form action="/contact" method="post">
                <label for="name">Name</label>
                <input type="text" id="name" name="name" required>

                <label for="email">Email</label>
                <input type="email" id="email" name="email" required>

                <label for="message">Message</label>
                <textarea id="message" name="message" rows="4" required></textarea>

                <button type="submit">Send Message</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 Alex Developer. Built with semantic HTML.</p>
    </footer>
</body>
</html>
```

---
