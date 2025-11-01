Excellent 🌟

Welcome to **Phase 13 — “Bootstrap Grid System in Action: Building a Responsive Product Catalog”**

Your students now understand the components like navbars, cards, carousels, and tabs.
Now, it’s time to *apply* all of that knowledge in a **real-world layout** — building a responsive **product catalog** page that adapts beautifully across devices.

---

## 🧑‍🏫 Mentor Storytelling

### Phase 13: “Designing for Every Screen — The Power of the Bootstrap Grid System”

---

### 🌸 Mentor Begins

**Mentor:**
“When we browse a website on a laptop, tablet, or phone — the layout looks perfectly adjusted.
How does it know which device you’re on?

That magic comes from Bootstrap’s **Grid System**, built on top of CSS Flexbox.
It’s like a flexible container with invisible lines that rearrange content depending on the screen size.”

---

## 🎯 Learning Objectives

By the end of this phase, students will:

* Understand Bootstrap’s 12-column grid system
* Use containers, rows, and columns effectively
* Design responsive layouts using breakpoints (`sm`, `md`, `lg`, `xl`)
* Create a responsive **Product Catalog Page**
* Test responsiveness using Chrome Developer Tools

---

## 🌷 Step 1 — Grid System Overview

Bootstrap divides the screen into **12 equal columns**.
You place content inside `<div class="col">` within `<div class="row">`.

```html
<div class="container">
  <div class="row">
    <div class="col-4">Column 1</div>
    <div class="col-4">Column 2</div>
    <div class="col-4">Column 3</div>
  </div>
</div>
```

✅ 3 columns each taking 4 units (4 + 4 + 4 = 12)
✅ Automatically responsive if you use `.col` instead of fixed sizes

---

## 🌹 Step 2 — Responsive Breakpoints

Bootstrap grid supports different layouts for various screen sizes.

| Breakpoint  | Prefix     | Min Width |
| ----------- | ---------- | --------- |
| Extra Small | `.col-`    | <576px    |
| Small       | `.col-sm-` | ≥576px    |
| Medium      | `.col-md-` | ≥768px    |
| Large       | `.col-lg-` | ≥992px    |
| Extra Large | `.col-xl-` | ≥1200px   |

Example:

```html
<div class="col-12 col-md-6 col-lg-4">Product Card</div>
```

* On **mobile** → 1 column (`col-12`)
* On **tablet** → 2 columns (`col-md-6`)
* On **desktop** → 3 columns (`col-lg-4`)

---

## 🌼 Step 3 — Product Catalog Example

```html
<div class="container my-5">
  <h2 class="text-center mb-4">Our Products</h2>
  <div class="row g-4">
    
    <div class="col-12 col-sm-6 col-md-4 col-lg-3">
      <div class="card h-100">
        <img src="images/product1.jpg" class="card-img-top" alt="Product 1">
        <div class="card-body">
          <h5 class="card-title">Wireless Earbuds</h5>
          <p class="card-text">$59.99</p>
          <a href="#" class="btn btn-primary">Buy Now</a>
        </div>
      </div>
    </div>

    <div class="col-12 col-sm-6 col-md-4 col-lg-3">
      <div class="card h-100">
        <img src="images/product2.jpg" class="card-img-top" alt="Product 2">
        <div class="card-body">
          <h5 class="card-title">Smart Watch</h5>
          <p class="card-text">$129.99</p>
          <a href="#" class="btn btn-primary">Buy Now</a>
        </div>
      </div>
    </div>

    <!-- Repeat for more products -->

  </div>
</div>
```

✅ Uses **`.row`** for alignment
✅ **`.col-*`** for responsive sizing
✅ **`.g-4`** for consistent spacing (gutters)
✅ **`.h-100`** ensures all cards are equal height

---

## 🌻 Step 4 — Enhancing the Layout

Add a **hero section** and footer for realism:

```html
<!-- Hero Banner -->
<div class="bg-primary text-white text-center p-5 mb-4 rounded-3">
  <h1>Welcome to Transflower Store 🌼</h1>
  <p>Your one-stop shop for smart tech and lifestyle products</p>
</div>

<!-- Footer -->
<footer class="bg-dark text-white text-center py-3 mt-4">
  <small>© 2025 Transflower Store. All Rights Reserved.</small>
</footer>
```

---

## 🌺 Mentor Wrap-Up

**Mentor:**
“Web design isn’t just about beauty — it’s about adaptability.
Your users are everywhere: phones, tablets, laptops, desktops.

Bootstrap’s Grid System makes sure your design *adapts gracefully* without writing separate CSS for every device.
That’s what makes your web pages look professional — everywhere, every time.”

> “The best UI doesn’t just resize — it *reflows* naturally, respecting every screen.”

---

### ✅ Students Learned

| Concept          | Description                 | Example                            |
| ---------------- | --------------------------- | ---------------------------------- |
| Grid System      | 12-column responsive layout | `.col-4`, `.col-md-6`, `.col-lg-3` |
| Breakpoints      | Device-based responsiveness | `sm`, `md`, `lg`, `xl`             |
| Containers       | Center and pad content      | `.container`, `.container-fluid`   |
| Gutters          | Spacing between columns     | `.g-3`, `.g-4`                     |
| Real Application | Product Catalog Page        | Responsive cards using grid        |

---

Would you like me to continue to **Phase 14 — “Bootstrap Utilities & Customization: Colors, Spacing, Shadows, and Themes for Personalized Design”**?
