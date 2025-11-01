Perfect 🌟

Welcome to **Phase 16 — “Bootstrap Layout Integration Project: Building a Complete Transflower Store Website”**

Your students have now mastered the building blocks — HTML, CSS, and Bootstrap.
They’ve created forms, components, grids, utilities, and responsive designs.
Now, it’s time to bring *everything together* into one **fully functional static website**:
✨ **Transflower Store — A Modern, Responsive E-Commerce Layout.**

---

## 🧑‍🏫 Mentor Storytelling

### Phase 16: “Bringing It All Together — From Pieces to a Complete Experience”

---

### 🌸 Mentor Begins

**Mentor:**
“When an artist paints, each brushstroke seems small and isolated — until the canvas is complete.

You’ve learned every brushstroke of web design — forms, grids, colors, responsiveness.
Now, we’ll paint the whole picture.

Our goal: build a **complete, multi-page, Bootstrap-based Transflower Store website** that’s beautiful, responsive, and consistent.”

---

## 🎯 Learning Objectives

By the end of this phase, students will:

* Combine all previous Bootstrap concepts into one coherent website
* Design five fully responsive pages
* Reuse components like Navbar, Footer, Cards, and Forms
* Apply consistent styling and theming
* Understand folder structure for maintainability

---

## 🌷 Step 1 — Project Structure

```plaintext
transflower-store/
│
├── index.html
├── catalog.html
├── about.html
├── contact.html
├── register.html
│
├── css/
│   └── style.css
│
├── js/
│   └── app.js
│
└── images/
    ├── banner.jpg
    ├── product1.jpg
    ├── product2.jpg
    ├── product3.jpg
    └── logo.png
```

✅ Each page uses the same **Navbar** and **Footer**
✅ All images stored in `/images`
✅ Custom styles in `/css/style.css`
✅ Optional JavaScript (for form validation, toasts) in `/js/app.js`

---

## 🌹 Step 2 — `index.html` (Home Page)

Purpose: Welcome visitors, showcase hero section, and promote products.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Transflower Store</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css" rel="stylesheet">
  <link rel="stylesheet" href="css/style.css">
</head>
<body>

  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <div class="container">
      <a class="navbar-brand fw-bold" href="#">🌸 Transflower Store</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarMenu">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarMenu">
        <ul class="navbar-nav ms-auto">
          <li class="nav-item"><a class="nav-link active" href="index.html">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="catalog.html">Catalog</a></li>
          <li class="nav-item"><a class="nav-link" href="about.html">About</a></li>
          <li class="nav-item"><a class="nav-link" href="contact.html">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Hero Section -->
  <div class="container-fluid bg-primary text-white text-center py-5">
    <h1 class="display-4 fw-bold">Welcome to Transflower Store 🌸</h1>
    <p class="lead">Where Technology Blooms with Style</p>
    <a href="catalog.html" class="btn btn-light btn-lg mt-3">Shop Now</a>
  </div>

  <!-- Featured Products -->
  <div class="container my-5">
    <h2 class="text-center mb-4">Featured Products</h2>
    <div class="row g-4">
      <div class="col-md-4">
        <div class="card shadow h-100">
          <img src="images/product1.jpg" class="card-img-top" alt="Product 1">
          <div class="card-body text-center">
            <h5 class="card-title">Wireless Earbuds</h5>
            <p>$59.99</p>
            <a href="#" class="btn btn-primary">Buy Now</a>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card shadow h-100">
          <img src="images/product2.jpg" class="card-img-top" alt="Product 2">
          <div class="card-body text-center">
            <h5 class="card-title">Smart Watch</h5>
            <p>$129.99</p>
            <a href="#" class="btn btn-primary">Buy Now</a>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card shadow h-100">
          <img src="images/product3.jpg" class="card-img-top" alt="Product 3">
          <div class="card-body text-center">
            <h5 class="card-title">Bluetooth Speaker</h5>
            <p>$89.99</p>
            <a href="#" class="btn btn-primary">Buy Now</a>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer class="bg-dark text-white text-center py-3 mt-5">
    <small>© 2025 Transflower Store. All Rights Reserved.</small>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

✅ Hero + Product Cards + Consistent Navbar/Footer
✅ Fully responsive design

---

## 🌼 Step 3 — Other Pages

* **catalog.html** → Grid of all products
* **about.html** → Story of Transflower, mission & vision
* **contact.html** → Form + contact info section
* **register.html** → User registration form with Bootstrap validation

Each page reuses:

* The same **Navbar & Footer**
* Bootstrap layout grid
* Custom `style.css` for theme consistency

---

## 🌻 Step 4 — Custom Styling Example (style.css)

```css
body {
  font-family: 'Poppins', sans-serif;
  background-color: #f8f9fa;
}

.card:hover {
  transform: scale(1.03);
  transition: 0.3s ease-in-out;
}

footer {
  font-size: 0.9rem;
}
```

---

## 🌺 Step 5 — Testing Responsiveness

🧩 Use **Chrome DevTools → Device Toolbar**
✅ Check on mobile, tablet, desktop viewports
✅ Ensure navbar collapses correctly
✅ Product grid stacks vertically on small screens

---

## 🌸 Mentor Wrap-Up

**Mentor:**
“You’ve built your first complete website — from concept to completion.
Every button, card, and color choice now has a purpose.

Bootstrap helped you think like a designer *and* a developer — creating user-friendly, responsive, and maintainable layouts.”

> “This project is not just a website — it’s your proof of learning, your first step toward professional web development.”

---

### ✅ Students Learned

| Concept             | Description                    | Example                        |
| ------------------- | ------------------------------ | ------------------------------ |
| Project Integration | Combine all Bootstrap features | Navbar + Hero + Cards + Footer |
| Page Structure      | Organized folder layout        | `/css`, `/js`, `/images`       |
| Reusability         | Shared components              | Navbar/Footer across pages     |
| Styling             | Consistent brand identity      | Custom CSS + Bootstrap         |
| Testing             | Device responsiveness          | DevTools viewport preview      |

