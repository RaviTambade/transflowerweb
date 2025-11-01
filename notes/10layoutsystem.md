

## Phase 8: “Design That Adapts — Understanding the Bootstrap Grid System”



### 🌼 Mentor Begins

**Mentor:**
“Imagine a bouquet shop that delivers across the country.
Every customer uses a different device — some browse on phones, others on tablets, and many on desktops.

If your website doesn’t *adapt* to these devices, users will scroll endlessly or miss key information.
That’s why professional developers use **responsive design frameworks like Bootstrap** — it’s like giving your website the flexibility of water: it fits any container!”



## 🎯 Learning Objectives

By the end of this phase, students will:

* Understand the **12-column Bootstrap grid system**
* Build **responsive layouts** using `.container`, `.row`, and `.col-*`
* Use **Flexbox utilities** for alignment and spacing
* Practice **breakpoints** for adaptive design
* Create a **responsive product card layout** for Transflower Store



## 🧱 Step 1 — The Bootstrap Grid System: Foundation

Bootstrap divides every page into a **12-column grid**.

Think of it like this:

* The page width = 12 parts
* You can combine these parts differently per device size

Example:

```html
<div class="container">
  <div class="row">
    <div class="col-12 col-md-6 col-lg-4">Box 1</div>
    <div class="col-12 col-md-6 col-lg-4">Box 2</div>
    <div class="col-12 col-md-6 col-lg-4">Box 3</div>
  </div>
</div>
```

🧠 **Explanation:**

* `.col-12`: full width on mobile
* `.col-md-6`: half width on tablets
* `.col-lg-4`: one-third width on large screens

This is **responsive design in action** — the layout automatically adjusts!


## 🧩 Step 2 — Breakpoints & Device Sizes

| Class Prefix | Screen Width | Device Type          |
| ------------ | ------------ | -------------------- |
| `.col-`      | `<576px`     | Extra Small (mobile) |
| `.col-sm-`   | `≥576px`     | Small devices        |
| `.col-md-`   | `≥768px`     | Tablets              |
| `.col-lg-`   | `≥992px`     | Laptops              |
| `.col-xl-`   | `≥1200px`    | Desktops             |
| `.col-xxl-`  | `≥1400px`    | Large screens        |

These breakpoints give full control over how your content behaves on each device.

## 🌸 Step 3 — Responsive Product Cards

Now, let’s make a **Responsive Product Gallery** for your Transflower Store homepage.

```html
<section class="container my-5">
  <h2 class="text-center mb-4">Our Bestselling Bouquets</h2>
  
  <div class="row g-4">
    <div class="col-12 col-md-6 col-lg-3">
      <div class="card h-100">
        <img src="images/rose.jpg" class="card-img-top" alt="Rose Bouquet">
        <div class="card-body text-center">
          <h5>Red Roses</h5>
          <p>Rs. 599</p>
        </div>
      </div>
    </div>

    <div class="col-12 col-md-6 col-lg-3">
      <div class="card h-100">
        <img src="images/tulip.jpg" class="card-img-top" alt="Tulip Bouquet">
        <div class="card-body text-center">
          <h5>Yellow Tulips</h5>
          <p>Rs. 699</p>
        </div>
      </div>
    </div>

    <div class="col-12 col-md-6 col-lg-3">
      <div class="card h-100">
        <img src="images/orchid.jpg" class="card-img-top" alt="Orchid Bouquet">
        <div class="card-body text-center">
          <h5>White Orchids</h5>
          <p>Rs. 799</p>
        </div>
      </div>
    </div>

    <div class="col-12 col-md-6 col-lg-3">
      <div class="card h-100">
        <img src="images/lily.jpg" class="card-img-top" alt="Lily Bouquet">
        <div class="card-body text-center">
          <h5>Pink Lilies</h5>
          <p>Rs. 749</p>
        </div>
      </div>
    </div>
  </div>
</section>
```

🧠 **Concepts introduced:**

* `.row` and `.col-*` define layout structure
* `.g-4` adds equal spacing (gutters)
* `.h-100` ensures equal card height
* Adapts perfectly from mobile → tablet → desktop

## 🧮 Step 4 — Flexbox Utilities

Sometimes you need fine-grained control inside your grid — that’s where **Flexbox utilities** shine.

```html
<div class="d-flex justify-content-between align-items-center p-3 bg-light">
  <div>🌼 Transflower</div>
  <div>
    <button class="btn btn-outline-danger">Login</button>
  </div>
</div>
```

🧠 **Explanation:**

* `d-flex` → enables flex layout
* `justify-content-between` → spaces elements apart horizontally
* `align-items-center` → aligns vertically

✅ This is how modern **headers, navbars, and dashboards** are structured.


## 🧭 Step 5 — Combining Grid + Flexbox for Hero Section

Here’s a **hero layout** example combining both:

```html
<section class="container my-5">
  <div class="row align-items-center">
    <div class="col-md-6 text-center text-md-start">
      <h1>Fresh Flowers Delivered Daily 🌹</h1>
      <p class="lead">Order online and make every day bloom beautifully.</p>
      <button class="btn btn-danger btn-lg mt-3">Shop Now</button>
    </div>
    <div class="col-md-6 text-center">
      <img src="images/hero.jpg" class="img-fluid rounded-4 shadow" alt="Hero Image">
    </div>
  </div>
</section>
```

🧠 **Concepts reinforced:**

* **Text + image layout** adapts to screen size
* `align-items-center` keeps both vertically aligned
* `.img-fluid` makes images responsive


## 🌈 Step 6 — Add Custom Styles

```css
h1 {
  color: #e91e63;
  font-weight: bold;
}

.lead {
  color: #555;
}

.card img {
  height: 200px;
  object-fit: cover;
}
```


## 🌟 Mentor Wrap-Up

**Mentor:**
“Design is not just about color and beauty — it’s about adaptability.
A responsive layout ensures that your design *respects* every user’s device, no matter how big or small.

Bootstrap gives you a professional-grade grid system — flexible, reliable, and production-ready.”

> “A good design feels natural everywhere. That’s the power of Bootstrap’s Grid.”


### ✅ Students Learned

| Concept           | Description                   | Example                            |
| ----------------- | ----------------------------- | ---------------------------------- |
| Grid System       | 12-column responsive layout   | `.col-md-6 .col-lg-3`              |
| Breakpoints       | Screen-size adaptability      | `.col-sm-`, `.col-md-`, `.col-lg-` |
| Flex Utilities    | Alignment & spacing           | `d-flex justify-content-center`    |
| Responsive Images | Scale automatically           | `.img-fluid`                       |
| Real-World Layout | Cards, hero sections, navbars | Transflower Store components       |

 