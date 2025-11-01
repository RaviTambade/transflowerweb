## Building a Responsive Landing Page using Bootstrap


### 🌱 Mentor Begins the Session

**Mentor:**
"Alright everyone, today we’re going to transform our plain HTML + CSS knowledge into something professional — using Bootstrap.
We’ll create a beautiful landing page for our fictional brand — **Transflower Store** 🌼 — where everything adjusts automatically for mobile, tablet, and desktop."


## Step 1️⃣ — Create Project Structure

Let’s start simple.

📁 Folder: `transflower-bootstrap`
Inside it, create:

```
index.html
style.css   (optional for custom overrides)
```

## Step 2️⃣ — Basic HTML Template

**Mentor:**
“Let’s start by setting up a basic HTML skeleton and linking Bootstrap.”

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Transflower Store</title>

  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">

  <!-- Custom CSS (optional) -->
  <link rel="stylesheet" href="style.css">
</head>
<body>
  
  <!-- Content will go here -->

  <!-- Bootstrap JS -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## Step 3️⃣ — Add a Navbar

**Mentor:**
“Every store begins with a strong header — our Navbar. Bootstrap provides ready-made navbars that are responsive out of the box!”

```html
<!-- Navbar -->
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container">
    <a class="navbar-brand fw-bold" href="#">🌼 Transflower Store</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link" href="#">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Products</a></li>
        <li class="nav-item"><a class="nav-link" href="#">About</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Contact</a></li>
      </ul>
    </div>
  </div>
</nav>
```

🧩 **Concept introduced:**

* `navbar-expand-lg` → Expands on large screens
* `navbar-toggler` → Collapsible on small screens
* `bg-dark`, `navbar-dark` → Bootstrap color and theme utilities
* `ms-auto` → Auto margin to push menu to right

## Step 4️⃣ — Add a Hero Section

**Mentor:**
“Now, let’s create the ‘hero area’ — the welcoming banner section that captures attention.”

```html
<!-- Hero Section -->
<section class="bg-light text-center py-5">
  <div class="container">
    <h1 class="display-4 fw-bold">Welcome to Transflower Store</h1>
    <p class="lead">Beautiful flowers, delivered fresh to your doorstep.</p>
    <a href="#" class="btn btn-primary btn-lg mt-3">Shop Now</a>
  </div>
</section>
```

🧠 **Concepts covered:**

* `container` for centered content
* `py-5` → vertical padding
* `display-4`, `lead` → typography utilities
* `btn btn-primary` → predefined button style


## Step 5️⃣ — Add a Responsive Product Grid

**Mentor:**
“Let’s display some sample products. Bootstrap’s **Grid System** helps us create layouts that automatically adjust for all devices.”

```html
<!-- Product Section -->
<section class="py-5">
  <div class="container">
    <h2 class="text-center mb-4">Our Featured Flowers</h2>
    <div class="row">
      <div class="col-md-4 mb-4">
        <div class="card">
          <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="Flower">
          <div class="card-body text-center">
            <h5 class="card-title">Red Roses</h5>
            <p class="card-text">Elegant bouquet for special moments.</p>
            <a href="#" class="btn btn-outline-primary">Buy Now</a>
          </div>
        </div>
      </div>

      <div class="col-md-4 mb-4">
        <div class="card">
          <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="Flower">
          <div class="card-body text-center">
            <h5 class="card-title">Tulip Delight</h5>
            <p class="card-text">Fresh tulips to brighten your day.</p>
            <a href="#" class="btn btn-outline-primary">Buy Now</a>
          </div>
        </div>
      </div>

      <div class="col-md-4 mb-4">
        <div class="card">
          <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="Flower">
          <div class="card-body text-center">
            <h5 class="card-title">Sunflower Joy</h5>
            <p class="card-text">Bring sunshine into your home.</p>
            <a href="#" class="btn btn-outline-primary">Buy Now</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

🧩 **Concept introduced:**

* `row` and `col-md-4` → divide layout into 3 equal columns on medium+ screens, stack on mobile
* `card` → Bootstrap component for product display
* Responsive images adjust automatically


## Step 6️⃣ — Footer

```html
<!-- Footer -->
<footer class="bg-dark text-white text-center py-3">
  <p class="mb-0">&copy; 2025 Transflower Store. All rights reserved.</p>
</footer>
```

## 🌐 Step 7️⃣ — Test Responsiveness

**Mentor:**
“Now comes the fun part!
Open your `index.html` in a browser and resize the window —
watch how the navbar collapses into a toggle, how products stack vertically, and how spacing adapts automatically.”


### 🧭 Mentor Wrap-up

> “See how fast we built a professional, mobile-friendly website without writing complex CSS?
> That’s the power of **Bootstrap** — it handles the responsiveness for you.
> As developers, your job becomes focusing on **content and logic**, not repetitive styling work.”

 