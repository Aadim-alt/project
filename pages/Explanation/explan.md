# 📄 COMPLETE HTML & CSS EXPLANATION FOR ECOMART

---

## 📄 HTML CODE EXPLANATION

### **1. Document Setup (Head Section)**

```html
<!DOCTYPE html>
```
- Tells the browser this is an HTML5 document

```html
<html lang="en">
```
- Root element, `lang="en"` means content is in English

```html
<head>
```
- Contains metadata (information about the page, not visible content)

**Meta Tags:**
```html
<meta charset="UTF-8">
```
- Sets character encoding to UTF-8 (supports all languages and symbols)

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- Makes website responsive on mobile devices
- `width=device-width` = page width matches screen width
- `initial-scale=1.0` = no zoom when page loads

```html
<meta name="description" content="...">
<meta name="keywords" content="...">
```
- Help search engines (Google) understand your page
- Description shows in search results
- Keywords help with SEO (Search Engine Optimization)

```html
<title>Products - EcoMart | Sustainable Lifestyle Products</title>
```
- Text that appears in browser tab
- Important for SEO

**CSS Links:**
```html
<link rel="stylesheet" href="css/styles.css">
```
- **External CSS**: Links to separate CSS file
- `rel="stylesheet"` = relationship is a stylesheet
- `href="css/styles.css"` = file location

```html
<style>
    /* CSS code here */
</style>
```
- **Internal CSS**: CSS written inside HTML file
- Used for page-specific styles

---

### **2. Navigation Bar**

```html
<nav class="navbar">
```
- `<nav>` = semantic HTML tag for navigation
- `class="navbar"` = assigns CSS class for styling

```html
<div class="nav-container">
```
- Container to hold and organize nav items

```html
<div class="logo">EcoMart</div>
```
- Your website logo/brand name

```html
<ul class="nav-menu">
    <li><a href="index.html">Home</a></li>
    <li><a href="products.html" class="active">Products</a></li>
    ...
</ul>
```
- `<ul>` = unordered list (bullet points removed by CSS)
- `<li>` = list item
- `<a href="...">` = hyperlink/anchor tag
- `class="active"` = highlights current page
- `href="products.html"` = link destination

---

### **3. Main Content Container**

```html
<div class="products-container">
```
- Main wrapper for all products
- CSS will center and style this

```html
<h1>Our Sustainable Products</h1>
```
- `<h1>` = main heading (largest, most important)
- Only use ONE `<h1>` per page for SEO

```html
<p style="text-align: center; color: #666;">...</p>
```
- `<p>` = paragraph
- `style="..."` = **Inline CSS** (applied directly to element)
- `text-align: center` = centers text
- `color: #666` = gray color

---

### **4. Products Grid**

```html
<div class="products-grid">
```
- Container for all product cards
- CSS Grid will arrange them in columns

---

### **5. Individual Product Card (Example: Product 1)**

```html
<div class="product-card" id="product1">
```
- `class="product-card"` = for CSS styling
- `id="product1"` = unique identifier (for JavaScript or specific styling)

**Product Image:**
```html
<img src="images/bamboo-bottle.jpg" alt="Bamboo Water Bottle" class="product-image">
```
- `<img>` = image tag (self-closing)
- `src="..."` = image source/location
- `alt="..."` = alternative text (shows if image fails, helps blind users)
- `class="product-image"` = CSS styling class

**Product Title:**
```html
<h2 class="product-title">Bamboo Water Bottle</h2>
```
- `<h2>` = second-level heading (smaller than h1)

**Product Description:**
```html
<p class="product-description">
    Premium bamboo water bottle...
</p>
```
- Regular paragraph with description

**Product Specifications Table:**
```html
<table style="width: 100%; margin: 15px 0; border-collapse: collapse;">
    <tr>
        <td style="padding: 5px; text-align: left;"><strong>Capacity:</strong></td>
        <td style="padding: 5px; text-align: right;">750ml</td>
    </tr>
    ...
</table>
```
- `<table>` = creates a table
- `<tr>` = table row
- `<td>` = table data/cell
- `<strong>` = bold text
- `border-collapse: collapse` = removes space between cells

**Price Section:**
```html
<div class="price-section">
    <span class="actual-price">NPR 2,500</span>
    <span class="discounted-price">NPR 1,999</span>
    <span class="discount-badge">20% OFF</span>
</div>
```
- `<span>` = inline container (doesn't create new line)
- Different classes for different price styling

**Add to Cart Button:**
```html
<button onclick="addToCart('Bamboo Water Bottle')" 
        style="background-color: #2c5f2d; color: white; ...">
    Add to Cart
</button>
```
- `<button>` = clickable button
- `onclick="addToCart(...)"` = calls JavaScript function when clicked
- `style="..."` = inline CSS for button styling

---

### **6. Footer**

```html
<footer style="background-color: #2c5f2d; color: white; ...">
    <p>&copy; 2026 EcoMart. All rights reserved.</p>
</footer>
```
- `<footer>` = semantic tag for page footer
- `&copy;` = HTML entity for copyright symbol ©

---

### **7. JavaScript Connection**

```html
<script src="js/script.js"></script>
```
- Links external JavaScript file
- Placed at end so HTML loads first (faster page load)

---

---

## 🎨 CSS CODE EXPLANATION

### **1. Universal Reset**

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
- `*` = selects ALL elements
- Removes default browser spacing
- `box-sizing: border-box` = padding/border included in width/height calculations

---

### **2. Body Styling**

```css
body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #f5f0e8;
    color: #4a3f35;
    line-height: 1.6;
}
```
- Sets default font for entire page
- `background-color: #f5f0e8` = cream/beige background
- `color: #4a3f35` = dark brown text
- `line-height: 1.6` = spacing between lines (improves readability)

---

### **3. Navigation Bar**

```css
.navbar {
    background: linear-gradient(135deg, #6b4423 0%, #8b5a3c 100%);
    padding: 15px 0;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
    position: sticky;
    top: 0;
    z-index: 1000;
}
```
- `.navbar` = class selector (applies to elements with `class="navbar"`)
- `linear-gradient(...)` = color gradient from dark brown to lighter brown
  - `135deg` = diagonal direction
  - `#6b4423 0%` = start color
  - `#8b5a3c 100%` = end color
- `padding: 15px 0` = 15px top/bottom, 0 left/right
- `box-shadow` = drop shadow effect
  - `0 2px 10px` = no horizontal offset, 2px down, 10px blur
  - `rgba(0, 0, 0, 0.2)` = black with 20% opacity
- `position: sticky` = navbar sticks to top when scrolling
- `z-index: 1000` = ensures navbar stays on top of other elements

---

### **4. Navigation Container**

```css
.nav-container {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
}
```
- `max-width: 1200px` = limits width on large screens
- `margin: 0 auto` = centers container (0 top/bottom, auto left/right)
- `display: flex` = flexbox layout (arranges items in row)
- `justify-content: space-between` = spaces items apart (logo left, menu right)
- `align-items: center` = vertically centers items

---

### **5. Logo**

```css
.logo {
    font-size: 28px;
    font-weight: bold;
    color: #f5f0e8;
    letter-spacing: 2px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}
```
- `letter-spacing: 2px` = adds 2px space between letters
- `text-shadow` = shadow behind text
  - `2px 2px` = 2px right, 2px down
  - `4px` = blur amount
  - `rgba(0, 0, 0, 0.3)` = black with 30% opacity

---

### **6. Navigation Menu**

```css
.nav-menu {
    list-style: none;
    display: flex;
    gap: 25px;
}
```
- `list-style: none` = removes bullet points
- `display: flex` = arranges items in row
- `gap: 25px` = 25px space between menu items

---

### **7. Navigation Links**

```css
.nav-menu a {
    text-decoration: none;
    color: #f5f0e8;
    font-size: 16px;
    padding: 8px 15px;
    border-radius: 5px;
    transition: all 0.3s ease;
}
```
- `text-decoration: none` = removes underline from links
- `padding: 8px 15px` = 8px top/bottom, 15px left/right
- `border-radius: 5px` = rounded corners
- `transition: all 0.3s ease` = smooth animation for any changes (0.3 seconds)

**Hover Effect:**
```css
.nav-menu a:hover {
    background-color: #a0826d;
    transform: translateY(-2px);
}
```
- `:hover` = applies when mouse is over element
- `transform: translateY(-2px)` = moves element up 2px

**Active Link:**
```css
.nav-menu a.active {
    background-color: #d4a574;
    color: #4a3f35;
    font-weight: bold;
}
```
- `.active` = highlights current page link

---

### **8. Headings**

```css
h1 {
    font-size: 2.5em;
    color: #6b4423;
    margin: 20px 0;
    text-align: center;
}
```
- `2.5em` = 2.5 times the default font size
- `margin: 20px 0` = 20px top/bottom, 0 left/right

```css
h2 {
    font-size: 1.8em;
    color: #8b5a3c;
}
```
- Slightly smaller than h1

---

### **9. Paragraphs**

```css
p {
    margin: 10px 0;
    font-size: 16px;
    color: #5a4a3a;
}
```
- Standard text styling

---

### **10. Buttons**

```css
button {
    cursor: pointer;
    transition: all 0.3s ease;
    font-family: Arial, Helvetica, sans-serif;
}

button:hover {
    transform: scale(1.05);
    box-shadow: 0 5px 15px rgba(107, 68, 35, 0.3);
}
```
- `cursor: pointer` = changes mouse to pointing hand
- `scale(1.05)` = enlarges button to 105% when hovering
- Creates subtle "lift" effect

---

### **11. Images**

```css
img {
    max-width: 100%;
    height: auto;
    display: block;
}
```
- `max-width: 100%` = image never exceeds container width
- `height: auto` = maintains aspect ratio
- `display: block` = removes tiny space below images

---

### **12. Tables**

```css
table {
    border-collapse: collapse;
    width: 100%;
}

table td {
    padding: 8px;
    border-bottom: 1px solid #d4a574;
}

table tr:hover {
    background-color: #f9f5ef;
}
```
- `border-collapse: collapse` = removes gaps between cells
- Hover effect on rows for interactivity

---

### **13. Forms**

```css
form {
    background-color: #ffffff;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(107, 68, 35, 0.1);
    max-width: 600px;
    margin: 30px auto;
}
```
- Styled container for forms

**Input Fields:**
```css
input[type="text"],
input[type="email"],
input[type="tel"],
textarea {
    width: 100%;
    padding: 12px;
    border: 2px solid #d4a574;
    border-radius: 5px;
    background-color: #faf8f5;
    transition: border-color 0.3s ease;
}
```
- `[type="text"]` = attribute selector (targets specific input types)
- `width: 100%` = fills container width

**Focus Effect:**
```css
input:focus,
textarea:focus {
    outline: none;
    border-color: #8b5a3c;
    background-color: #ffffff;
}
```
- `:focus` = applies when user clicks in field
- Changes border color for visual feedback

**Labels:**
```css
label {
    display: block;
    margin-top: 15px;
    color: #6b4423;
    font-weight: bold;
    font-size: 14px;
}
```
- `display: block` = puts label on its own line

**Submit Button:**
```css
input[type="submit"],
button[type="submit"] {
    background-color: #6b4423;
    color: #f5f0e8;
    padding: 12px 30px;
    border: none;
    border-radius: 5px;
    font-size: 16px;
    font-weight: bold;
    width: 100%;
    margin-top: 20px;
}

input[type="submit"]:hover,
button[type="submit"]:hover {
    background-color: #8b5a3c;
}
```
- Full-width button with hover effect

---

### **14. Links**

```css
a {
    color: #8b5a3c;
    text-decoration: underline;
    transition: color 0.3s ease;
}

a:hover {
    color: #6b4423;
}
```
- Standard link styling with color change on hover

---

### **15. Container Class**

```css
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
}
```
- Reusable class to center and contain content

---

### **16. Card Component**

```css
.card {
    background-color: #ffffff;
    border-radius: 10px;
    padding: 20px;
    margin: 20px 0;
    box-shadow: 0 4px 8px rgba(107, 68, 35, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(107, 68, 35, 0.2);
}
```
- Reusable card design with lift effect on hover

---

### **17. Sections**

```css
section {
    padding: 40px 20px;
    margin: 20px 0;
}

section:nth-child(even) {
    background-color: #ffffff;
}
```
- `section` = semantic HTML tag for page sections
- `:nth-child(even)` = selects every 2nd, 4th, 6th section (alternating backgrounds)

---

### **18. Header**

```css
header {
    background: linear-gradient(135deg, #8b5a3c 0%, #a0826d 100%);
    color: #f5f0e8;
    padding: 60px 20px;
    text-align: center;
}
```
- Hero section styling with gradient

---

### **19. Footer**

```css
footer {
    background-color: #4a3f35;
    color: #f5f0e8;
    text-align: center;
    padding: 30px 20px;
    margin-top: 50px;
}

footer a {
    color: #d4a574;
    text-decoration: none;
}

footer a:hover {
    color: #f5f0e8;
}
```
- Dark footer with lighter links

---

### **20. Utility Classes**

```css
.text-center {
    text-align: center;
}

.mt-20 {
    margin-top: 20px;
}

.mb-20 {
    margin-bottom: 20px;
}

.p-20 {
    padding: 20px;
}
```
- Quick helper classes for common styles
- Example: `<div class="text-center mt-20">` = centered text with 20px top margin

---

### **21. Responsive Design - Tablets**

```css
@media (max-width: 768px) {
    .nav-menu {
        flex-direction: column;
        gap: 10px;
    }
    
    h1 {
        font-size: 2em;
    }
    
    .nav-container {
        flex-direction: column;
        gap: 15px;
    }
}
```
- `@media` = media query (applies CSS based on screen size)
- `max-width: 768px` = tablets and smaller
- `flex-direction: column` = stacks menu items vertically
- Makes navigation and text smaller on tablets

---

### **22. Responsive Design - Mobile**

```css
@media (max-width: 480px) {
    h1 {
        font-size: 1.8em;
    }
    
    h2 {
        font-size: 1.5em;
    }
    
    .logo {
        font-size: 24px;
    }
    
    .nav-menu a {
        font-size: 14px;
        padding: 6px 10px;
    }
}
```
- `max-width: 480px` = mobile phones
- Further reduces font sizes for small screens
- Adjusts padding for better touch targets

---

---

## 🔗 HOW HTML & CSS WORK TOGETHER

### **Connection Method 1: CLASS Names**

**HTML:**
```html
<div class="navbar">
```

**CSS:**
```css
.navbar {
    background-color: brown;
}
```

The `.` in CSS means "select elements with this class"

---

### **Connection Method 2: ID Names**

**HTML:**
```html
<div id="product1">
```

**CSS:**
```css
#product1 {
    border: 2px solid red;
}
```

The `#` in CSS means "select element with this ID"
IDs must be unique on a page!

---

### **Connection Method 3: Tag Names**

**HTML:**
```html
<button>Click Me</button>
```

**CSS:**
```css
button {
    background-color: blue;
}
```

No symbol needed - directly targets all `<button>` elements

---

### **Connection Method 4: Inline Styles**

**HTML:**
```html
<p style="color: red; font-size: 20px;">Text</p>
```

Styles applied directly in HTML (not recommended for large projects)

---

---

## 📊 THREE TYPES OF CSS

### **1. EXTERNAL CSS** (Best Practice)
```html
<link rel="stylesheet" href="css/styles.css">
```
**Advantages:**
- Clean separation of HTML and CSS
- Reusable across multiple pages
- Easier to maintain
- Browser caches the file (faster loading)

---

### **2. INTERNAL CSS**
```html
<style>
    .navbar { background: brown; }
</style>
```
**When to use:**
- Page-specific styles
- Quick testing
- Single-page websites

---

### **3. INLINE CSS**
```html
<div style="color: red; padding: 10px;">
```
**When to use:**
- Quick fixes
- Testing
- Overriding other styles
- Dynamically generated content

**Priority:** Inline > Internal > External

---

---

## 🎯 PRACTICAL EXAMPLE: COMPLETE FLOW

**1. HTML Structure:**
```html
<div class="product-card">
    <h2>Bamboo Bottle</h2>
    <button onclick="buyNow()">Buy Now</button>
</div>
```

**2. External CSS Styling:**
```css
.product-card {
    background: white;
    padding: 20px;
    border-radius: 10px;
}

.product-card h2 {
    color: brown;
}

.product-card button {
    background: green;
    color: white;
}
```

**3. JavaScript Interaction:**
```javascript
function buyNow() {
    alert('Added to cart!');
}
```

**Result:** 
- HTML creates the structure
- CSS makes it beautiful
- JavaScript makes it interactive

---

---

## 🌈 COLOR CODES EXPLAINED

```css
color: #6b4423;
```
- `#` = hexadecimal color
- `6b` = red value (0-FF)
- `44` = green value (0-FF)
- `23` = blue value (0-FF)

**Alternative formats:**
```css
color: rgb(107, 68, 35);        /* Same color */
color: rgba(107, 68, 35, 0.5);  /* Same color, 50% transparent */
```

---

---

## 📐 SPACING EXPLANATION

### **Padding vs Margin**

```css
padding: 10px;  /* Space INSIDE element */
margin: 10px;   /* Space OUTSIDE element */
```

**Four-value syntax:**
```css
padding: 10px 20px 30px 40px;
/* top right bottom left (clockwise) */
```

**Two-value syntax:**
```css
padding: 10px 20px;
/* 10px top/bottom, 20px left/right */
```

**One value:**
```css
padding: 10px;
/* Same on all sides */
```

---

---

## 🎨 BROWN COLOR PALETTE USED

- **Main Brown:** `#6b4423` - Navigation, headings
- **Medium Brown:** `#8b5a3c` - Gradients, h2 tags
- **Light Brown:** `#a0826d` - Hover effects
- **Tan:** `#d4a574` - Accents, borders
- **Cream:** `#f5f0e8` - Background, light text
- **Dark Brown:** `#4a3f35` - Text, footer
- **Beige:** `#5a4a3a` - Paragraph text

---

---

## ✅ SUMMARY

**HTML provides:**
- Structure (headings, paragraphs, images)
- Content (text, links, buttons)
- Semantic meaning (nav, header, footer)

**CSS provides:**
- Visual design (colors, fonts, spacing)
- Layout (positioning, alignment)
- Responsiveness (mobile, tablet, desktop)
- Animations (hover effects, transitions)

**Together they create:**
A beautiful, functional, and responsive website!

---

## 💡 TIPS FOR YOUR PROJECT

1. **Use meaningful class names:** `.product-card` not `.box1`
2. **Comment your code:** Helps you and others understand
3. **Test on different screens:** Desktop, tablet, mobile
4. **Validate your HTML:** Use W3C validator
5. **Keep CSS organized:** Group related styles together
6. **Use consistent spacing:** Stick to 2 or 4 spaces for indentation
7. **Name files properly:** `products.html` not `page1.html`

---