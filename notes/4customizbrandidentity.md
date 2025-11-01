

## Phase 3 : “Making Bootstrap Your Own — Creating the Transflower Theme”


### 🌼 Mentor Begins

**Mentor:**
“You’ve mastered responsiveness and interactivity — congratulations!
But here’s a truth about professional front-end work:
**No company ships a default Bootstrap theme.**

Every brand has its own colors, fonts, and feel.
Your job as a developer is to take Bootstrap’s solid foundation and **dress it in your brand’s identity**.

So today, we’ll turn our site from *Bootstrap Blue* to *Transflower Blossom.* 🌸”



## Step 1️⃣ — Decide Brand Colors and Fonts

Let’s pick a **simple, natural color palette** for *Transflower Store*:

| Purpose   | Color                 | Example   |
| --------- | --------------------- | --------- |
| Primary   | Blossom Pink          | `#e91e63` |
| Secondary | Leaf Green            | `#4caf50` |
| Accent    | Sunshine Yellow       | `#ffeb3b` |
| Font      | “Poppins”, sans-serif |           |


### Add Google Font and Custom CSS

In the `<head>` of `index.html`, just above `style.css`:

```html
<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
```

Then open `style.css` and start customizing:

```css
/* ===== Transflower Theme ===== */
body {
  font-family: "Poppins", sans-serif;
}

/* Override Bootstrap colors */
:root {
  --bs-primary: #e91e63;       /* blossom pink */
  --bs-secondary: #4caf50;     /* leaf green */
  --bs-warning: #ffeb3b;       /* sunshine yellow */
}

/* Navbar tweak */
.navbar {
  background-color: var(--bs-primary) !important;
}
.navbar .nav-link {
  color: #fff !important;
  font-weight: 500;
}
.navbar .nav-link:hover {
  color: var(--bs-warning) !important;
}

/* Buttons */
.btn-primary {
  background-color: var(--bs-primary);
  border-color: var(--bs-primary);
}
.btn-primary:hover {
  background-color: #c2185b;
  border-color: #c2185b;
}

/* Cards */
.card {
  border: none;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  border-radius: 10px;
}

/* Footer */
footer {
  background-color: var(--bs-secondary);
}
```

🧩 **Concept introduced:**

* Using CSS Variables (`--bs-primary`) to override Bootstrap theme colors
* Keeping brand consistency across components


## Step 2️⃣ — Add a Themed Background

Let’s make our **hero/carousel captions** more visually consistent.

```css
.carousel-caption h5,
.carousel-caption p {
  background-color: rgba(233, 30, 99, 0.6); /* translucent pink */
  padding: 10px;
  border-radius: 8px;
}
```

This ensures your text remains readable regardless of the slide’s brightness.


## Step 3️⃣ — Add Custom Hover Effects

“Small animations delight users — let’s make cards and buttons feel alive!”

```css
.card:hover {
  transform: scale(1.03);
  transition: 0.3s ease-in-out;
}
.btn-outline-primary:hover {
  background-color: var(--bs-primary);
  color: #fff;
  border-color: var(--bs-primary);
}
```

🧠 **Concept:** subtle transitions create perceived quality — they show attention to detail.

## Step 4️⃣ — Customize Spacing & Containers

Bootstrap’s default spacing is good, but sometimes we need tighter or wider sections.

```css
section {
  padding-top: 60px;
  padding-bottom: 60px;
}
```

---

## Step 5️⃣ — Theme Testing

**Mentor:**
“Now, reload your page.
Notice the pink navbar, the soft shadows on product cards, the elegant hover zooms.

You’ve just branded your Bootstrap project — without breaking its responsiveness.”


### 🌟 Mentor Wrap-Up

> “Bootstrap gives structure; **your design language** gives emotion.
> When you override variables and styles thoughtfully, you’re no longer a coder — you’re a creator.
> This is how startups and companies craft unique visual identities using Bootstrap as their base.”


### ✅ What Students Learned

| Skill Area    | Concept                        | Outcome                 |
| ------------- | ------------------------------ | ----------------------- |
| Design System | Bootstrap variable overrides   | Custom brand colors     |
| Typography    | Google Fonts integration       | Consistent, modern look |
| UX Detail     | Hover & Transition Effects     | Interactive feedback    |
| Customization | CSS variables + utility tuning | Personalized theme      |

