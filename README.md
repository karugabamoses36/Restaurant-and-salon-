
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <meta name="description" content="Fremiot Food Nest &amp; Beauty Parlor – Premium Ugandan cuisine, authentic Luwombo, corporate delivery &amp; luxury beauty services in Kiwatule, Kampala.">
    <title>Fremiot | Food Nest &amp; Beauty Parlor – Excellence in Dining &amp; Glamour</title>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&amp;family=Montserrat:wght@300;400;500;600;700&amp;display=swap" rel="stylesheet">
    <!-- Font Awesome 6 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            background-color: #0a0806;
            color: #2c2b28;
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        h1, h2, h3, h4, .logo-text, .gold-text {
            font-family: 'Cormorant Garamond', serif;
            font-weight: 700;
        }

        :root {
            --gold: #d4af37;
            --gold-light: #f3e5ab;
            --gold-dark: #997a00;
            --dark-bg: #11100e;
            --card-bg: #fffbf2;
            --text-light: #f5f0e0;
            --glass-bg: rgba(20, 18, 16, 0.75);
        }

        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #1e1c18; }
        ::-webkit-scrollbar-thumb { background: var(--gold); border-radius: 10px; }

        /* Navbar – Premium glass morphism */
        .navbar {
            background: rgba(10, 8, 6, 0.94);
            backdrop-filter: blur(16px);
            padding: 0.6rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1100;
            border-bottom: 1px solid rgba(212, 175, 55, 0.5);
            transition: all 0.3s ease;
        }
        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            width: 100%;
            max-width: 1400px;
            margin: 0 auto;
        }
        .logo-area {
            display: flex;
            align-items: center;
            gap: 18px;
        }
        /* ENLARGED & CLEAR LOGO */
        .logo-img {
            width: 85px;
            height: 85px;
            border-radius: 50%;
            overflow: hidden;
            background: linear-gradient(135deg, var(--gold), #b8860b);
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 6px 20px rgba(212, 175, 55, 0.6);
            transition: transform 0.3s ease;
        }
        .logo-img:hover {
            transform: scale(1.03);
        }
        .logo-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .logo-text h1 {
            font-size: 2.1rem;
            color: var(--gold);
            letter-spacing: 2px;
            line-height: 1.1;
            text-shadow: 0 2px 5px rgba(0,0,0,0.3);
        }
        .logo-text p {
            font-size: 0.75rem;
            color: #f0e6c5;
            letter-spacing: 3px;
            margin-top: -4px;
            font-weight: 500;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2.5rem;
            align-items: center;
        }
        .nav-links a {
            color: var(--text-light);
            text-decoration: none;
            font-weight: 500;
            font-size: 1rem;
            transition: color 0.3s ease;
            position: relative;
        }
        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0%;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: var(--gold);
            transition: width 0.3s ease;
        }
        .nav-links a:hover::after {
            width: 100%;
        }
        .nav-links a:hover {
            color: var(--gold);
        }

        .hamburger {
            display: none;
            font-size: 1.8rem;
            color: var(--gold);
            cursor: pointer;
        }
        .cart-icon {
            position: relative;
            font-size: 1.6rem;
            color: var(--gold);
            cursor: pointer;
            transition: transform 0.2s;
        }
        .cart-icon:hover {
            transform: scale(1.05);
        }
        .cart-count {
            position: absolute;
            top: -8px;
            right: -8px;
            background: #111;
            color: var(--gold);
            font-size: 0.7rem;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            border: 1px solid var(--gold);
        }

        /* Hero */
        .hero {
            background: linear-gradient(105deg, rgba(0,0,0,0.7) 0%, rgba(0,0,0,0.5) 100%), 
                        url('https://images.unsplash.com/photo-1555396273-367ea4eb4db5?ixlib=rb-4.0.3&auto=format&fit=crop&w=2074&q=80') center/cover no-repeat fixed;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
        }
        .hero-content {
            max-width: 900px;
            padding: 2rem;
            animation: fadeUp 1s ease-out;
        }
        @keyframes fadeUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .hero-content h1 {
            font-size: 4.2rem;
            color: var(--gold);
            letter-spacing: 3px;
            margin-bottom: 1rem;
        }
        .hero-content p {
            font-size: 1.35rem;
            margin: 1.2rem auto 2.5rem;
        }
        .hero-buttons {
            display: flex;
            gap: 1.2rem;
            justify-content: center;
            flex-wrap: wrap;
        }
        .btn-gold {
            background: var(--gold);
            color: #111;
            padding: 14px 36px;
            border-radius: 50px;
            font-weight: 700;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            font-size: 1.05rem;
            border: none;
            cursor: pointer;
        }
        .btn-outline-gold {
            background: transparent;
            border: 2px solid var(--gold);
            color: var(--gold);
            padding: 12px 32px;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.4s;
            cursor: pointer;
        }
        .btn-gold:hover, .btn-outline-gold:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 28px rgba(212, 175, 55, 0.5);
        }

        .section {
            padding: 6rem 5%;
            max-width: 1400px;
            margin: 0 auto;
        }
        .section-dark {
            background: #141210;
            color: #f0ede8;
        }
        .section-title {
            text-align: center;
            font-size: 3rem;
            margin-bottom: 1rem;
            color: var(--gold);
            position: relative;
        }
        .section-title:after {
            content: '';
            display: block;
            width: 110px;
            height: 4px;
            background: linear-gradient(to right, transparent, var(--gold), transparent);
            margin: 1rem auto;
        }
        .subtitle {
            text-align: center;
            color: #c0b28a;
            font-size: 1.15rem;
            margin-bottom: 3rem;
        }

        .grid-3, .grid-4 {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(310px, 1fr));
            gap: 2.2rem;
        }
        .card {
            background: var(--card-bg);
            border-radius: 28px;
            overflow: hidden;
            box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.2);
            transition: all 0.4s cubic-bezier(0.2, 0.9, 0.4, 1.1);
            border: 1px solid rgba(212, 175, 55, 0.2);
        }
        .card:hover {
            transform: translateY(-12px) scale(1.01);
            box-shadow: 0 35px 45px -12px rgba(212, 175, 55, 0.4);
        }
        .card img {
            width: 100%;
            height: 240px;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        .card:hover img {
            transform: scale(1.05);
        }
        .card-content {
            padding: 1.5rem;
        }
        .card-content h3 {
            font-size: 1.55rem;
            margin-bottom: 0.6rem;
            color: #1f1b14;
        }
        .price {
            color: var(--gold-dark);
            font-weight: 800;
            font-size: 1.4rem;
        }
        .btn-book, .btn-cart {
            width: 100%;
            margin-top: 1rem;
            padding: 12px;
            border-radius: 50px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s;
        }
        .btn-book {
            background: var(--gold);
            color: #111;
            border: none;
        }
        .btn-cart {
            background: #111;
            color: var(--gold);
            border: 2px solid var(--gold);
        }
        .btn-book:hover { background: var(--gold-dark); color: white; }
        .btn-cart:hover { background: var(--gold); color: #111; }

        .special-banner {
            margin: 4rem 0;
            background: linear-gradient(135deg, #1f1b14, #0c0a07);
            border-radius: 48px;
            padding: 3rem 2rem;
            text-align: center;
        }
        .services-highlight {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            background: #1c1814;
            border-radius: 42px;
            padding: 2.5rem;
        }
        .service-block {
            flex: 1;
            min-width: 280px;
            background: #2a241e;
            padding: 2rem;
            border-radius: 32px;
            text-align: center;
            transition: 0.4s;
        }
        .service-block:hover {
            transform: translateY(-8px);
            background: #332b23;
            box-shadow: 0 20px 30px rgba(212, 175, 55, 0.2);
        }
        .service-block i {
            font-size: 3rem;
            color: var(--gold);
            margin-bottom: 1rem;
        }

        /* Gallery */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 1.8rem;
        }
        .gallery-item {
            border-radius: 28px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        .gallery-item img {
            transition: transform 0.5s ease;
            width: 100%;
            height: 220px;
            object-fit: cover;
        }
        .gallery-item:hover img {
            transform: scale(1.1);
        }

        /* Modals */
        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background: rgba(0, 0, 0, 0.95);
            align-items: center;
            justify-content: center;
            z-index: 2000;
            backdrop-filter: blur(8px);
        }
        .modal-content {
            background: #1f1b16;
            color: #f0e6d2;
            border-radius: 32px;
            width: 90%;
            max-width: 520px;
            max-height: 90vh;
            overflow-y: auto;
            border: 1px solid rgba(212, 175, 55, 0.5);
            padding: 2rem;
        }
        .whatsapp-float {
            position: fixed;
            bottom: 25px;
            right: 25px;
            background: #25D366;
            color: white;
            width: 62px;
            height: 62px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            box-shadow: 0 8px 25px rgba(37, 211, 102, 0.6);
            z-index: 9999;
            animation: pulse 2s infinite;
            transition: 0.2s;
        }
        .whatsapp-float:hover {
            transform: scale(1.08);
            background: #20b859;
        }
        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.6); }
            70% { box-shadow: 0 0 0 15px rgba(37, 211, 102, 0); }
            100% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0); }
        }
        footer {
            background: #050403;
            padding: 3rem 5% 1.5rem;
            color: #aa9f7f;
            text-align: center;
        }
        .footer-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            flex-wrap: wrap;
            margin: 2rem 0;
        }
        @media (max-width: 992px) {
            .nav-links { display: none; flex-direction: column; position: absolute; top: 100%; left: 0; width: 100%; background: #0a0806e6; backdrop-filter: blur(12px); padding: 2rem 5%; gap: 1.5rem; }
            .nav-links.active { display: flex; }
            .hamburger { display: block; }
            .hero-content h1 { font-size: 2.8rem; }
            .section-title { font-size: 2.5rem; }
            .logo-img { width: 70px; height: 70px; }
            .logo-text h1 { font-size: 1.6rem; }
        }
    </style>
</head>
<body>

<nav class="navbar">
    <div class="nav-container">
        <div class="logo-area">
            <div class="logo-img">
                <img src="/rapids.html/fremiot logo.jpg" alt="Fremiot Logo" onerror="this.src='https://placehold.co/85x85/2a241e/FFD966?text=F'">
            </div>
            <div class="logo-text">
                <h1>FREMIOT</h1>
                <p>FOOD NEST & BEAUTY PARLOR</p>
            </div>
        </div>
        <ul class="nav-links" id="navLinks">
            <li><a href="#home">Home</a></li>
            <li><a href="#restaurant">Restaurant</a></li>
            <li><a href="#drinks">Drinks</a></li>
            <li><a href="#salon">Beauty</a></li>
            <li><a href="#delivery">Delivery</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <div style="display: flex; align-items: center; gap: 1.5rem;">
            <div class="cart-icon" onclick="showCart()">
                <i class="fas fa-shopping-cart"></i>
                <span class="cart-count" id="cartCount">0</span>
            </div>
            <i class="fas fa-bars hamburger" onclick="toggleMobileMenu()"></i>
        </div>
    </div>
</nav>

<section id="home" class="hero">
    <div class="hero-content">
    <h1>TASTE  THE EXCELLENCE</h1>
        <p>Luxury Ugandan dining • Signature Luwombo • Corporate catering • Premium beauty & wellness in Kiwatule, Kampala</p>
        <div class="hero-buttons">
            <a href="#restaurant" class="btn-gold"><i class="fas fa-utensils"></i> Explore Menu & Order</a>
            <a href="#salon" class="btn-outline-gold"><i class="fas fa-spa"></i> Book Beauty</a>
        </div>
        <div style="margin-top: 2rem; font-size: 0.95rem;"><i class="fas fa-truck"></i> Free delivery in Kiwatule & surrounding • Open daily 24/7</div>
    </div>
</section>

<!-- RESTAURANT SECTION with LOCAL UGANDAN FOOD + LUWOMBO -->
<section id="restaurant" class="section">
    <h2 class="section-title">Fremiot Food Nest</h2>
    <div class="subtitle">Authentic Ugandan Flavors • Fresh Ingredients • Royal Taste</div>
    <div style="display: flex; justify-content: center; gap: 1rem; flex-wrap: wrap; margin-bottom: 2rem;">
        <button onclick="filterMeal('all')" class="btn-gold" id="filter-all">All</button>
        <button onclick="filterMeal('breakfast')" class="btn-outline-gold">Breakfast</button>
        <button onclick="filterMeal('lunch')" class="btn-outline-gold">Lunch</button>
        <button onclick="filterMeal('dinner')" class="btn-outline-gold">Dinner</button>
    </div>
    <div id="restaurant-menu-container" class="grid-3"></div>

    <!-- Signature Luwombo Trio (explicit local pride) -->
    <div class="special-banner">
        <h2 style="color: var(--gold); font-size: 2.4rem;">✨ Our Legendary Luwombo ✨</h2>
        <p style="font-size: 1.2rem; margin-bottom: 2rem;">Steamed in banana leaves – authentic Ugandan heritage</p>
        <div class="grid-3">
            <div class="card"><img src="https://images.unsplash.com/photo-1555396273-367ea4eb4db5?w=800" alt="Chicken Luwombo"><div class="card-content"><h3>Chicken Luwombo</h3><div class="price">UGX 17,000</div><p>Tender chicken, groundnut sauce, spices</p><button class="btn-cart" onclick="addToCartDirect('Chicken Luwombo', 17000)">Add to Cart</button></div></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1603133872878-684f208fb84b?w=800" alt="Goat Luwombo"><div class="card-content"><h3>Goat Luwombo</h3><div class="price">UGX 17,000</div><p>Rich goat meat, aromatic banana leaf steam</p><button class="btn-cart" onclick="addToCartDirect('Goat Luwombo', 17000)">Add to Cart</button></div></div>
            <div class="card"><img src="https://images.unsplash.com/photo-1625938144755-6d68c9d16ccb?w=800" alt="Groundnut Luwombo"><div class="card-content"><h3>Groundnut Luwombo (Veg)</h3><div class="price">UGX 13,000</div><p>Creamy groundnut sauce, vegetarian delight</p><button class="btn-cart" onclick="addToCartDirect('Groundnut Luwombo', 13000)">Add to Cart</button></div></div>
        </div>
    </div>

    <!-- Additional local Ugandan food showcase -->
    <div style="margin-top: 3rem; text-align: center;">
        <h3 style="color: var(--gold-dark); font-size: 2rem;">🇺🇬 More Ugandan Classics</h3>
        <div class="grid-3" id="local-specials"></div>
    </div>
</section>

<!-- DRINKS MENU (Modern) -->
<section id="drinks" class="section section-dark">
    <h2 class="section-title">Refreshing Drinks Menu</h2>
    <div class="subtitle">Fresh juices • Sodas • Traditional Brews • Mocktails</div>
    <div id="drinks-container" class="grid-4"></div>
</section>

<!-- DELIVERY & CATERING -->
<section id="delivery" class="section section-dark">
    <h2 class="section-title">Delivery & Outside Catering</h2>
    <div class="services-highlight">
        <div class="service-block"><i class="fas fa-truck-fast"></i><h3>Free Delivery</h3><p>Kiwatule, Ntinda, Kisaasi & Kulambiro within 35min</p><span style="color:var(--gold);">Min UGX 25,000</span></div>
        <div class="service-block"><i class="fas fa-building"></i><h3>Corporate Lunch Plans</h3><p>Weekly subscriptions, staff meals.</p><button onclick="location.href='#contact'" class="btn-book" style="margin-top:1rem;">Get Quote</button></div>
        <div class="service-block"><i class="fas fa-party-horn"></i><h3>Events & Catering</h3><p>Weddings, birthdays, corporate events</p></div>
    </div>
</section>

<!-- BEAUTY PARLOR -->
<section id="salon" class="section" style="background: #fef7e8;">
    <h2 class="section-title" style="color:#997a00;">Fremiot Beauty Parlor</h2>
    <div class="subtitle">Glamour • Professional Care • Modern African Beauty</div>
    <div id="beauty-services-container" class="grid-4"></div>
    <div style="text-align:center; margin-top: 3rem; background:#1f1b14; color:#f0e6d2; border-radius:32px; padding:2rem;">
        <i class="fas fa-phone-alt" style="font-size:2rem; color:var(--gold);"></i> <strong>Beauty Hotline:</strong> 0778 214 409
    </div>
</section>

<!-- GALLERY -->
<section class="section section-dark">
    <h2 class="section-title">Moments of Excellence</h2>
    <div class="gallery-grid">
        <div class="gallery-item"><img src="https://images.unsplash.com/photo-1555396273-367ea4eb4db5?w=800" alt="Luwombo"></div>
        <div class="gallery-item"><img src="https://images.unsplash.com/photo-1603133872878-684f208fb84b?w=800" alt="Pilau"></div>
        <div class="gallery-item"><img src="https://images.unsplash.com/photo-1562322140-8baeececf3df?w=800" alt="Hair"></div>
        <div class="gallery-item"><img src="https://images.unsplash.com/photo-1519677100203-a0e668c92439?w=800" alt="Bridal"></div>
        <div class="gallery-item"><img src="https://images.unsplash.com/photo-1570172619644-dfd03ed5d881?w=800" alt="Facial"></div>
        <div class="gallery-item"><img src="https://images.unsplash.com/photo-1544025162-d76694265947?w=800" alt="Grilled Fish"></div>
    </div>
</section>

<!-- CONTACT -->
<section id="contact" class="section section-dark">
    <h2 class="section-title">Visit or Connect</h2>
    <div style="max-width:1200px; margin:0 auto; display:grid; grid-template-columns:repeat(auto-fit, minmax(320px,1fr)); gap:3rem;">
        <div><iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3985.9999999999995!2d32.628!3d0.368!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x177d9f2d2f2f2f2f%3A0x1234567890abcdef!2sKiwatule%2C%20Kampala!5e0!3m2!1sen!2sug!4v1710000000000" width="100%" height="380" style="border:0; border-radius:28px;" loading="lazy"></iframe></div>
        <div style="background:#1c1812; padding:2.5rem; border-radius:32px;">
            <div><i class="fas fa-map-pin" style="color:var(--gold);"></i> <strong>Kiwatule, opposite PK Supermarket</strong></div>
            <div><i class="fas fa-phone" style="color:var(--gold);"></i> <strong>Restaurant:</strong> 0791 433 433 / 0754 336 053</div>
            <div><i class="fas fa-cut" style="color:var(--gold);"></i> <strong>Beauty:</strong> 0778 214 409</div>
            <div><i class="fas fa-envelope" style="color:var(--gold);"></i> kaijadavidfremiot@gmail.com</div>
            <div class="social-icons" style="text-align:center; margin-top:2rem; font-size:2rem;">
                <a href="#" style="color:var(--gold); margin:0 12px;"><i class="fab fa-facebook-f"></i></a>
                <a href="#" style="color:var(--gold); margin:0 12px;"><i class="fab fa-instagram"></i></a>
                <a href="#" style="color:var(--gold); margin:0 12px;"><i class="fab fa-whatsapp"></i></a>
            </div>
        </div>
    </div>
</section>
<footer><p>© 2026 Fremiot Food Nest & Beauty Parlor • Taste the Excellence • Feel the Glamour</p><div class="footer-links"><a href="#restaurant" style="color:#aa9f7f;">Menu</a><a href="#drinks" style="color:#aa9f7f;">Drinks</a><a href="#salon" style="color:#aa9f7f;">Beauty</a><a href="#contact" style="color:#aa9f7f;">Location</a></div></footer>

<!-- Cart Modal & Booking Modal -->
<div id="cartModal" class="modal"><div class="modal-content"><h2 style="color:var(--gold);">Your Order</h2><div id="cartItemsList"></div><hr><div style="font-size:1.3rem;">Total: UGX <span id="cartTotal">0</span></div><div style="display:flex; gap:1rem; margin-top:1.5rem;"><button class="btn-gold" onclick="checkout()">Checkout via WhatsApp</button><button class="btn-outline-gold" onclick="closeCart()">Close</button></div></div></div>
<div id="bookingModal" class="modal"><div class="modal-content"><h2>Book Appointment</h2><form id="bookingForm"><input type="hidden" id="bookItemName"><input type="text" id="custName" placeholder="Full Name" required><input type="tel" id="custPhone" placeholder="Phone Number" required><input type="datetime-local" id="bookingTime" required><button type="submit" class="btn-gold">Confirm Booking</button></form><div id="bookingMsg"></div><button onclick="closeModal()" class="btn-outline-gold" style="margin-top:1rem;">Close</button></div></div>
<a href="https://wa.me/256791433433" target="_blank" class="whatsapp-float"><i class="fab fa-whatsapp"></i></a>

<script>
    // ---------- UPDATED FULL MENU (local Ugandan food) ----------
    const restaurantMenu = [
        { name: "French toasted bread", category: "breakfast", desc: "Eggs, bacon, sausages, beans, toast", price: 8000, img: "https://images.unsplash.com/photo-1533089860892-a7c6f0a88666?w=800" },
        { name: "Ugandan Rolex", category: "breakfast", desc: "Chapati rolled with eggs & fresh veg", price: 8000, img: "https://images.unsplash.com/photo-1633321702518-7feccafb94d5?w=800" },
        { name: "Chicken Pilau", category: "breakfast", desc: "Traditional morning staple", price: 12000, img: "https://images.unsplash.com/photo-1603133872878-684f208fb84b?w=800" },
        { name: "Beef Pilau", category: "lunch", desc: "Fragrant rice with spiced beef", price: 18000, img: "https://images.unsplash.com/photo-1603133872878-684f208fb84b?w=800" },
        { name: "Matooke & Beef Stew", category: "lunch", desc: "Steamed in  bananas leaves + rich beef", price: 16000, img: "https://images.unsplash.com/photo-1625938144755-6d68c9d16ccb?w=800" },
        { name: "Tilapia Fish fillet & 🍟chips ", category: "lunch", desc: " style Fish fillet with chips", price: 22000, img: "https://images.unsplash.com/photo-1544025162-d76694265947?w=800" },
        { name: "Groundnut Sauce with Rice", category: "lunch", desc: "Creamy groundnut, steamed rice", price: 11000, img: "https://images.unsplash.com/photo-1625938144755-6d68c9d16ccb?w=800" },
        { name: "Luwombo Feast Mix", category: "dinner", desc: "Chicken & goat, sides & posho", price: 20000, img: "https://images.unsplash.com/photo-1555396273-367ea4eb4db5?w=800" },
        { name: "Grilled Pork Chops", category: "dinner", desc: "Marinated pork, sauteed veg", price: 22000, img: "https://images.unsplash.com/photo-1544025162-d76694265947?w=800" },
        { name: "Ugandan Samosas (3pcs)", category: "dinner", desc: "Spiced meat/veg pastry", price: 9000, img: "https://images.unsplash.com/photo-1601050690597-df0568f70950?w=800" }
    ];

    const drinksMenu = [
        { name: "Fresh Passion Juice", price: 7000, desc: "Natural passion fruit blend", img: "https://images.unsplash.com/photo-1621263764928-df1444c5e859?w=800" },
        { name: "Mango Tango Smoothie", price: 8500, desc: "Ripe mango & yoghurt", img: "https://images.unsplash.com/photo-1623065422902-30a2d299e4cd?w=800" },
        { name: "Ginger Lemongrass Tea", price: 5000, desc: "Local herbal infusion", img: "https://images.unsplash.com/photo-1544787219-7f47ccb76574?w=800" },
        { name: "Ugandan Masala Chai", price: 4000, desc: "Spiced milk tea", img: "https://images.unsplash.com/photo-1564890369478-c89ca6d9cde9?w=800" },
        { name: "Soda (Coke/Fanta/Sprite)", price: 3000, desc: "Chilled bottle", img: "https://images.unsplash.com/photo-1622484214935-6fcb1f6dcbf0?w=800" },
        { name: "Waragi Cocktail", price: 12000, desc: "Ugandan gin special", img: "https://images.unsplash.com/photo-1514362545857-3bc16c4c7d1b?w=800" },
        { name: "Bottled Water", price: 2000, desc: "Pure & fresh", img: "https://images.unsplash.com/photo-1560022777-0d3bcf3d4f6e?w=800" },
        { name: "Omubisi (Fermented Cane)", price: 8000, desc: "Traditional brew", img: "https://images.unsplash.com/photo-1596803244618-8dbee5e3c3f4?w=800" }
    ];

    const beautyServices = [
        { name: "Hair Blowout & Style", price: 45000, desc: "Professional blow-dry, smooth finish", img: "https://images.unsplash.com/photo-1562322140-8baeececf3df?w=800" },
        { name: "Signature Haircut & Fade", price: 30000, desc: "Precision cuts", img: "https://images.unsplash.com/photo-1585747860715-2ba37e788b70?w=800" },
        { name: "Bridal Beauty Package", price: 150000, desc: "Makeup+hairstyle+facial+nails", img: "https://images.unsplash.com/photo-1519677100203-a0e668c92439?w=800" },
        { name: "Gel Manicure & Nail Art", price: 35000, desc: "Long-lasting design", img: "https://images.unsplash.com/photo-1610992385407-60dafd24afb6?w=800" },
        { name: "Luxury Pedicure Spa", price: 40000, desc: "Foot soak, scrub, massage", img: "https://images.unsplash.com/photo-1549305443-1e06b2f6f7ae?w=800" },
        { name: "Deep Cleansing Facial", price: 70000, desc: "Vitamin C glow", img: "https://images.unsplash.com/photo-1570172619644-dfd03ed5d881?w=800" },
        { name: "Full Glam Makeup", price: 80000, desc: "Airbrush event makeup", img: "https://images.unsplash.com/photo-1487412947147-5cebf100ffc2?w=800" }
    ];

    let cart = [];

    function renderRestaurant(filter = 'all') {
        const container = document.getElementById('restaurant-menu-container');
        if(!container) return;
        let items = filter === 'all' ? restaurantMenu : restaurantMenu.filter(i => i.category === filter);
        container.innerHTML = items.map(item => `
            <div class="card"><img src="${item.img}" onerror="this.src='https://placehold.co/400x220/1f1b14/gold?text=Fremiot'"><div class="card-content"><h3>${item.name}</h3><p>${item.desc}</p><div class="price">UGX ${item.price.toLocaleString()}</div><button class="btn-cart" onclick="addToCartDirect('${item.name.replace(/'/g, "\\'")}', ${item.price})">Add to Cart</button><button class="btn-book" onclick="openBookingModal('${item.name.replace(/'/g, "\\'")}', 'restaurant')">Book Table</button></div></div>
        `).join('');
    }

    function renderDrinks() {
        const container = document.getElementById('drinks-container');
        if(container) container.innerHTML = drinksMenu.map(d => `
            <div class="card"><img src="${d.img}" onerror="this.src='https://placehold.co/400x220'"><div class="card-content"><h3>${d.name}</h3><p>${d.desc}</p><div class="price">UGX ${d.price.toLocaleString()}</div><button class="btn-cart" onclick="addToCartDirect('${d.name.replace(/'/g, "\\'")}', ${d.price})">Add to Cart</button></div></div>
        `).join('');
    }

    function renderBeauty() {
        const container = document.getElementById('beauty-services-container');
        if(container) container.innerHTML = beautyServices.map(s => `
            <div class="card"><img src="${s.img}" onerror="this.src='https://placehold.co/400x220'"><div class="card-content"><h3>${s.name}</h3><p>${s.desc}</p><div class="price">UGX ${s.price.toLocaleString()}</div><button class="btn-book" onclick="openBookingModal('${s.name.replace(/'/g, "\\'")}', 'beauty')">Book Appointment</button></div></div>
        `).join('');
    }

    function renderLocalSpecials() {
        const specials = [
            { name: "Rolex (Chapati & Eggs)", price: 8000, img: "https://images.unsplash.com/photo-1633321702518-7feccafb94d5?w=800", desc: "Street classic" },
            { name: "Matooke & Groundnuts", price: 13000, img: "https://images.unsplash.com/photo-1625938144755-6d68c9d16ccb?w=800", desc: "Steamed matooke, rich peanut sauce" },
            { name: "Ugali & Fish Stew", price: 18000, img: "https://images.unsplash.com/photo-1544025162-d76694265947?w=800", desc: "Posho with tilapia stew" }
        ];
        const container = document.getElementById('local-specials');
        if(container) container.innerHTML = specials.map(s => `
            <div class="card"><img src="${s.img}" onerror="this.src='https://placehold.co/400x220'"><div class="card-content"><h3>${s.name}</h3><p>${s.desc}</p><div class="price">UGX ${s.price.toLocaleString()}</div><button class="btn-cart" onclick="addToCartDirect('${s.name.replace(/'/g, "\\'")}', ${s.price})">Add to Cart</button></div></div>
        `).join('');
    }

    window.addToCartDirect = (name, price) => {
        cart.push({ name, price, id: Date.now() + Math.random() });
        updateCartCount();
        alert(`✅ ${name} added to cart!`);
    };

    function updateCartCount() {
        document.getElementById('cartCount').innerText = cart.length;
    }

    window.showCart = () => {
        const modal = document.getElementById('cartModal');
        const listDiv = document.getElementById('cartItemsList');
        if(cart.length === 0) { listDiv.innerHTML = '<p>Your cart is empty.</p>'; document.getElementById('cartTotal').innerText = '0'; modal.style.display = 'flex'; return; }
        listDiv.innerHTML = cart.map((item, idx) => `<div style="display:flex; justify-content:space-between; border-bottom:1px solid #555; padding:8px 0;"><span>${item.name}</span><span>UGX ${item.price.toLocaleString()}</span><button onclick="removeFromCart(${idx})" style="background:crimson; border:none; color:white; border-radius:20px; padding:4px 10px;">Remove</button></div>`).join('');
        const total = cart.reduce((sum, i) => sum + i.price, 0);
        document.getElementById('cartTotal').innerText = total.toLocaleString();
        modal.style.display = 'flex';
    };
    window.removeFromCart = (idx) => { cart.splice(idx,1); updateCartCount(); showCart(); };
    window.closeCart = () => document.getElementById('cartModal').style.display = 'none';
    window.checkout = () => {
        if(cart.length === 0) return alert('Cart empty');
        let msg = `Hello Fremiot, I'd like to order:\n${cart.map(i=>`- ${i.name} (UGX ${i.price})`).join('\n')}\nTotal: UGX ${cart.reduce((s,i)=>s+i.price,0).toLocaleString()}`;
        window.open(`https://wa.me/256791433433?text=${encodeURIComponent(msg)}`, '_blank');
        cart = []; updateCartCount(); closeCart(); alert('Order forwarded to WhatsApp!');
    };
    window.openBookingModal = (itemName, type) => {
        document.getElementById('bookItemName').value = `${itemName} (${type})`;
        document.getElementById('bookingModal').style.display = 'flex';
    };
    window.closeModal = () => document.getElementById('bookingModal').style.display = 'none';
    window.filterMeal = (cat) => { renderRestaurant(cat); };
    window.toggleMobileMenu = () => document.getElementById('navLinks').classList.toggle('active');

    document.getElementById('bookingForm')?.addEventListener('submit', (e) => {
        e.preventDefault();
        const name = document.getElementById('custName').value;
        const phone = document.getElementById('custPhone').value;
        const time = document.getElementById('bookingTime').value;
        const service = document.getElementById('bookItemName').value;
        if(!name || !phone || !time) { alert("Please fill all fields"); return; }
        const msg = `Booking: ${service}\nName: ${name}\nPhone: ${phone}\nDateTime: ${time}`;
        window.open(`https://wa.me/256791433433?text=${encodeURIComponent(msg)}`, '_blank');
        document.getElementById('bookingMsg').innerHTML = '<span style="color:#a5d6a5;">✓ Request sent! We will contact you.</span>';
        setTimeout(() => { closeModal(); document.getElementById('bookingForm').reset(); document.getElementById('bookingMsg').innerHTML = ''; }, 2000);
    });

    window.onload = () => {
        renderRestaurant('all');
        renderDrinks();
        renderBeauty();
        renderLocalSpecials();
        updateCartCount();
        document.querySelectorAll('a[href^="#"]').forEach(anchor => anchor.addEventListener('click', function(e) {
            if(this.getAttribute('href') !== '#') { e.preventDefault(); const target = document.querySelector(this.getAttribute('href')); if(target) target.scrollIntoView({ behavior: 'smooth' }); }
            document.getElementById('navLinks')?.classList.remove('active');
        }));
    };
</script>
</body>
</html>
