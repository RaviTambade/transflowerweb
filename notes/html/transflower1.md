## Step-by-step guide  **Transflower Learning** website"**.

A compact, practical walkthrough to build a simple **Transflower Learning** static website using plain HTML (with a little CSS). This guide covers project structure, commonly used HTML elements, accessibility, and sample files you can copy and modify.


## 1. Project idea & scope

Transflower Learning is a small educational site that offers:

* Home (welcome + featured courses)
* About (mission, instructors)
* Courses / Lessons (list of learning modules)
* Contact (simple contact form)

Keep it small: 4–6 pages, responsive and accessible.



## 2. Folder structure (recommended)

```
transflower/
├─ index.html
├─ about.html
├─ courses.html
├─ lesson.html        (template for individual lesson)
├─ contact.html
├─ css/
│  └─ style.css
├─ images/
│  └─ logo.png
└─ assets/
   └─ favicon.ico
```


## 3. HTML basics to use often (elements & roles)

Use semantic tags wherever possible:

* `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`
* Headings: `<h1>`…`<h6>` — one `<h1>` per page
* Text: `<p>`, `<strong>`, `<em>`, `<small>`
* Links & images: `<a href="...">`, `<img src="..." alt="...">`
* Lists: `<ul>`, `<ol>`, `<li>`
* Media: `<figure>`, `<figcaption>`
* Forms: `<form>`, `<label>`, `<input>`, `<textarea>`, `<button>`, `<select>`
* Tables (if needed): `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`
* Metadata & SEO: `<meta name="description">`, `<meta charset="utf-8">`, `<title>`

Use ARIA and good `alt` text for accessibility when necessary.


## 4. Boilerplate HTML (use on every page)

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Transflower Learning — Page Title</title>
  <meta name="description" content="Transflower Learning: short description of the site">
  <link rel="stylesheet" href="css/style.css">
  <link rel="icon" href="assets/favicon.ico">
</head>
<body>
  <!-- content here -->
</body>
</html>
```


## 5. Navigation bar (example)

Place this inside `<header>` so every page can have consistent navigation.

```html
<header>
  <div class="container">
    <a href="index.html" class="logo"><img src="images/logo.png" alt="Transflower logo"></a>
    <nav>
      <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="courses.html">Courses</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
  </div>
</header>
```



## 6. Sample `index.html` (complete minimal home page)

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Transflower Learning — Home</title>
  <meta name="description" content="Free and friendly learning modules on web and programming">
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header>
    <div class="container">
      <a class="logo" href="index.html"><img src="images/logo.png" alt="Transflower logo" width="120"></a>
      <nav aria-label="Main navigation">
        <ul>
          <li><a href="index.html">Home</a></li>
          <li><a href="about.html">About</a></li>
          <li><a href="courses.html">Courses</a></li>
          <li><a href="contact.html">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero">
      <h1>Welcome to Transflower Learning</h1>
      <p>Learn web, programming basics and more, step by step.</p>
      <a class="btn" href="courses.html">Explore courses</a>
    </section>

    <section class="features">
      <article>
        <h2>Beginner friendly</h2>
        <p>Short lessons, clear examples, practice tasks.</p>
      </article>
      <article>
        <h2>Hands-on projects</h2>
        <p>Work on small projects and build your portfolio.</p>
      </article>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Transflower Learning</p>
  </footer>
</body>
</html>
```



## 7. Simple `css/style.css` (start here)

```css
/* Reset-ish */
* { box-sizing: border-box; }
body { font-family: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial; margin:0; line-height:1.5; }
.container{ max-width:1000px; margin:0 auto; padding:1rem; }
header{ background:#f8f9fa; border-bottom:1px solid #e8e8e8; }
header .container{ display:flex; align-items:center; justify-content:space-between; }
nav ul{ list-style:none; display:flex; gap:1rem; margin:0; padding:0; }
a{ color:inherit; text-decoration:none; }
.hero{ padding:3rem 0; text-align:center; }
.features{ display:flex; gap:1rem; padding:2rem 0; }
.features article{ flex:1; padding:1rem; border:1px solid #eee; border-radius:8px; }
.btn{ display:inline-block; padding:0.5rem 1rem; border-radius:6px; background:#007bff; color:white; }
footer{ text-align:center; padding:1rem 0; border-top:1px solid #eee; }

/* Responsive */
@media (max-width:700px){
  .features{ flex-direction:column; }
  header .container{ flex-direction:column; gap:0.5rem; }
  nav ul{ flex-direction:column; align-items:center; }
}
```


## 8. Courses / Lessons page ideas

* Use a list of course cards (each `<article>` with an `<h3>`, summary `<p>`, and "Start" link).
* For each lesson use a structured article: title (`<h1>`), published date (`<time datetime="2025-11-05">`), content sections (`<section>`), code blocks (`<pre><code>`), and a navigation to previous/next lesson.

Example course card:

```html
<article class="course-card">
  <h3>HTML Basics</h3>
  <p>Learn elements, semantic HTML, and best practices.</p>
  <a href="lesson.html">Start lesson</a>
</article>
```


## 9. Contact page (form)

Keep the form simple and accessible. Use `label` for inputs and `required` where necessary.

```html
<form action="#" method="post" aria-label="Contact form">
  <label for="name">Name</label>
  <input id="name" name="name" type="text" required>

  <label for="email">Email</label>
  <input id="email" name="email" type="email" required>

  <label for="message">Message</label>
  <textarea id="message" name="message" rows="6"></textarea>

  <button type="submit">Send</button>
</form>
```

If you want to capture messages without a server, use a third‑party form service (Formspree, Netlify Forms) or use `mailto:` for a simple fallback.


## 10. Accessibility & Best Practices

* Always include `alt` for images.
* Use semantic elements and heading order (don't skip `h2` under `h1`).
* Keyboard navigable (links and form controls focusable). Add `:focus` styles in CSS.
* Color contrast — ensure text is readable on background.
* Add `lang` attribute on `<html>`.
* Use `aria-label` or proper `label` elements when needed.

 

## 11. Checklist before launch

* [ ] All pages have `<title>` and meta description
* [ ] Navigation works and highlights current page
* [ ] Images have `alt` text
* [ ] Forms have labels
* [ ] Mobile friendly (viewport set)
* [ ] Basic CSS for layout and focus states
* [ ] Favicon present


