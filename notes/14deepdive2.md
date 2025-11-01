

## 🧑‍🏫 Mentor Storytelling

### Phase 12: “Designing the Storefront — Where Users Explore, Discover, and Engage”

---

### 🌸 Mentor Begins

**Mentor:**
“Every online store begins with a first impression — that’s your **home page**.
Before users click *Buy Now*, they must *feel* they’re in the right place.

Bootstrap helps you design that welcoming experience —
a clean navigation bar, an elegant carousel to showcase offers, and product cards that look professional on any device.

Let’s now build the **Transflower Store Front Page** step by step.”

---

## 🎯 Learning Objectives

By the end of this phase, students will be able to:

* Build a **Navbar** with links, dropdowns, and a responsive toggle
* Create a **Carousel** to showcase product banners or promotions
* Display products using **Cards** and **Grid layout**
* Organize content using **Tabs and Navs**
* Build a complete **responsive storefront landing page**

---

## 🌼 Step 1 — Setting Up the Page

Create a file: `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Transflower Store</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

<!-- Navbar Section -->
<nav class="navbar navbar-expand-lg navbar-dark bg-danger">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">🌸 Transflower Store</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Products</a></li>
        <li class="nav-item"><a class="nav-link" href="#">About Us</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Contact</a></li>
        <li class="nav-item"><a class="nav-link" href="login.html">Login</a></li>
      </ul>
    </div>
  </div>
</nav>
```

✅ **Concepts introduced:**

* `.navbar`, `.navbar-expand-lg` for responsive navigation
* `.navbar-dark` with `bg-danger` for color theme
* `.navbar-toggler` for collapsing on mobile

---

## 🌹 Step 2 — Bootstrap Carousel (Hero Section)

Add this below your navbar:

```html
<div id="storeCarousel" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="images/banner1.jpg" class="d-block w-100" alt="Fresh Flowers">
      <div class="carousel-caption bg-dark bg-opacity-50 rounded p-2">
        <h3>Fresh Flowers Everyday</h3>
        <p>Bringing Nature to Your Doorstep</p>
      </div>
    </div>
    <div class="carousel-item">
      <img src="images/banner2.jpg" class="d-block w-100" alt="Gifts and Hampers">
      <div class="carousel-caption bg-dark bg-opacity-50 rounded p-2">
        <h3>Gifts & Hampers</h3>
        <p>Perfect for Every Occasion</p>
      </div>
    </div>
  </div>

  <button class="carousel-control-prev" type="button" data-bs-target="#storeCarousel" data-bs-slide="prev">
    <span class="carousel-control-prev-icon"></span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#storeCarousel" data-bs-slide="next">
    <span class="carousel-control-next-icon"></span>
  </button>
</div>
```

✅ **Concepts introduced:**

* `.carousel-item` for each slide
* `.carousel-caption` for overlay text
* `.carousel-control-prev` / `.carousel-control-next` for navigation

---

## 🌷 Step 3 — Product Cards (Showcase Section)

```html
<div class="container my-5">
  <h2 class="text-center mb-4">🌼 Featured Products</h2>
  <div class="row row-cols-1 row-cols-md-3 g-4">
    <div class="col">
      <div class="card shadow-sm">
        <img src="images/rose.jpg" class="card-img-top" alt="Rose Bouquet">
        <div class="card-body">
          <h5 class="card-title">Rose Bouquet</h5>
          <p class="card-text">A timeless symbol of love and affection.</p>
          <button class="btn btn-danger w-100">Buy Now</button>
        </div>
      </div>
    </div>
    <div class="col">
      <div class="card shadow-sm">
        <img src="images/lily.jpg" class="card-img-top" alt="Lily Bouquet">
        <div class="card-body">
          <h5 class="card-title">Lily Bouquet</h5>
          <p class="card-text">Elegant white lilies for special moments.</p>
          <button class="btn btn-danger w-100">Buy Now</button>
        </div>
      </div>
    </div>
    <div class="col">
      <div class="card shadow-sm">
        <img src="images/tulip.jpg" class="card-img-top" alt="Tulip Bouquet">
        <div class="card-body">
          <h5 class="card-title">Tulip Bouquet</h5>
          <p class="card-text">Brighten someone’s day with colorful tulips.</p>
          <button class="btn btn-danger w-100">Buy Now</button>
        </div>
      </div>
    </div>
  </div>
</div>
```

✅ **Concepts introduced:**

* `.card` component for product display
* `.row-cols-md-3` for auto-responsive columns
* `.shadow-sm` and `btn-danger` for consistent branding

---

## 🌺 Step 4 — Tabs for Product Categories

```html
<div class="container my-5">
  <ul class="nav nav-tabs" id="categoryTabs" role="tablist">
    <li class="nav-item"><button class="nav-link active" data-bs-toggle="tab" data-bs-target="#flowers">Flowers</button></li>
    <li class="nav-item"><button class="nav-link" data-bs-toggle="tab" data-bs-target="#gifts">Gifts</button></li>
    <li class="nav-item"><button class="nav-link" data-bs-toggle="tab" data-bs-target="#plants">Plants</button></li>
  </ul>

  <div class="tab-content p-3 border border-top-0">
    <div class="tab-pane fade show active" id="flowers">
      <p>Explore our vibrant collection of fresh flowers.</p>
    </div>
    <div class="tab-pane fade" id="gifts">
      <p>Unique gifts for birthdays, weddings, and more.</p>
    </div>
    <div class="tab-pane fade" id="plants">
      <p>Indoor and outdoor plants to bring freshness home.</p>
    </div>
  </div>
</div>
```

✅ **Concepts introduced:**

* `.nav-tabs` and `.tab-content` for organizing multiple sections
* Controlled through `data-bs-toggle="tab"`

---

## 🌻 Step 5 — Footer

```html
<footer class="bg-danger text-white text-center p-3">
  <p>&copy; 2025 Transflower Store. All rights reserved.</p>
</footer>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

✅ Adds closure and professionalism to the page.

---

## 🌸 Mentor Wrap-Up

**Mentor:**
“Now your store feels alive — with navigation, imagery, and elegant presentation.
Bootstrap gave you building blocks; your creativity turned them into a digital experience.

This is how front-end developers craft *user journeys* — from browsing to believing.”

> “Design is not decoration. It’s communication through clarity and emotion.”

---

### ✅ Students Learned

| Component   | Purpose                    | Example                     |
| ----------- | -------------------------- | --------------------------- |
| Navbar      | Top navigation             | `.navbar`, `.navbar-brand`  |
| Carousel    | Image sliders              | `.carousel-item`            |
| Cards       | Product layouts            | `.card`, `.card-body`       |
| Tabs        | Organized content sections | `.nav-tabs`, `.tab-pane`    |
| Grid System | Responsive arrangement     | `.row-cols-md-3`            |
| Footer      | Consistent branding        | `.bg-danger`, `.text-white` |

 