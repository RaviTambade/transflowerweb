

# Phase 4: “From Single Page to Multi-Page — Structuring the Transflower Portal”


### 🌼 Mentor Begins

**Mentor:**
“You’ve built a beautiful, responsive, branded interface using Bootstrap.
But right now, everything lives on a single page.

In the real world, websites grow — they have a home, products, about, and contact pages.
Each page has its own content but shares a consistent *look and feel.*

Today, we’ll learn to **reuse layouts** smartly, just like a professional front-end team.”


## 🎯 Learning Objectives

By the end of this phase, students will:

* Create multiple Bootstrap-based pages (`index.html`, `products.html`, `about.html`, `contact.html`)
* Share a **common header (navbar)** and **footer**
* Maintain consistent styling using the Transflower theme
* Use responsive containers and Bootstrap grid system


## 🏗️ Step 1 — Plan the Site Structure

**Mentor:**
“Before you code, plan your pages — every good developer sketches the blueprint first.”

```
Transflower/
│
├── index.html           → Home / Landing Page
├── products.html        → Product List / Gallery
├── about.html           → About the Company
├── contact.html         → Contact Form
├── css/
│   └── style.css        → Transflower theme overrides
└── images/
    └── (carousel & product images)
```


## 🧩 Step 2 — Create Shared Navbar

Every page begins with the same **Bootstrap navbar** so users can easily navigate.

```html
<!-- Shared Navbar -->
<nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <div class="container">
    <a class="navbar-brand fw-bold" href="index.html">🌸 Transflower</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link" href="index.html">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="products.html">Products</a></li>
        <li class="nav-item"><a class="nav-link" href="about.html">About</a></li>
        <li class="nav-item"><a class="nav-link" href="contact.html">Contact</a></li>
      </ul>
    </div>
  </div>
</nav>
```

> **Mentor Tip:** In professional web apps, this header is made into a *layout component* (in React, Angular, or Razor). But here, we’ll copy it across HTML files to learn the concept.


## 🏠 Step 3 — `index.html` (Home Page)

This is your **landing page** with a carousel banner and short intro.

```html
<section class="mt-4">
  <div id="homeCarousel" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="images/flowers1.jpg" class="d-block w-100" alt="Fresh Flowers">
        <div class="carousel-caption">
          <h5>Welcome to Transflower Store</h5>
          <p>Where Nature Meets Beauty</p>
        </div>
      </div>
      <div class="carousel-item">
        <img src="images/flowers2.jpg" class="d-block w-100" alt="Bouquets">
        <div class="carousel-caption">
          <h5>Fresh Blooms Everyday</h5>
          <p>Delivered with Love and Care</p>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="container text-center my-5">
  <h2>Why Choose Transflower?</h2>
  <p class="lead">We deliver fresh, handpicked flowers that speak your emotions beautifully.</p>
</section>
```


## 🛍️ Step 4 — `products.html` (Product Gallery)

```html
<section class="container my-5">
  <h2 class="text-center mb-4">Our Featured Products</h2>
  <div class="row g-4">
    <div class="col-md-4">
      <div class="card">
        <img src="images/rose.jpg" class="card-img-top" alt="Rose">
        <div class="card-body text-center">
          <h5 class="card-title">Red Rose Bouquet</h5>
          <p class="card-text">Rs. 599</p>
          <a href="#" class="btn btn-primary">Buy Now</a>
        </div>
      </div>
    </div>
    <!-- Repeat 2 more product cards -->
  </div>
</section>
```

🧠 **Concept:** Bootstrap Grid (`.row`, `.col-md-4`) for responsive layout


## 🏢 Step 5 — `about.html`

```html
<section class="container my-5">
  <h2>About Transflower</h2>
  <p>Transflower is India’s favorite online flower shop dedicated to spreading joy through fresh, elegant, and eco-friendly floral arrangements. We started in 2005 with a simple mission — to make every occasion bloom.</p>
</section>
```


## 📞 Step 6 — `contact.html`

```html
<section class="container my-5">
  <h2>Contact Us</h2>
  <form class="mt-4">
    <div class="mb-3">
      <label for="name" class="form-label">Name</label>
      <input type="text" id="name" class="form-control" placeholder="Your Name">
    </div>
    <div class="mb-3">
      <label for="email" class="form-label">Email</label>
      <input type="email" id="email" class="form-control" placeholder="you@example.com">
    </div>
    <div class="mb-3">
      <label for="message" class="form-label">Message</label>
      <textarea id="message" class="form-control" rows="4"></textarea>
    </div>
    <button type="submit" class="btn btn-primary">Send Message</button>
  </form>
</section>
```


## 🧱 Step 7 — Shared Footer

Add this footer to all pages:

```html
<footer class="text-center text-white py-3">
  <p class="mb-0">&copy; 2025 Transflower Store. All Rights Reserved.</p>
</footer>
```


## 🌟 Mentor Wrap-Up

**Mentor:**
“Today you took your Bootstrap knowledge and used it to structure a complete website.
You learned how to maintain consistent UI across multiple pages — something every real-world website requires.”

> “Bootstrap helped us stay *organized, responsive, and brand-aligned.*
> You’ve just built a professional website foundation — from a single responsive page to a full online identity.”


### ✅ Students Learned

| Concept                 | Skill                        | Outcome                  |
| ----------------------- | ---------------------------- | ------------------------ |
| Layout Design           | Shared header/footer         | Consistent navigation    |
| Multi-page Architecture | Linked pages                 | Structured site          |
| Bootstrap Grid          | `.container`, `.row`, `.col` | Responsive product cards |
| Theming                 | Reused custom CSS            | Brand continuity         |


