Perfect 🌟

Welcome to **Phase 13 — “Integrating All Pages into a Complete Bootstrap Website Layout”**

Your students have now mastered individual Bootstrap components — Navbar, Carousel, Cards, Tabs, and Forms.
Now, we’ll bring everything together into a **cohesive, multi-page responsive website**:
the **Transflower Store Portal** 🌸

---

## 🧑‍🏫 Mentor Storytelling

### Phase 13: “From Pages to a Portal — Building a Seamless Web Experience”

---

### 🌸 Mentor Begins

**Mentor:**
“Developing a single beautiful page is good — but building a *consistent experience* across multiple pages is great.

When users navigate your site, they should feel they are inside the same digital world —
same colors, same layout, same spirit.

Let’s now connect all our pages — Home, About Us, Contact, Register, and Login — into one Bootstrap-based portal.

We’ll make our store *feel whole*.”

---

## 🎯 Learning Objectives

By the end of this phase, students will:

* Reuse common components (Navbar, Footer) across multiple pages
* Maintain consistent styling and layout
* Link pages using anchor tags and Bootstrap navigation
* Test full responsiveness across all pages
* Understand the structure of a complete website

---

## 🌷 Folder Structure

```
transflower-store/
│
├── index.html              → Home page
├── about.html              → About Us page
├── contact.html            → Contact page
├── register.html           → Customer registration form
├── login.html              → Login form
│
├── css/
│   └── style.css           → Custom styles
├── images/                 → Banners & product images
└── js/
    └── app.js              → Optional scripts
```

---

## 🌹 Step 1 — Common Navbar (used in all pages)

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-danger">
  <div class="container">
    <a class="navbar-brand" href="index.html">🌸 Transflower Store</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link" href="index.html">Home</a></li>
        <li class="nav-item"><a class="nav-link" href="about.html">About</a></li>
        <li class="nav-item"><a class="nav-link" href="contact.html">Contact</a></li>
        <li class="nav-item"><a class="nav-link" href="register.html">Register</a></li>
        <li class="nav-item"><a class="nav-link" href="login.html">Login</a></li>
      </ul>
    </div>
  </div>
</nav>
```

✅ Same navbar included on every page ensures **uniform navigation**.

---

## 🌼 Step 2 — Home Page (index.html)

Re-use content from **Phase 12** (Navbar, Carousel, Product Cards, Tabs, Footer).
Make sure all navigation links point to real pages.

```html
<a class="btn btn-outline-light" href="register.html">Start Shopping</a>
```

✅ Test by clicking through links to navigate between pages.

---

## 🌸 Step 3 — About Us Page (about.html)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>About Us - Transflower Store</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

<!-- Include Navbar -->
<nav class="navbar navbar-expand-lg navbar-dark bg-danger"> ... </nav>

<div class="container my-5">
  <h2 class="text-center text-danger mb-4">About Transflower Store</h2>
  <div class="row align-items-center">
    <div class="col-md-6">
      <img src="images/about.jpg" class="img-fluid rounded shadow" alt="About Transflower">
    </div>
    <div class="col-md-6">
      <p>
        Transflower Store is a leading online flower and gift retailer known for creativity and quality. 
        We believe in spreading joy through nature’s beauty.
      </p>
      <p>
        Founded in 2020, we have delivered happiness to over 10,000 customers across India.
        Every bouquet, plant, or hamper is handpicked with love.
      </p>
    </div>
  </div>
</div>

<footer class="bg-danger text-white text-center p-3">
  &copy; 2025 Transflower Store. All Rights Reserved.
</footer>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

✅ Introduces storytelling and company presentation.

---

## 🌹 Step 4 — Contact Page (contact.html)

```html
<div class="container my-5">
  <h2 class="text-center text-danger mb-4">Contact Us</h2>
  <div class="row justify-content-center">
    <div class="col-md-6">
      <form>
        <div class="mb-3">
          <label class="form-label">Full Name</label>
          <input type="text" class="form-control" required>
        </div>
        <div class="mb-3">
          <label class="form-label">Email</label>
          <input type="email" class="form-control" required>
        </div>
        <div class="mb-3">
          <label class="form-label">Message</label>
          <textarea class="form-control" rows="4" required></textarea>
        </div>
        <button type="submit" class="btn btn-danger w-100">Send Message</button>
      </form>
    </div>
  </div>
</div>
```

✅ Uses Bootstrap form layout and buttons for professional feedback.

---

## 🌺 Step 5 — Register & Login Pages

Re-use the forms from **Phase 10**.
Ensure links on both pages are connected:

```html
<p class="mt-3 text-center">
  Already have an account? <a href="login.html" class="text-danger">Login here</a>
</p>
```

and in `login.html`:

```html
<p class="mt-3 text-center">
  New user? <a href="register.html" class="text-danger">Create an account</a>
</p>
```

✅ Seamless transition between login and register.

---

## 🌻 Step 6 — Footer (Same on Every Page)

```html
<footer class="bg-danger text-white text-center p-3 mt-5">
  <p>&copy; 2025 Transflower Store. Built with ❤️ using Bootstrap 5.</p>
</footer>
```

✅ Add consistent closing touch to all pages.

---

## 🌼 Step 7 — Custom Styling (css/style.css)

```css
body {
  font-family: 'Poppins', sans-serif;
}

h2 {
  letter-spacing: 1px;
}

.btn-danger {
  border-radius: 25px;
}

footer {
  font-size: 0.9rem;
}
```

✅ Enhances uniform typography and aesthetics.

---

## 🌸 Mentor Wrap-Up

**Mentor:**
“Today, you’ve moved from *building pages* to *crafting an experience*.
You’ve stitched together Home, About, Contact, Register, and Login —
creating a true web presence with consistent identity.

This is the foundation of professional front-end development.”

> “Bootstrap is not just a UI library — it’s a design philosophy of clarity, consistency, and care.”

---

### ✅ Students Learned

| Concept             | Description                | Example                               |
| ------------------- | -------------------------- | ------------------------------------- |
| Page Integration    | Linking multiple pages     | `<a href="about.html">About</a>`      |
| Consistent Layout   | Shared Navbar & Footer     | Reusable design pattern               |
| Responsive Design   | Mobile-ready layout        | `.container`, `.row`, `.col-md`       |
| Page Navigation     | Internal linking           | Navbar navigation                     |
| Professional Polish | Unified color & typography | `bg-danger`, `btn-danger`, custom CSS |

 