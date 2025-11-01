


## Phase 7: “Designing for Discovery — Dynamic Content with Bootstrap Components”

 
### 🌼 Mentor Begins

**Mentor:**
“You’ve made your website visually stunning and interactive.
But now let’s make it *dynamic* — not with code, but with smart components.

In real-world websites, we often deal with *a lot* of content — FAQs, customer stories, product categories.
We can’t dump everything on one page. Instead, we use **accordions, tabs, and carousels** to organize information elegantly.”


## 🎯 Learning Objectives

By the end of this phase, students will:

* Use the **Bootstrap Carousel** for rotating content (images or testimonials)
* Implement an **Accordion** for FAQs or details
* Create **Tabs** for organized product or information sections
* Understand Bootstrap’s JavaScript component behavior (no manual JS required)


## 🏗️ Step 1 — Carousel for Testimonials or Featured Products

Let’s add a **testimonial carousel** to your `about.html`.

```html
<section class="container my-5">
  <h2 class="text-center mb-4">What Our Customers Say</h2>
  
  <div id="testimonialCarousel" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
      <div class="carousel-item active text-center">
        <blockquote class="blockquote">
          <p class="mb-4">"Transflower never disappoints! My anniversary bouquet was perfect."</p>
          <footer class="blockquote-footer">Sneha K.</footer>
        </blockquote>
      </div>

      <div class="carousel-item text-center">
        <blockquote class="blockquote">
          <p class="mb-4">"Fresh flowers and fast delivery — simply beautiful!"</p>
          <footer class="blockquote-footer">Rahul M.</footer>
        </blockquote>
      </div>

      <div class="carousel-item text-center">
        <blockquote class="blockquote">
          <p class="mb-4">"Best online flower store in Pune! Highly recommend."</p>
          <footer class="blockquote-footer">Aditi S.</footer>
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
</section>
```

🧠 **Concepts introduced:**

* `data-bs-ride="carousel"` enables auto-sliding
* Carousel items are switched automatically or via controls
* Great for product banners or testimonials

## 📚 Step 2 — Accordion for FAQ Section

Let’s add an FAQ section at the bottom of your `about.html`.

```html
<section class="container my-5">
  <h2 class="text-center mb-4">Frequently Asked Questions</h2>

  <div class="accordion" id="faqAccordion">
    <div class="accordion-item">
      <h2 class="accordion-header">
        <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#faq1">
          How long does delivery take?
        </button>
      </h2>
      <div id="faq1" class="accordion-collapse collapse show" data-bs-parent="#faqAccordion">
        <div class="accordion-body">
          We deliver within 24 hours for all Pune city orders and 2–3 days for other cities.
        </div>
      </div>
    </div>

    <div class="accordion-item">
      <h2 class="accordion-header">
        <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#faq2">
          Can I customize my bouquet?
        </button>
      </h2>
      <div id="faq2" class="accordion-collapse collapse" data-bs-parent="#faqAccordion">
        <div class="accordion-body">
          Absolutely! You can choose flower types, wrapping styles, and message cards.
        </div>
      </div>
    </div>
  </div>
</section>
```

🧠 **Concepts introduced:**

* Accordion automatically handles expand/collapse
* `data-bs-parent` ensures only one item opens at a time
* No custom JS needed — fully Bootstrap-driven


## 🧩 Step 3 — Tabs for Product Categories

Let’s make your `products.html` page more interactive using **Tabs**.

```html
<section class="container my-5">
  <h2 class="text-center mb-4">Explore Our Collections</h2>

  <!-- Tab Navigation -->
  <ul class="nav nav-tabs justify-content-center" id="productTab" role="tablist">
    <li class="nav-item" role="presentation">
      <button class="nav-link active" id="roses-tab" data-bs-toggle="tab" data-bs-target="#roses" type="button" role="tab">Roses</button>
    </li>
    <li class="nav-item" role="presentation">
      <button class="nav-link" id="tulips-tab" data-bs-toggle="tab" data-bs-target="#tulips" type="button" role="tab">Tulips</button>
    </li>
    <li class="nav-item" role="presentation">
      <button class="nav-link" id="orchids-tab" data-bs-toggle="tab" data-bs-target="#orchids" type="button" role="tab">Orchids</button>
    </li>
  </ul>

  <!-- Tab Content -->
  <div class="tab-content mt-4" id="productTabContent">
    <div class="tab-pane fade show active" id="roses" role="tabpanel">
      <div class="row">
        <div class="col-md-4">
          <div class="card">
            <img src="images/rose.jpg" class="card-img-top">
            <div class="card-body text-center">
              <h5>Red Rose Bouquet</h5>
              <p>Rs. 599</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="tab-pane fade" id="tulips" role="tabpanel">
      <p class="text-center">Tulip collection coming soon 🌷</p>
    </div>

    <div class="tab-pane fade" id="orchids" role="tabpanel">
      <p class="text-center">Orchid arrangements launching next week 🌸</p>
    </div>
  </div>
</section>
```

🧠 **Concepts introduced:**

* `nav-tabs` for visual navigation
* `tab-pane` + `fade` + `show active` for toggling sections
* Great for category-based UI

---

## 💄 Step 4 — Add Styling and Smooth Animation

In your `style.css`, add:

```css
.accordion-button:focus {
  box-shadow: 0 0 0 0.25rem rgba(233, 30, 99, 0.25);
}

.nav-tabs .nav-link.active {
  background-color: #e91e63;
  color: #fff;
}

.tab-content {
  animation: fadeIn 0.5s ease-in;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}
```

Now your accordion and tabs feel responsive *and smooth*.


## 🌟 Mentor Wrap-Up

**Mentor:**
“Today, you learned how to make your website truly dynamic — not by writing complex JavaScript, but by using Bootstrap’s built-in power.

Carousels tell stories.
Accordions simplify details.
Tabs organize categories.

These are the UI patterns that make content easy to navigate and enjoyable to explore.”

> “A good designer hides complexity. Bootstrap helps you do that with elegance.”


### ✅ Students Learned

| Concept   | Component                   | Real-World Application                |
| --------- | --------------------------- | ------------------------------------- |
| Carousel  | `.carousel`                 | Testimonials, banners, featured items |
| Accordion | `.accordion`                | FAQs, collapsible content             |
| Tabs      | `.nav-tabs`, `.tab-content` | Category navigation, product grouping |
| Animation | Keyframes + CSS             | Smooth transitions                    |

