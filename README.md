# Zobo Delight Project

**Zobo Delight** is a product site for an authentic Nigerian hibiscus drink built step by step. This README outlines the evolution of the site—from a basic HTML skeleton to a fully featured, polished, and responsive product site.

---

## Table of Contents

1. [Step 1: Basic HTML Structure](#step-1-basic-html-structure)
2. [Step 2: Add Navigation and Additional Sections](#step-2-add-navigation-and-additional-sections)
3. [Step 3: Sticky Header and Basic Layout Enhancements](#step-3-sticky-header-and-basic-layout-enhancements)
4. [Step 4: External Fonts, CSS :root Variables, and Icons](#step-4-external-fonts-css-root-variables-and-icons)
5. [Step 5: Build the Products Section](#step-5-build-the-products-section)
6. [Step 6: Build the Testimonials Section](#step-6-build-the-testimonials-section)
7. [Step 7: Build the Team & Gallery Section](#step-7-build-the-team--gallery-section)
8. [Step 8: Build the Contact Section](#step-8-build-the-contact-section)
9. [Step 9: Final Touches – Animations, Transitions, and Responsiveness](#step-9-final-touches)
10. [Step 10: Final Integration and Review](#step-10-final-integration-and-review)

---

## Step 1: Basic HTML Structure

**Objective:**  
Introduce a minimal HTML skeleton with essential elements.

**HTML:**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Zobo Delight</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <header>
      <h1>Zobo Delight</h1>
    </header>
    <main>
      <section id="about">
        <h2>About Zobo</h2>
        <p>Welcome to Zobo Delight – a refreshing local drink.</p>
      </section>
    </main>
    <footer>
      <p>&copy; 2025 Zobo Delight</p>
    </footer>
  </body>
</html>
```

**CSS (styles.css):**

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  text-align: center;
}

header {
  background-color: lightgray;
  padding: 20px;
}

footer {
  background-color: darkgray;
  padding: 10px;
  color: white;
}
```

**Explanation:**
_This basic version introduces the header, main content (with one "About" section), and footer. It forms the foundation for later enhancements._

---

## Step 2: Add Navigation and Additional Sections

**Objective:**  
Add a semantic navigation bar and placeholders for additional content sections.

**HTML Update:**

```html
<header>
  <h1>Zobo Delight</h1>
  <nav>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#products">Products</a></li>
      <li><a href="#testimonials">Testimonials</a></li>
      <li><a href="#team-gallery">Team & Gallery</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>
<main>
  <!-- About Section -->
  <section id="about">
    <h2>About Zobo</h2>
    <p>
      Welcome to Zobo Delight – a refreshing local drink crafted from hibiscus,
      ginger, and spices.
    </p>
  </section>
  <!-- Products Section -->
  <section id="products">
    <h2>Our Products</h2>
    <!-- Products content will be added later -->
  </section>
  <!-- Testimonials Section -->
  <section id="testimonials">
    <h2>Customer Love</h2>
    <!-- Testimonials content will be added later -->
  </section>
  <!-- Team & Gallery Section -->
  <section id="team-gallery">
    <h2>Our Team & Gallery</h2>
    <!-- Team & Gallery content will be added later -->
  </section>
  <!-- Contact Section -->
  <section id="contact">
    <h2>Contact</h2>
    <!-- Contact form will be added later -->
  </section>
</main>
<footer>
  <p>&copy; 2025 Zobo Delight</p>
</footer>
```

**CSS Update:**

```css
nav ul {
  list-style: none;
  padding: 0;
  margin: 10px 0;
  display: flex;
  justify-content: center;
  gap: 20px;
}

nav a {
  text-decoration: none;
  color: black;
}
```

**Explanation:**
_This step adds a navigation menu and creates placeholders for future sections._

---

## Step 3: Sticky Header and Basic Layout Enhancements

**Objective:**
Use Flexbox for a full-height layout and make the header sticky.

**CSS Update:**

```css
body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

header {
  position: sticky;
  top: 0;
  z-index: 1000;
  background-color: lightgray;
  padding: 20px;
}

main {
  flex: 1;
  padding: 20px;
}
```

**Explanation:**
_Using Flexbox ensures that the main content fills the viewport, while a sticky header keeps the navigation in view._

---

## Step 4: External Fonts, :root Variables, and Icons

**Objective:**
Load Google Fonts, define CSS variables for theming, and add a Font Awesome icon.

**HTML Update (inside `<head>`)**

```html
<!-- Google Fonts -->
<link
  href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&family=Playfair+Display:wght@700&display=swap"
  rel="stylesheet"
/>
<!-- Font Awesome for icons -->
<link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
/>
```

**CSS Update:**

```css
:root {
  --primary-color: #9f2b2b; /* Hibiscus red */
  --secondary-color: #f4a460; /* Warm accent */
  --dark-color: #2c1810;
  --light-color: #fff5ee;
  --error-color: #c00;
  --transition-speed: 0.3s;
}

body {
  font-family: "Poppins", sans-serif;
}

h1,
h2,
h3 {
  font-family: "Playfair Display", serif;
}
```

**Explanation:**
_External fonts and CSS variables ensure a consistent theme, while Font Awesome adds visual icons._

---

## Step 5: Build the Products Section

**Objective:**
Create a responsive products section using CSS Grid.

**HTML (Products Section)**

```html
<section id="products" aria-labelledby="products-heading">
  <h2 id="products-heading">Our Products</h2>
  <div class="product-grid">
    <article class="product">
      <h3>Classic Zobo</h3>
      <img
        src="https://picsum.photos/seed/classic-zobo/400/300"
        alt="Classic Zobo drink"
        loading="lazy"
      />
      <p>
        Our original recipe that delivers pure hibiscus flavor with a natural
        tang.
      </p>
      <button class="add-to-cart" aria-label="Add Classic Zobo to cart">
        Order Now
      </button>
    </article>
    <article class="product">
      <h3>Spiced Zobo</h3>
      <img
        src="https://picsum.photos/seed/spiced-zobo/400/300"
        alt="Spiced Zobo drink"
        loading="lazy"
      />
      <p>
        Infused with ginger and cloves, offering an extra kick for a bold taste
        experience.
      </p>
      <button class="add-to-cart" aria-label="Add Spiced Zobo to cart">
        Order Now
      </button>
    </article>
    <article class="product">
      <h3>Premium Zobo</h3>
      <img
        src="https://picsum.photos/seed/premium-zobo/400/300"
        alt="Premium Zobo drink"
        loading="lazy"
      />
      <p>
        A refined blend with a hint of citrus for a sophisticated flavor
        profile.
      </p>
      <button class="add-to-cart" aria-label="Add Premium Zobo to cart">
        Order Now
      </button>
    </article>
  </div>
</section>
```

**CSS (Product Styling):**

```css
.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.product {
  text-align: center;
  padding: 1.5rem;
  border-radius: 10px;
  transition: transform var(--transition-speed);
}

.product:hover {
  transform: translateY(-5px);
}

.product img {
  border-radius: 10px;
  height: 200px;
  object-fit: cover;
  margin: 1rem 0;
}

.add-to-cart {
  background: var(--primary-color);
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 25px;
  text-decoration: none;
  display: inline-block;
  margin-top: 1rem;
  transition: background var(--transition-speed);
  border: none;
  cursor: pointer;
}

.add-to-cart:hover {
  background: var(--dark-color);
}
```

**Explanation:**
_CSS Grid creates a flexible layout for products, and hover effects improve interactivity._

---

## Step 6: Build the Testimonials Section

**Objective:**
Create a testimonials section with customer quotes and responsive rating stars.

**HTML (Testimonials Section)**

```html
<section id="testimonials" aria-labelledby="testimonials-heading">
  <h2 id="testimonials-heading">Customer Love</h2>
  <div class="testimonial-grid">
    <article class="testimonial">
      <div class="quote-icon"><i class="fas fa-quote-left"></i></div>
      <p>
        "The best Zobo I've ever tasted! Perfect balance of sweetness and
        spice."
      </p>
      <div class="customer">
        <img
          src="https://i.pravatar.cc/100?img=47"
          alt="Amina Mohammed"
          loading="lazy"
        />
        <h4>Amina Mohammed</h4>
        <div class="rating">
          <i class="fas fa-star"></i>
          <i class="fas fa-star"></i>
          <i class="fas fa-star"></i>
          <i class="fas fa-star"></i>
          <i class="fas fa-star"></i>
        </div>
      </div>
    </article>
    <article class="testimonial">
      <div class="quote-icon"><i class="fas fa-quote-left"></i></div>
      <p>"Zobo Delight is my go-to drink for staying refreshed and healthy!"</p>
      <div class="customer">
        <img
          src="https://i.pravatar.cc/100?img=46"
          alt="Chinedu Okoro"
          loading="lazy"
        />
        <h4>Chinedu Okoro</h4>
        <div class="rating">
          <i class="fas fa-star"></i>
          <i class="fas fa-star"></i>
          <i class="fas fa-star"></i>
          <i class="fas fa-star"></i>
          <i class="fas fa-star-half-alt"></i>
        </div>
      </div>
    </article>
  </div>
</section>
```

**CSS (Testimonial Styling):**

```css
.testimonial-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.testimonial {
  background: white;
  padding: 2rem;
  border-radius: 10px;
  position: relative;
}

.quote-icon {
  color: var(--secondary-color);
  font-size: 2rem;
  opacity: 0.3;
}

.customer {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-top: 1rem;
}

.customer img {
  border-radius: 50%;
}

.rating {
  color: #ffd700;
}

.rating i {
  font-size: 1.2rem; /* Responsive rating stars */
}
```

**Explanation:**
_The testimonial section is set in a grid, and the rating stars are sized responsively using rem units._

---

## Step 7: Build the Team & Gallery Section

**Objective:**
Showcase the team (using Flexbox) and a product gallery (using CSS Grid).

**HTML (Team & Gallery Section)**

```html
<section id="team-gallery" aria-labelledby="team-gallery-heading">
  <h2 id="team-gallery-heading">Our Team & Gallery</h2>
  <!-- Our Team (Flexbox) -->
  <div class="flex-demo">
    <div class="flex-item">
      <img
        src="https://picsum.photos/seed/member1/100/100"
        alt="Adewale - Master Brewer"
        loading="lazy"
      />
      <h5>Adewale</h5>
      <p>Master Brewer</p>
    </div>
    <div class="flex-item">
      <img
        src="https://picsum.photos/seed/member2/100/100"
        alt="Ifeoma - Quality Control"
        loading="lazy"
      />
      <h5>Ifeoma</h5>
      <p>Quality Control</p>
    </div>
    <div class="flex-item">
      <img
        src="https://picsum.photos/seed/member3/100/100"
        alt="Chinedu - Packaging Manager"
        loading="lazy"
      />
      <h5>Chinedu</h5>
      <p>Packaging Manager</p>
    </div>
  </div>
  <!-- Gallery (Grid) -->
  <div class="grid-demo">
    <div class="grid-item">
      <img
        src="https://picsum.photos/seed/gallery1/400/300"
        alt="Zobo in a Glass"
        loading="lazy"
      />
      <p>Zobo in a Glass</p>
    </div>
    <div class="grid-item">
      <img
        src="https://picsum.photos/seed/gallery2/400/300"
        alt="Bottled Zobo"
        loading="lazy"
      />
      <p>Bottled Zobo</p>
    </div>
    <div class="grid-item">
      <img
        src="https://picsum.photos/seed/gallery3/400/300"
        alt="Zobo with Ice"
        loading="lazy"
      />
      <p>Zobo with Ice</p>
    </div>
  </div>
</section>
```

**CSS (Team & Gallery Styling):**

```css
/* Flexbox: Our Team */
.flex-demo {
  display: flex;
  justify-content: space-around;
  gap: 15px;
  margin: 1rem 0;
  flex-wrap: wrap;
}

.flex-item {
  background-color: var(--light-color);
  padding: 1rem;
  flex: 1;
  min-width: 150px;
  max-width: 200px;
  text-align: center;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.flex-item img {
  border-radius: 50%;
  width: 80px;
  height: 80px;
  margin-bottom: 0.5rem;
}

.flex-item h5 {
  font-family: "Playfair Display", serif;
  font-size: 1.1rem;
  margin: 0;
}

.flex-item p {
  margin-top: 0.5rem;
  font-size: 0.9rem;
  color: var(--dark-color);
}

/* Grid: Gallery */
.grid-demo {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 15px;
  margin: 1rem 0;
}

.grid-item {
  background-color: white;
  padding: 1rem;
  text-align: center;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.grid-item img {
  width: 100%;
  height: auto;
  border-radius: 5px;
}

.grid-item p {
  margin-top: 0.5rem;
  font-size: 0.9rem;
  font-weight: bold;
  color: var(--dark-color);
}
```

**Explanation:**
_Flexbox arranges the team member profiles evenly, while CSS Grid creates a responsive gallery layout._

---

## Step 8: Build the Contact Section

**Objective:**
Create an accessible contact form with proper labels and focus styles.

**HTML (Contact Section)**

```html
<section id="contact" aria-labelledby="contact-heading">
  <h2 id="contact-heading">Contact</h2>
  <form id="contact-form" novalidate>
    <div class="form-group">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" required aria-required="true" />
    </div>
    <div class="form-group">
      <label for="email">Email:</label>
      <input
        type="email"
        id="email"
        name="email"
        required
        aria-required="true"
      />
    </div>
    <div class="form-group">
      <label for="phone">Phone Number:</label>
      <input
        type="tel"
        id="phone"
        name="phone"
        pattern="[0-9]{11}"
        aria-describedby="phone-help"
      />
      <small id="phone-help">Enter 11-digit Nigerian phone number</small>
    </div>
    <div class="form-group">
      <label for="message">Message:</label>
      <textarea
        id="message"
        name="message"
        rows="5"
        required
        aria-required="true"
      ></textarea>
    </div>
    <button type="submit">Send Message</button>
  </form>
</section>
```

**CSS (Contact Styling):**

```css
/* Contact Section */
form {
  max-width: 600px;
  margin: 0 auto;
}

.form-group {
  margin-bottom: 1rem;
}

.form-group label {
  display: block;
  margin-bottom: 0.5rem;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 0.5rem;
  border: 2px solid var(--primary-color);
  border-radius: 5px;
  transition: border-color var(--transition-speed);
}

.form-group input:focus,
.form-group textarea:focus {
  border-color: var(--secondary-color);
  outline: none;
}

button {
  background: var(--primary-color);
  color: white;
  border: none;
  padding: 1rem 2rem;
  border-radius: 25px;
  font-size: 1.1rem;
  cursor: pointer;
  transition: background var(--transition-speed);
  width: 100%;
}

button:hover {
  background: var(--dark-color);
}
```

**Explanation:**
The contact form uses accessible markup with proper labels and focus styles, ensuring usability and clarity.

---

## Step 9: Final Touches – Animations, Transitions, and Responsiveness

**Objective:**
Add subtle animations, smooth transitions, and media queries for a responsive design.

**CSS (Final Enhancements)**

```css
/* Simple Animation for Heading */
h1 {
  transition: color var(--transition-speed);
}

h1:hover {
  color: red;
}

/* Responsive Design */
@media (max-width: 768px) {
  html {
    font-size: 14px;
  }

  nav ul {
    flex-direction: column;
    gap: 10px;
  }

  .product-grid,
  .testimonial-grid {
    grid-template-columns: 1fr;
  }

  .product img {
    height: 150px;
  }
}

/* About Section Image Sizing */
#about img {
  width: 100%;
  height: auto;
  max-width: 800px;
  margin: 0 auto;
  display: block;
}

@media (min-width: 1200px) {
  #about img {
    max-width: 600px;
  }
}
```

**Explanation:**
These final touches polish the user experience with animations on hover and ensure the site is responsive on various devices.

---

## Step 10: Final Integration and Review

**Objective:**
Review the complete codebase, ensuring all sections and enhancements are integrated, and discuss the incremental improvements.

**Final Checklist:**

1. **HTML Structure:**

   - All sections (About, Products, Testimonials, Team & Gallery, Contact) are present with semantic markup and ARIA attributes.

2. **CSS Variables:**

   - :root variables are defined and consistently applied.

3. **Header & Navigation:**

   - The header is sticky and includes a logo and shopping cart icon; the navigation is responsive.

4. **Content Sections:**

   - Products, Testimonials, and Gallery sections effectively use CSS Grid and Flexbox.
   - The contact form is accessible, with proper labels and focus styles.

5. **Animations & Responsiveness:**

   - Hover effects and transitions add interactivity.
   - Media queries ensure the site is responsive on various devices.

6. **External Resources:**:
   - Google Fonts and Font Awesome are integrated and enhancing the visual design.
