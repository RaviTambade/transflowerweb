Excellent 🌟

Welcome to **Phase 17 — “Bootstrap Cards & Media Components: Building Interactive Content Sections”**

Your students can now design responsive layouts, forms, and navigation bars.
Now it’s time to teach them how to present **content attractively** — product listings, user profiles, blog posts, or course summaries — using **Bootstrap Cards and Media components**.

---

## 🧑‍🏫 Mentor Storytelling

### Phase 17: “Telling Stories with Cards — The Building Blocks of Modern UI”

---

### 🌸 Mentor Begins

**Mentor:**
“Have you ever scrolled through an online store like Amazon or Flipkart?
What’s common across all those pages?

Products, arranged neatly in little boxes — each with an image, name, price, and button.
Those boxes are not random. They’re called **Cards** — self-contained content blocks that make your UI modular, reusable, and visually consistent.”

---

## 🎯 Learning Objectives

By the end of this phase, students will:

* Understand the purpose and structure of **Bootstrap Cards**
* Use **media objects** for image-text layouts
* Combine cards in grids, decks, and carousels
* Design an elegant **Product Catalog section**
* Add interactivity and responsiveness to content sections

---

## 🌷 Step 1 — What Is a Bootstrap Card?

A **Card** is a flexible, content container with options for images, headers, footers, and buttons.
It replaces the old, rigid HTML tables with modern, mobile-first design.

---

### Example: Simple Card

```html
<div class="card" style="width: 18rem;">
  <img src="images/watch.jpg" class="card-img-top" alt="Smart Watch">
  <div class="card-body">
    <h5 class="card-title">Smart Watch</h5>
    <p class="card-text">Track your health, steps, and notifications with style.</p>
    <a href="#" class="btn btn-primary">Buy Now</a>
  </div>
</div>
```

✅ Contains: image, title, text, and button
✅ Automatically adjusts for small screens

---

## 🌸 Step 2 — Adding Card Variations

Bootstrap lets you enhance cards with additional components:

| Feature       | Class                      | Example                                                |
| ------------- | -------------------------- | ------------------------------------------------------ |
| Header        | `card-header`              | `<div class="card-header">Featured</div>`              |
| Footer        | `card-footer`              | `<div class="card-footer text-muted">2 days ago</div>` |
| Image Overlay | `card-img-overlay`         | Use text over an image                                 |
| Background    | `bg-primary`, `text-white` | Stylish color cards                                    |

Example:

```html
<div class="card text-bg-dark">
  <img src="images/laptop.jpg" class="card-img" alt="Laptop">
  <div class="card-img-overlay">
    <h5 class="card-title">Powerful Laptops</h5>
    <p class="card-text">Now with Intel i9 processors and 16GB RAM.</p>
  </div>
</div>
```

---

## 🌺 Step 3 — Card Layouts: Grouping & Grids

You can create multiple cards in a row using **Card Groups** or **Grid System**.

### 🧩 Card Group

```html
<div class="card-group">
  <div class="card">
    <img src="images/phone.jpg" class="card-img-top" alt="Phone">
    <div class="card-body">
      <h5 class="card-title">Smartphone</h5>
      <p class="card-text">Sleek design with 5G performance.</p>
    </div>
  </div>

  <div class="card">
    <img src="images/headphones.jpg" class="card-img-top" alt="Headphones">
    <div class="card-body">
      <h5 class="card-title">Wireless Headphones</h5>
      <p class="card-text">Noise-canceling sound experience.</p>
    </div>
  </div>
</div>
```

✅ Equal height
✅ Seamless alignment

---

### 🌼 Grid Layout

```html
<div class="container mt-5">
  <div class="row">
    <div class="col-md-4 mb-4">
      <div class="card shadow-sm">
        <img src="images/camera.jpg" class="card-img-top" alt="Camera">
        <div class="card-body text-center">
          <h5 class="card-title">Digital Camera</h5>
          <p class="card-text">$399.00</p>
          <button class="btn btn-outline-primary">View Details</button>
        </div>
      </div>
    </div>

    <div class="col-md-4 mb-4">
      <div class="card shadow-sm">
        <img src="images/laptop.jpg" class="card-img-top" alt="Laptop">
        <div class="card-body text-center">
          <h5 class="card-title">Laptop</h5>
          <p class="card-text">$899.00</p>
          <button class="btn btn-outline-primary">View Details</button>
        </div>
      </div>
    </div>
  </div>
</div>
```

✅ Perfect for product grids or team profiles

---

## 🌻 Step 4 — Media Object (Image + Text Alignment)

Media objects are used for aligning images beside text — great for blogs, testimonials, or chat messages.

```html
<div class="d-flex align-items-center border p-3 rounded shadow-sm">
  <img src="images/user.jpg" class="rounded-circle me-3" width="80" height="80" alt="User">
  <div>
    <h6 class="fw-bold mb-1">Ravi Tambade</h6>
    <p class="mb-0 text-muted">Mentorship is not about teaching, it’s about awakening curiosity.</p>
  </div>
</div>
```

---

## 🌷 Step 5 — Mini Hands-on: Product Catalog Section

```html
<div class="container py-5">
  <h2 class="text-center mb-4 text-primary">Popular Products</h2>
  <div class="row row-cols-1 row-cols-md-3 g-4">
    <div class="col">
      <div class="card h-100 shadow">
        <img src="images/phone.jpg" class="card-img-top" alt="Phone">
        <div class="card-body text-center">
          <h5 class="card-title">Smartphone</h5>
          <p class="card-text">Latest Android model with AI camera.</p>
          <button class="btn btn-primary">Buy Now</button>
        </div>
      </div>
    </div>

    <div class="col">
      <div class="card h-100 shadow">
        <img src="images/watch.jpg" class="card-img-top" alt="Watch">
        <div class="card-body text-center">
          <h5 class="card-title">Smart Watch</h5>
          <p class="card-text">Fitness tracking with heart-rate monitor.</p>
          <button class="btn btn-primary">Buy Now</button>
        </div>
      </div>
    </div>
  </div>
</div>
```

---

## 🌸 Mentor Wrap-Up

**Mentor:**
“Cards help you structure information so users can browse easily.
They’re the ‘product displays’ of the digital world — consistent, elegant, and reusable.”

> “In UI design, good presentation is silent persuasion — and cards are the quiet salespeople of your web page.”

---

### ✅ Students Learned

| Concept        | Description         | Example                            |
| -------------- | ------------------- | ---------------------------------- |
| Card Structure | Image, Body, Footer | `card`, `card-body`, `card-footer` |
| Layouts        | Group, Deck, Grid   | `card-group`, `row-cols-3`         |
| Media Object   | Image beside text   | `d-flex align-items-center`        |
| Hands-on       | Product Catalog     | Real-world mini project            |

 