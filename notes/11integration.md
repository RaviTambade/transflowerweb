

## Phase 9: “From Pieces to Perfection — Building the Transflower Store Landing Page”



### 🌼 Mentor Begins

**Mentor:**
“You’ve learned how to build beautiful sections — carousels, cards, and forms.
Now it’s time to assemble them like petals into a complete bouquet — your **Transflower Store** landing page.

This is where your project becomes more than just a demo — it becomes a real, working mini website.

Let’s see how every Bootstrap component you’ve learned fits together harmoniously.”


## 🎯 Learning Objectives

By the end of this phase, students will:

* Build a complete responsive **landing page** using Bootstrap
* Combine **Navbar, Hero Section, Product Cards, Testimonials, and Footer**
* Learn the **flow of sections** in modern web design
* Practice **consistency, responsiveness, and UI hierarchy**


## 🌷 Step 1 — Setup the Base Structure

Create a file: `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Transflower Store 🌼</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>
<body>
```


## 🌸 Step 2 — Navbar

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light shadow-sm">
  <div class="container">
    <a class="navbar-brand fw-bold text-danger" href="#">🌼 Transflower</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link active" href="#">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Products</a></li>
        <li class="nav-item"><a class="nav-link" href="#">About</a></li>
        <li class="nav-item"><a class="nav-link" href="#">Contact</a></li>
        <li class="nav-item"><a class="btn btn-danger ms-2" href="#">Login</a></li>
      </ul>
    </div>
  </div>
</nav>
```

🧠 **Concepts applied:**

* `.navbar-expand-lg` makes the menu collapsible on small screens
* `.ms-auto` aligns menu items to the right
* `.navbar-toggler` handles mobile menu



## 🌼 Step 3 — Hero Section

```html
<header class="bg-light py-5">
  <div class="container d-flex flex-column flex-md-row align-items-center justify-content-between">
    <div class="text-center text-md-start">
      <h1 class="fw-bold text-danger">Fresh Flowers, Fresh Smiles 🌸</h1>
      <p class="lead text-muted">Delivering happiness across India — every bouquet tells a story.</p>
      <a href="#" class="btn btn-danger btn-lg mt-3">Shop Now</a>
    </div>
    <div class="mt-4 mt-md-0">
      <img src="images/hero.jpg" class="img-fluid rounded-4 shadow" alt="Flower Banner">
    </div>
  </div>
</header>
```

🧠 Uses:

* Flexbox layout for text + image
* `.img-fluid` ensures full responsiveness
* Perfectly adapts from desktop to mobile


## 🌺 Step 4 — Product Gallery (Cards + Grid)

```html
<section class="container my-5">
  <h2 class="text-center mb-4 text-danger">Our Bestselling Bouquets</h2>
  <div class="row g-4">
    <div class="col-12 col-md-6 col-lg-3">
      <div class="card h-100 shadow-sm">
        <img src="images/rose.jpg" class="card-img-top" alt="Red Roses">
        <div class="card-body text-center">
          <h5 class="fw-bold">Red Roses</h5>
          <p>Rs. 599</p>
          <button class="btn btn-outline-danger">Buy Now</button>
        </div>
      </div>
    </div>
    <div class="col-12 col-md-6 col-lg-3">
      <div class="card h-100 shadow-sm">
        <img src="images/tulip.jpg" class="card-img-top" alt="Tulips">
        <div class="card-body text-center">
          <h5 class="fw-bold">Yellow Tulips</h5>
          <p>Rs. 699</p>
          <button class="btn btn-outline-danger">Buy Now</button>
        </div>
      </div>
    </div>
    <div class="col-12 col-md-6 col-lg-3">
      <div class="card h-100 shadow-sm">
        <img src="images/orchid.jpg" class="card-img-top" alt="Orchids">
        <div class="card-body text-center">
          <h5 class="fw-bold">White Orchids</h5>
          <p>Rs. 799</p>
          <button class="btn btn-outline-danger">Buy Now</button>
        </div>
      </div>
    </div>
    <div class="col-12 col-md-6 col-lg-3">
      <div class="card h-100 shadow-sm">
        <img src="images/lily.jpg" class="card-img-top" alt="Lilies">
        <div class="card-body text-center">
          <h5 class="fw-bold">Pink Lilies</h5>
          <p>Rs. 749</p>
          <button class="btn btn-outline-danger">Buy Now</button>
        </div>
      </div>
    </div>
  </div>
</section>
```

🧠 **Concepts integrated:**

* Grid system (`.row`, `.col-*`)
* Cards with `.h-100` for uniformity
* Buttons styled with `.btn-outline-danger`


## 🌼 Step 5 — Testimonials (Carousel)

```html
<section class="bg-light py-5">
  <div class="container">
    <h2 class="text-center text-danger mb-4">What Our Customers Say 💬</h2>
    <div id="testimonialCarousel" class="carousel slide" data-bs-ride="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active text-center">
          <blockquote class="blockquote">
            <p class="mb-4">"Transflower made my day special with fresh roses!"</p>
            <footer class="blockquote-footer">Sneha Kulkarni</footer>
          </blockquote>
        </div>
        <div class="carousel-item text-center">
          <blockquote class="blockquote">
            <p class="mb-4">"Fast delivery and stunning arrangements!"</p>
            <footer class="blockquote-footer">Rahul Mehta</footer>
          </blockquote>
        </div>
      </div>
      <button class="carousel-control-prev" type="button" data-bs-target="#testimonialCarousel" data-bs-slide="prev">
        <span class="carousel-control-prev-icon"></span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#testimonialCarousel" data-bs-slide="next">
        <span class="carousel-control-next-icon"></span>
      </button>
    </div>
  </div>
</section>
```


## 🌻 Step 6 — Footer

```html
<footer class="bg-dark text-light py-4 mt-5">
  <div class="container text-center">
    <p class="mb-1">© 2025 Transflower Store. All rights reserved.</p>
    <p class="mb-0">Follow us on 
      <a href="#" class="text-danger text-decoration-none">Instagram</a> | 
      <a href="#" class="text-danger text-decoration-none">Facebook</a>
    </p>
  </div>
</footer>
```

## 🌿 Step 7 — Close HTML

```html
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

## 💄 Step 8 — Add Some Custom CSS (style.css)

```css
body {
  font-family: 'Poppins', sans-serif;
}

h1, h2 {
  font-weight: bold;
}

.card img {
  height: 200px;
  object-fit: cover;
}

footer a:hover {
  text-decoration: underline;
}
```

## 🌟 Mentor Wrap-Up

**Mentor:**
“Congratulations! You’ve just built a complete **responsive Bootstrap website** — from navbar to footer.
This is what professionals do: they design *modular sections*, test responsiveness, and ensure the UI feels natural on every device.

Each Bootstrap feature you learned has now found its real-world purpose.”

> “Good UI is not built in one go — it’s assembled piece by piece, like a bouquet.”


### ✅ Students Learned

| Concept       | Description               | Example                          |
| ------------- | ------------------------- | -------------------------------- |
| Navbar        | Responsive navigation     | `.navbar-expand-lg`, `.collapse` |
| Hero Section  | Intro with image/text     | Flex + Grid combo                |
| Product Cards | Grid layout for products  | `.col-md-6`, `.col-lg-3`         |
| Carousel      | Auto-sliding testimonials | `.carousel-item`                 |
| Footer        | Consistent site ending    | `.bg-dark`, `.text-light`        |

