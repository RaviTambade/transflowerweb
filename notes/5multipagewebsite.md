
# **Phase 4 — Building a Multi-Page Transflower Website using Bootstrap**

### Theme: “Scaling from One Page to a Complete Website Layout”


### 🌼 Mentor Begins

**Mentor:**
“Team, we’ve come a long way. You’ve built a **beautiful, responsive, and branded landing page** for *Transflower Store*.

Now, it’s time to grow beyond a single page — just like a real business expands its branches.

We’ll organize our site into **multiple pages**, each with its own purpose, but all sharing the same **Navbar, Footer, and Theme**.
That’s what real-world developers do — they build a **consistent user experience** across all pages.”


## 🌐 Website Structure

**Mentor draws on board:**

```
transflower-website/
│
├── index.html           → Home page
├── products.html        → Product listing
├── about.html           → About company
├── contact.html         → Contact form
├── style.css            → Common theme
└── /images/             → Logo, product pictures
```


## Step 1️⃣ — Create the Common Header (Navbar)

Let’s reuse the **same navbar** across all pages for consistency.

```html
<!-- Navbar -->
<nav class="navbar navbar-expand-lg navbar-dark" style="background-color: var(--bs-primary);">
  <div class="container">
    <a class="navbar-brand fw-bold" href="index.html">🌼 Transflower</a>
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

🧩 **Concept introduced:**

* Shared navigation layout — same across all pages
* Helps users feel orientation and consistency


## Step 2️⃣ — Shared Footer

Create a `footer.html` section and reuse it on all pages (for now, copy-paste manually; later, students can learn templating).

```html
<footer class="text-center text-white py-3" style="background-color: var(--bs-secondary);">
  <p class="mb-0">&copy; 2025 Transflower Store | Designed with 💗 using Bootstrap</p>
</footer>
```

## Step 3️⃣ — Home Page (`index.html`)

This is your main landing page — the one we already created with Carousel + Featured Products.

Simplify it for now:

```html
<section class="text-center py-5 bg-light">
  <div class="container">
    <h1 class="fw-bold">Welcome to Transflower Store</h1>
    <p class="lead">Nature-inspired beauty delivered fresh every day.</p>
    <a href="products.html" class="btn btn-primary btn-lg mt-3">Explore Flowers</a>
  </div>
</section>
```

## Step 4️⃣ — Products Page (`products.html`)

**Mentor:**
“This page lists all our products in a responsive grid. Notice how easy it is to reuse our Bootstrap card layout!”

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Transflower - Products</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <!-- Include Navbar -->
  <!-- Copy from index.html -->

  <section class="py-5">
    <div class="container">
      <h2 class="text-center mb-5">Our Products</h2>
      <div class="row g-4">
        <div class="col-md-4">
          <div class="card h-100">
            <img src="images/redrose.jpg" class="card-img-top" alt="Red Roses">
            <div class="card-body text-center">
              <h5 class="card-title">Red Roses</h5>
              <p>₹499 | Elegant bouquet for special moments</p>
              <a href="#" class="btn btn-outline-primary">Buy Now</a>
            </div>
          </div>
        </div>

        <div class="col-md-4">
          <div class="card h-100">
            <img src="images/tulip.jpg" class="card-img-top" alt="Tulip Delight">
            <div class="card-body text-center">
              <h5 class="card-title">Tulip Delight</h5>
              <p>₹399 | Fresh tulips to brighten your day</p>
              <a href="#" class="btn btn-outline-primary">Buy Now</a>
            </div>
          </div>
        </div>

        <div class="col-md-4">
          <div class="card h-100">
            <img src="images/sunflower.jpg" class="card-img-top" alt="Sunflower Joy">
            <div class="card-body text-center">
              <h5 class="card-title">Sunflower Joy</h5>
              <p>₹299 | Bring sunshine into your home</p>
              <a href="#" class="btn btn-outline-primary">Buy Now</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <!-- Copy from index.html -->

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## Step 5️⃣ — About Page (`about.html`)

**Mentor:**
“Every brand needs a story. Let’s use Bootstrap’s grid to make an elegant About section.”

```html
<section class="py-5">
  <div class="container">
    <div class="row align-items-center">
      <div class="col-md-6">
        <img src="images/team.jpg" class="img-fluid rounded" alt="Our Team">
      </div>
      <div class="col-md-6">
        <h2>About Transflower Store</h2>
        <p>Founded in 2020, Transflower Store started with a simple dream — to make the world a little happier with flowers. Our team of florists handpick fresh blooms from local farms and deliver them with love.</p>
        <p>We believe flowers speak a universal language — of emotions, of connections, of beauty. Each bouquet we deliver is crafted with care and purpose.</p>
      </div>
    </div>
  </div>
</section>
```

🧠 **Concept introduced:**

* Responsive image + text alignment using Bootstrap grid
* Professional storytelling through layout


## Step 6️⃣ — Contact Page (`contact.html`)

**Mentor:**
“This page invites users to reach out. Let’s reuse the modal form idea as a full-page contact form.”

```html
<section class="py-5 bg-light">
  <div class="container">
    <h2 class="text-center mb-4">Get in Touch</h2>
    <div class="row justify-content-center">
      <div class="col-md-6">
        <form>
          <div class="mb-3">
            <label class="form-label">Your Name</label>
            <input type="text" class="form-control" placeholder="Enter your name">
          </div>
          <div class="mb-3">
            <label class="form-label">Email</label>
            <input type="email" class="form-control" placeholder="Enter your email">
          </div>
          <div class="mb-3">
            <label class="form-label">Message</label>
            <textarea class="form-control" rows="4" placeholder="Write your message"></textarea>
          </div>
          <button class="btn btn-primary w-100">Send Message</button>
        </form>
      </div>
    </div>
  </div>
</section>
```

## Step 7️⃣ — Add Active Link Highlighting

In `style.css`, add:

```css
.nav-link.active {
  color: var(--bs-warning) !important;
  font-weight: 600;
}
```

Then manually mark the current page link as active:

```html
<li class="nav-item"><a class="nav-link active" href="products.html">Products</a></li>
```

## 🧭 Mentor Wrap-Up

**Mentor:**
“Now your Transflower website isn’t just one static page — it’s a **mini ecosystem** of connected pages with shared design, brand colors, and consistent layout.

This is how real-world web projects evolve —
➡️ from static to responsive
➡️ from single-page to multi-page
➡️ from template to branded website.”


### ✅ Summary of Concepts Learned

| Concept          | Description                           |
| ---------------- | ------------------------------------- |
| Shared Layout    | Navbar and footer reused across pages |
| Responsive Grid  | Consistent structure across devices   |
| Themed Pages     | Brand consistency maintained          |
| Navigation Links | Routing between static pages          |
| User Experience  | Storytelling through design           |

 