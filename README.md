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
11. [Teaching Tips](#teaching-tips)

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
Load Google Fonts, define CSS variables for theming, and add a Font Awesome shopping cart icon.

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
