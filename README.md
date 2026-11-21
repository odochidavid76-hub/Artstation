 index.html
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#171613">
<meta name="description" content="Shop beautiful artwork, premium framed prints and contemporary wall art at ARTSTATION.">

<title>ARTSTATION | Premium Art & Frames</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
:root {
  --dark:#171613;
  --cream:#f7f4ed;
  --gold:#c5a46b;
  --muted:#77736a;
  --white:#fff;
}

* {
  margin:0;
  padding:0;
  box-sizing:border-box;
}

html {scroll-behavior:smooth}

body {
  background:var(--cream);
  color:var(--dark);
  font-family:'DM Sans',sans-serif;
}

button,input,select,textarea {font:inherit}
button {cursor:pointer}
a {text-decoration:none;color:inherit}
img {width:100%;display:block;object-fit:cover}

.container {
  width:min(1200px,92%);
  margin:auto;
}

.announcement {
  background:var(--dark);
  color:white;
  padding:10px;
  text-align:center;
  font-size:11px;
  letter-spacing:1.5px;
}

header {
  position:sticky;
  top:0;
  z-index:100;
  background:rgba(247,244,237,.96);
  backdrop-filter:blur(15px);
  border-bottom:1px solid #e5dfd3;
}

.nav {
  min-height:78px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:20px;
}

.logo {
  font-family:'Playfair Display',serif;
  font-size:27px;
  font-weight:700;
  letter-spacing:1px;
}

.logo span {color:var(--gold)}

.nav-links {
  display:flex;
  gap:28px;
  align-items:center;
  list-style:none;
  font-size:13px;
}

.nav-links a:hover {color:#a17e45}

.nav-actions {
  display:flex;
  gap:15px;
  align-items:center;
}

.icon-btn {
  background:none;
  border:0;
  font-size:20px;
  position:relative;
}

.cart-count {
  position:absolute;
  top:-8px;
  right:-9px;
  background:var(--gold);
  color:white;
  width:17px;
  height:17px;
  border-radius:50%;
  font-size:10px;
  display:grid;
  place-items:center;
}

.menu-btn {
  display:none;
  border:0;
  background:none;
  font-size:25px;
}

/* HERO */

.hero {
  min-height:620px;
  display:grid;
  grid-template-columns:1fr 1fr;
  background:#e9e3d8;
}

.hero-content {
  display:flex;
  flex-direction:column;
  justify-content:center;
  padding:80px max(5vw,30px);
}

.eyebrow {
  font-size:11px;
  letter-spacing:3px;
  text-transform:uppercase;
  color:#9a7744;
  margin-bottom:25px;
}

.hero h1 {
  font-family:'Playfair Display',serif;
  font-size:clamp(45px,6vw,76px);
  font-weight:500;
  line-height:1.08;
}

.hero p {
  color:#6d685f;
  line-height:1.9;
  max-width:420px;
  margin:25px 0 30px;
  font-size:14px;
}

.btn {
  display:inline-flex;
  align-items:center;
  justify-content:center;
  background:var(--dark);
  color:white;
  border:1px solid var(--dark);
  padding:16px 25px;
  font-size:12px;
  letter-spacing:1px;
  transition:.3s;
}

.btn:hover {
  background:var(--gold);
  border-color:var(--gold);
}

.hero-image {
  min-height:620px;
  overflow:hidden;
}

.hero-image img {
  height:100%;
  object-fit:cover;
}

/* GENERAL */

section {padding:90px 0}

.section-heading {
  text-align:center;
  margin-bottom:45px;
}

.section-heading small {
  color:#a17e45;
  font-size:11px;
  letter-spacing:3px;
}

.section-heading h2 {
  font-family:'Playfair Display',serif;
  font-size:clamp(32px,4vw,48px);
  font-weight:500;
  margin-top:13px;
}

.section-heading p {
  color:var(--muted);
  font-size:13px;
  margin-top:12px;
}

/* BENEFITS */

.benefits {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
  padding:40px 0;
  border-bottom:1px solid #e3ddd1;
}

.benefit {
  text-align:center;
  padding:15px;
}

.benefit strong {
  display:block;
  font-family:'Playfair Display',serif;
  font-size:19px;
  margin-bottom:8px;
}

.benefit span {
  color:var(--muted);
  font-size:12px;
}

/* CATEGORIES */

.category-grid {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
}

.category {
  height:280px;
  position:relative;
  overflow:hidden;
  cursor:pointer;
  background:#ddd;
}

.category img {
  height:100%;
  transition:.5s;
}

.category:hover img {transform:scale(1.06)}

.category-label {
  position:absolute;
  bottom:0;
  left:0;
  width:100%;
  padding:40px 20px 20px;
  color:white;
  background:linear-gradient(transparent,rgba(0,0,0,.8));
}

.category-label h3 {
  font-family:'Playfair Display',serif;
  font-size:25px;
}

/* SHOP */

.shop {background:#f0ece3}

.shop-toolbar {
  display:flex;
  justify-content:space-between;
  gap:15px;
  flex-wrap:wrap;
  margin-bottom:30px;
}

.search-box {
  border:1px solid #d7d0c3;
  background:white;
  padding:12px 15px;
  width:250px;
  outline:none;
}

.filters {
  display:flex;
  gap:8px;
  flex-wrap:wrap;
}

.filter-btn {
  padding:11px 16px;
  background:transparent;
  border:1px solid #d5cebf;
  font-size:11px;
}

.filter-btn.active {
  background:var(--dark);
  color:white;
}

.product-grid {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:25px;
}

.product-card {
  background:white;
  overflow:hidden;
}

.product-image {
  height:300px;
  overflow:hidden;
  position:relative;
  background:#e5e0d5;
}

.product-image img {
  height:100%;
  transition:.5s;
}

.product-card:hover .product-image img {
  transform:scale(1.05);
}

.tag {
  position:absolute;
  top:14px;
  left:14px;
  background:white;
  padding:7px 11px;
  font-size:9px;
  letter-spacing:1px;
}

.product-info {padding:20px}

.product-info h3 {
  font-family:'Playfair Display',serif;
  font-size:20px;
  font-weight:500;
}

.product-info p {
  color:var(--muted);
  font-size:11px;
  margin:8px 0 13px;
}

.price {
  font-weight:700;
  font-size:16px;
}

.product-controls {
  display:flex;
  gap:8px;
  margin-top:17px;
}

.frame-select {
  flex:1;
  min-width:0;
  padding:11px 5px;
  border:1px solid #ded8cd;
  background:white;
  font-size:11px;
}

.add-btn {
  flex:1;
  padding:12px 5px;
  border:0;
  background:var(--dark);
  color:white;
  font-size:10px;
  letter-spacing:.5px;
}

.add-btn:hover {background:#9a7744}

.no-results {
  grid-column:1/-1;
  text-align:center;
  padding:50px;
  color:var(--muted);
}

/* STORY */

.story-grid {
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:65px;
  align-items:center;
}

.story-image {height:450px}
.story-image img {height:100%}

.story-text h2 {
  font-family:'Playfair Display',serif;
  font-size:43px;
  font-weight:500;
}

.story-text p {
  color:var(--muted);
  line-height:1.9;
  font-size:14px;
  margin:20px 0;
}

/* CUSTOM ART */

.custom {
  background:#211f1a;
  color:white;
  text-align:center;
}

.custom h2 {
  font-family:'Playfair Display',serif;
  font-size:clamp(34px,5vw,55px);
  font-weight:500;
}

.custom p {
  color:#c4bfb3;
  max-width:550px;
  margin:20px auto 30px;
  font-size:13px;
  line-height:1.9;
}

.custom .btn {
  background:var(--gold);
  border-color:var(--gold);
}

/* FAQ */

.faq-item {
  padding:22px 0;
  border-bottom:1px solid #ded8cc;
}

.faq-question {
  display:flex;
  justify-content:space-between;
  width:100%;
  background:none;
  border:0;
  text-align:left;
  font-weight:600;
}

.faq-answer {
  display:none;
  color:var(--muted);
  line-height:1.8;
  font-size:13px;
  padding-top:15px;
}

.faq-item.open .faq-answer {display:block}

/* NEWSLETTER */

.newsletter {
  background:#e9e3d8;
  text-align:center;
}

.newsletter h2 {
  font-family:'Playfair Display',serif;
  font-size:38px;
  font-weight:500;
}

.newsletter p {
  color:var(--muted);
  font-size:13px;
  margin:15px 0 25px;
}

.newsletter form {
  display:flex;
  max-width:450px;
  margin:auto;
}

.newsletter input {
  flex:1;
  min-width:0;
  padding:15px;
  border:1px solid #d5cebf;
  outline:none;
}

.newsletter button {
  border:0;
  background:var(--dark);
  color:white;
  padding:0 20px;
}

/* FOOTER */

footer {
  background:var(--dark);
  color:white;
  padding:65px 0 25px;
}

.footer-grid {
  display:grid;
  grid-template-columns:2fr 1fr 1fr;
  gap:40px;
  padding-bottom:45px;
}

.footer-grid p {
  color:#aaa69d;
  line-height:1.9;
  font-size:12px;
  margin-top:17px;
}

.footer-grid h4 {margin-bottom:18px}

.footer-grid a {
  display:block;
  color:#aaa69d;
  font-size:12px;
  margin-bottom:13px;
}

.footer-grid a:hover {color:var(--gold)}

.copyright {
  border-top:1px solid #39372f;
  padding-top:22px;
  display:flex;
  justify-content:space-between;
  gap:15px;
  flex-wrap:wrap;
  font-size:10px;
  color:#aaa69d;
}

/* CART DRAWER */

.overlay {
  display:none;
  position:fixed;
  inset:0;
  background:rgba(0,0,0,.5);
  z-index:200;
}

.overlay.show {display:block}

.cart-drawer {
  position:fixed;
  right:-450px;
  top:0;
  width:min(420px,100%);
  height:100%;
  background:white;
  z-index:201;
  padding:25px;
  transition:.35s;
  overflow:auto;
}

.cart-drawer.show {right:0}

.drawer-header {
  display:flex;
  justify-content:space-between;
  align-items:center;
  border-bottom:1px solid #eee;
  padding-bottom:20px;
}

.close-btn {
  background:none;
  border:0;
  font-size:25px;
}

.cart-item {
  display:grid;
  grid-template-columns:80px 1fr;
  gap:15px;
  padding:20px 0;
  border-bottom:1px solid #eee;
}

.cart-item img {
  height:90px;
  object-fit:cover;
}

.cart-item h4 {font-size:13px}

.cart-item p {
  font-size:11px;
  color:var(--muted);
  margin:7px 0;
}

.cart-item button {
  background:none;
  border:0;
  color:#a04b3f;
  font-size:11px;
}

.cart-summary {
  padding:25px 0;
}

.cart-total {
  display:flex;
  justify-content:space-between;
  font-weight:700;
  margin-bottom:20px;
}

.full-btn {
  width:100%;
  padding:16px;
  background:var(--dark);
  color:white;
  border:0;
}

.empty-cart {
  padding:50px 0;
  text-align:center;
  color:var(--muted);
}

/* CHECKOUT */

.modal {
  display:none;
  position:fixed;
  inset:0;
  z-index:300;
  background:rgba(0,0,0,.65);
  align-items:center;
  justify-content:center;
  padding:15px;
}

.modal.show {display:flex}

.modal-content {
  background:white;
  width:min(550px,100%);
  max-height:90vh;
  overflow:auto;
  padding:30px;
  position:relative;
}

.modal-content h2 {
  font-family:'Playfair Display',serif;
  margin-bottom:10px;
}

.modal-content p {
  color:var(--muted);
  font-size:12px;
  margin-bottom:20px;
}

.checkout-form input,
.checkout-form select,
.checkout-form textarea {
  width:100%;
  padding:13px;
  margin-bottom:12px;
  border:1px solid #ddd;
  outline:none;
  background:white;
  font-size:12px;
}

.checkout-form textarea {min-height:75px}

.checkout-total {
  padding:15px 0;
  display:flex;
  justify-content:space-between;
  font-weight:700;
}

.checkout-form button {
  width:100%;
  padding:16px;
  background:var(--dark);
  color:white;
  border:0;
}

.payment-note {
  font-size:10px;
  color:#777;
  line-height:1.7;
  margin-top:15px;
}

.whatsapp {
  position:fixed;
  bottom:22px;
  right:20px;
  z-index:90;
  background:#218c55;
  color:white;
  padding:14px 19px;
  border-radius:30px;
  font-size:12px;
  box-shadow:0 5px 20px #0002;
}

@media(max-width:850px) {
  .nav-links {
    display:none;
    position:absolute;
    top:78px;
    left:0;
    width:100%;
    background:var(--cream);
    padding:25px;
    flex-direction:column;
    align-items:flex-start;
  }

  .nav-links.active {display:flex}
  .menu-btn {display:block}

  .hero {grid-template-columns:1fr}
  .hero-content {padding:75px 7%}
  .hero-image {height:400px;min-height:0}

  .product-grid {grid-template-columns:repeat(2,1fr)}
  .story-grid {gap:30px}
}

@media(max-width:580px) {
  section {padding:65px 0}
  .benefits {grid-template-columns:1fr}
  .category-grid {grid-template-columns:1fr}
  .category {height:250px}
  .product-grid {grid-template-columns:1fr}
  .product-image {height:350px}
  .story-grid {grid-template-columns:1fr}
  .story-image {height:330px}
  .footer-grid {grid-template-columns:1fr}
  .shop-toolbar {flex-direction:column}
  .search-box {width:100%}
  .logo {font-size:23px}
}
</style>
</head>

<body>

<div class="announcement">
  DISCOVER ART THAT INSPIRES · WORLDWIDE SHOPPING
</div>

<header>
  <div class="container nav">

    <a class="logo" href="#">ARTSTATION<span>.</span></a>

    <button class="menu-btn" id="menuBtn" aria-label="Open menu">☰</button>

    <ul class="nav-links" id="navLinks">
      <li><a href="#home">Home</a></li>
      <li><a href="#categories">Collections</a></li>
      <li><a href="#shop">Shop Art</a></li>
      <li><a href="#about">About Us</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>

    <div class="nav-actions">
      <button class="icon-btn" id="cartOpen" aria-label="Open shopping cart">
        ♧ <span class="cart-count" id="cartCount">0</span>
      </button>
    </div>

  </div>
</header>

<main>

<!-- HERO -->

<section class="hero" id="home">

  <div class="hero-content">
    <div class="eyebrow">The Art of Beautiful Living</div>

    <h1>Make your walls tell a beautiful story.</h1>

    <p>
      Discover exceptional artwork, stunning canvas prints
      and premium picture frames. Bring your space to life
      with art that speaks to you.
    </p>

    <a href="#shop" class="btn">EXPLORE THE COLLECTION ↗</a>
  </div>

  <div class="hero-image">
    <img src="https://images.unsplash.com/photo-1579783902614-a3fb3927b6a5?auto=format&fit=crop&w=1200&q=85" alt="Beautiful framed artwork in a gallery">
  </div>

</section>

<div class="container benefits">

  <div class="benefit">
    <strong>Worldwide Shopping</strong>
    <span>Shop from different countries</span>
  </div>

  <div class="benefit">
    <strong>Premium Frames</strong>
    <span>Choose a frame that suits your space</span>
  </div>

  <div class="benefit">
    <strong>Secure Checkout</strong>
    <span>Payment integration ready</span>
  </div>

</div>

<!-- CATEGORIES -->

<section id="categories">
  <div class="container">

    <div class="section-heading">
      <small>OUR COLLECTIONS</small>
      <h2>Explore the world of art</h2>
      <p>Find the perfect artwork for every space.</p>
    </div>

    <div class="category-grid">

      <a class="category" href="#shop" data-category="Abstract">
        <img src="https://images.unsplash.com/photo-1541961017774-22349e4a1262?auto=format&fit=crop&w=800&q=85" alt="Abstract artwork">
        <div class="category-label"><h3>Abstract Art</h3></div>
      </a>

      <a class="category" href="#shop" data-category="Modern">
        <img src="https://images.unsplash.com/photo-1577083552431-6e5fd01aa342?auto=format&fit=crop&w=800&q=85" alt="Modern art">
        <div class="category-label"><h3>Modern Art</h3></div>
      </a>

      <a class="category" href="#shop" data-category="Nature">
        <img src="https://images.unsplash.com/photo-1470252649378-9c29740c9fa8?auto=format&fit=crop&w=800&q=85" alt="Nature inspired art">
        <div class="category-label"><h3>Nature & Landscapes</h3></div>
      </a>

    </div>
  </div>
</section>

<!-- SHOP -->

<section class="shop" id="shop">

  <div class="container">

    <div class="section-heading">
      <small>THE ARTSTATION SHOP</small>
      <h2>Curated for your space</h2>
      <p>Choose your favourite artwork and customize its frame.</p>
    </div>

    <div class="shop-toolbar">

      <input class="search-box" id="search" placeholder="Search artwork...">

      <div class="filters">
        <button class="filter-btn active" data-filter="All">All</button>
        <button class="filter-btn" data-filter="Abstract">Abstract</button>
        <button class="filter-btn" data-filter="Modern">Modern</button>
        <button class="filter-btn" data-filter="Nature">Nature</button>
      </div>

      <select id="sort" class="search-box">
        <option value="default">Sort products</option>
        <option value="low">Price: Low to High</option>
        <option value="high">Price: High to Low</option>
      </select>

    </div>

    <div class="product-grid" id="productGrid"></div>

  </div>
</section>

<!-- ABOUT -->

<section id="about">
  <div class="container story-grid">

    <div class="story-image">
      <img src="https://images.unsplash.com/photo-1577083552431-6e5fd01aa342?auto=format&fit=crop&w=1000&q=85" alt="Art gallery collection">
    </div>

    <div class="story-text">
      <div class="eyebrow">THE ARTSTATION STORY</div>

      <h2>Art is more than decoration.</h2>

      <p>
        ARTSTATION is an art and frame shopping destination
        created for people who appreciate creativity, beauty
        and personal expression.
      </p>

      <p>
        Our goal is to make discovering and purchasing artwork
        simple, enjoyable and accessible to art lovers around
        the world.
      </p>

      <a href="#contact" class="btn">GET IN TOUCH ↗</a>
    </div>

  </div>
</section>

<!-- CUSTOM ORDERS -->

<section class="custom">
  <div class="container">
    <div class="eyebrow">PERSONALIZED ART</div>

    <h2>Looking for something unique?</h2>

    <p>
      Need a special frame, custom artwork or a specific
      size? Tell us what you have in mind and let us help
      you find the perfect piece.
    </p>

    <a href="mailto:artwork@gmail.com?subject=Custom%20Artwork%20Request" class="btn">
      REQUEST CUSTOM ARTWORK ↗
    </a>
  </div>
</section>

<!-- FAQ -->

<section>
  <div class="container">

    <div class="section-heading">
      <small>HELP CENTER</small>
      <h2>Frequently asked questions</h2>
    </div>

    <div class="faq-item">
      <button class="faq-question">Do you accept international orders? <span>+</span></button>
      <div class="faq-answer">The store is designed for international shopping. Available destinations and delivery costs must be confirmed before orders are accepted.</div>
    </div>

    <div class="faq-item">
      <button class="faq-question">Can I choose a frame? <span>+</span></button>
      <div class="faq-answer">Yes. Each eligible artwork has frame options, including no frame, black, white and natural wood.</div>
    </div>

    <div class="faq-item">
      <button class="faq-question">How do I pay? <span>+</span></button>
      <div class="faq-answer">Online payment can be enabled through a secure payment provider such as Stripe after the payment server is configured.</div>
    </div>

    <div class="faq-item">
      <button class="faq-question">Can I request custom artwork? <span>+</span></button>
      <div class="faq-answer">Yes. Contact our team by email to discuss a custom design or framing request.</div>
    </div>

  </div>
</section>

<!-- NEWSLETTER -->

<section class="newsletter">
  <div class="container">

    <h2>Stay inspired.</h2>
    <p>Join our community and discover beautiful artwork.</p>

    <form id="newsletterForm">
      <input type="email" id="newsletterEmail" placeholder="Enter your email address" required>
      <button type="submit">JOIN</button>
    </form>

  </div>
</section>

</main>

<!-- FOOTER -->

<footer id="contact">
  <div class="container">

    <div class="footer-grid">

      <div>
        <a class="logo" href="#">ARTSTATION<span>.</span></a>
        <p>
          Discover beautiful artwork and premium frames.
          Bringing creativity and elegance to spaces around
          the world.
        </p>
      </div>

      <div>
        <h4>Explore</h4>
        <a href="#home">Home</a>
        <a href="#categories">Collections</a>
        <a href="#shop">Shop artwork</a>
        <a href="#about">Our story</a>
      </div>

      <div>
        <h4>Contact</h4>
        <a href="mailto:artwork@gmail.com">artwork@gmail.com</a>
        <a href="#contact">Los Angeles, California, USA</a>
        <a href="mailto:artwork@gmail.com?subject=Shipping%20Enquiry">Shipping enquiries</a>
      </div>

    </div>

    <div class="copyright">
      <span>© <span id="year"></span> ARTSTATION. All rights reserved
