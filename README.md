<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RFMS - Royal Facility Management Services</title>
    <!-- Google Fonts & FontAwesome for icons -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary: #0a369d;
            --primary-dark: #051c52;
            --accent: #d4af37; /* Elegant gold tone */
            --glass-bg: rgba(255, 255, 255, 0.75);
            --glass-border: rgba(255, 255, 255, 0.6);
            --text-dark: #0f172a;
            --text-light: #475569;
            --white: #ffffff;
            --transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            color: var(--text-dark);
            background: linear-gradient(135deg, #f0f4f8 0%, #dbeafe 100%);
            min-height: 100vh;
            line-height: 1.6;
            scroll-behavior: smooth;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            list-style: none;
        }

        /* Top Bar */
        .top-bar {
            background-color: var(--primary-dark);
            color: var(--white);
            font-size: 0.85rem;
            padding: 10px 0;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
        }

        .top-bar .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .top-bar-info span {
            margin-right: 20px;
        }

        .top-bar-info i {
            color: var(--accent);
            margin-right: 6px;
        }

        /* Header & Navbar - Glassmorphism */
        header {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            box-shadow: 0 8px 32px 0 rgba(10, 54, 157, 0.08);
            border-bottom: 1px solid rgba(255, 255, 255, 0.4);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            max-width: 1200px;
            margin: 0 auto;
            padding: 15px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            flex-direction: column;
        }

        .logo-text {
            font-size: 1.8rem;
            font-weight: 800;
            color: var(--primary);
            letter-spacing: 1px;
            text-shadow: 0 2px 4px rgba(10, 54, 157, 0.1);
        }

        .logo-sub {
            font-size: 0.75rem;
            font-weight: 600;
            color: var(--text-light);
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .nav-links {
            display: flex;
            gap: 30px;
            align-items: center;
        }

        .nav-links a {
            font-weight: 500;
            color: var(--text-dark);
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .btn-cta {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: var(--white) !important;
            padding: 10px 24px;
            border-radius: 50px;
            font-weight: 600;
            transition: var(--transition);
            box-shadow: 0 4px 15px rgba(10, 54, 157, 0.3);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .btn-cta:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(10, 54, 157, 0.4);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, rgba(5, 28, 82, 0.9), rgba(10, 54, 157, 0.85)), url('https://images.unsplash.com/photo-1581578731548-c64695cc6952?auto=format&fit=crop&w=1920&q=80') no-repeat center center/cover;
            color: var(--white);
            padding: 120px 20px 140px;
            text-align: center;
            position: relative;
            box-shadow: inset 0 0 50px rgba(0,0,0,0.3);
        }

        .hero-badge {
            display: inline-block;
            background: rgba(212, 175, 55, 0.15);
            backdrop-filter: blur(8px);
            border: 1px solid var(--accent);
            color: #fef08a;
            padding: 8px 20px;
            border-radius: 30px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 25px;
            text-transform: uppercase;
            letter-spacing: 1px;
            box-shadow: 0 4px 15px rgba(212, 175, 55, 0.2);
        }

        .hero h1 {
            font-size: 3.2rem;
            font-weight: 800;
            margin-bottom: 20px;
            line-height: 1.2;
            text-shadow: 0 4px 12px rgba(0,0,0,0.3);
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 35px;
            color: #e2e8f0;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            justify-content: center;
        }

        .btn-outline {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(8px);
            border: 2px solid rgba(255, 255, 255, 0.8);
            color: var(--white);
            padding: 10px 25px;
            border-radius: 50px;
            font-weight: 600;
            transition: var(--transition);
        }

        .btn-outline:hover {
            background: var(--white);
            color: var(--primary);
        }

        /* Services Section */
        .section {
            padding: 100px 20px;
            max-width: 1250px;
            margin: 0 auto;
        }

        .section-header {
            text-align: center;
            margin-bottom: 70px;
        }

        .section-header h2 {
            font-size: 2.5rem;
            font-weight: 800;
            color: var(--primary);
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .section-header p {
            color: var(--text-light);
            font-size: 1.1rem;
        }

        /* Perfect Centered Grid using auto-fit and max-width alignment */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 360px));
            justify-content: center;
            justify-items: center;
            gap: 35px;
            margin-bottom: 60px;
        }

        /* Glassmorphic Service Card */
        .service-card {
            background: rgba(255, 255, 255, 0.65);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border-radius: 20px;
            padding: 40px 30px;
            text-align: center;
            transition: var(--transition);
            border: 1px solid rgba(255, 255, 255, 0.8);
            position: relative;
            overflow: hidden;
            cursor: pointer;
            box-shadow: 0 10px 30px 0 rgba(31, 38, 135, 0.07);
            width: 100%;
            max-width: 360px;
        }

        .service-card:hover {
            transform: translateY(-10px) scale(1.02);
            background: rgba(255, 255, 255, 0.9);
            box-shadow: 0 20px 40px 0 rgba(10, 54, 157, 0.15);
            border-color: rgba(212, 175, 55, 0.5);
        }

        .service-card::after {
            content: 'Click to view gallery';
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: var(--white);
            font-size: 0.8rem;
            font-weight: 600;
            padding: 8px;
            transform: translateY(100%);
            transition: var(--transition);
            letter-spacing: 0.5px;
        }

        .service-card:hover::after {
            transform: translateY(0);
        }

        .service-icon {
            width: 75px;
            height: 75px;
            background: linear-gradient(135deg, rgba(10, 54, 157, 0.1), rgba(212, 175, 55, 0.15));
            color: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
            margin: 0 auto 25px;
            transition: var(--transition);
            box-shadow: inset 0 2px 5px rgba(255,255,255,0.8);
        }

        .service-card:hover .service-icon {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: var(--white);
            transform: rotateY(360deg);
        }

        .service-card h3 {
            font-size: 1.35rem;
            font-weight: 700;
            margin-bottom: 12px;
            color: var(--text-dark);
        }

        .service-card p {
            color: var(--text-light);
            font-size: 0.95rem;
        }

        /* Glassmorphic Contracts & Payment Banner - Center Aligned */
        .contracts-banner {
            background: rgba(255, 255, 255, 0.75);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.9);
            border-top: 4px solid var(--accent);
            padding: 50px 40px;
            border-radius: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            gap: 30px;
            max-width: 900px;
            margin: 60px auto 0;
            box-shadow: 0 15px 35px rgba(10, 54, 157, 0.08);
        }

        .contracts-content h3 {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 10px;
        }

        .contracts-content p {
            color: var(--text-light);
            font-size: 1.1rem;
            max-width: 700px;
        }

        .payment-box {
            background: rgba(255, 255, 255, 0.9);
            padding: 20px 40px;
            border-radius: 14px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.05);
            text-align: center;
            border: 1px solid rgba(212, 175, 55, 0.4);
        }

        .payment-box h4 {
            font-size: 0.85rem;
            text-transform: uppercase;
            color: var(--text-light);
            letter-spacing: 1px;
            margin-bottom: 6px;
        }

        .payment-box p {
            font-size: 1.4rem;
            font-weight: 700;
            color: var(--primary);
        }

        /* Glassmorphic Modal / Gallery Popup */
        .modal-overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(15, 23, 42, 0.6);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 2000;
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
            backdrop-filter: blur(8px);
            -webkit-backdrop-filter: blur(8px);
            padding: 20px;
        }

        .modal-overlay.active {
            opacity: 1;
            visibility: visible;
        }

        .modal-container {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            width: 100%;
            max-width: 850px;
            border-radius: 24px;
            overflow: hidden;
            transform: scale(0.95) translateY(20px);
            transition: var(--transition);
            box-shadow: 0 25px 60px rgba(10, 54, 157, 0.3);
            border: 1px solid rgba(255, 255, 255, 1);
            max-height: 90vh;
            display: flex;
            flex-direction: column;
        }

        .modal-overlay.active .modal-container {
            transform: scale(1) translateY(0);
        }

        .modal-header {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: var(--white);
            padding: 24px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .modal-header h3 {
            font-size: 1.6rem;
            font-weight: 700;
            text-shadow: 0 2px 4px rgba(0,0,0,0.2);
        }

        .modal-close {
            background: rgba(255,255,255,0.2);
            border: none;
            color: var(--white);
            width: 38px;
            height: 38px;
            border-radius: 50%;
            font-size: 1.2rem;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }

        .modal-close:hover {
            background: var(--accent);
            color: var(--primary-dark);
            transform: rotate(90deg);
        }

        .modal-body {
            padding: 35px;
            overflow-y: auto;
        }

        .modal-description {
            font-size: 1.1rem;
            color: var(--text-light);
            margin-bottom: 30px;
        }

        .modal-gallery-title {
            font-size: 1.15rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 18px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .modal-gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
            gap: 20px;
        }

        .modal-img-card {
            border-radius: 14px;
            overflow: hidden;
            box-shadow: 0 8px 20px rgba(0,0,0,0.08);
            background: #e2e8f0;
            height: 190px;
            position: relative;
            border: 2px solid var(--white);
        }

        .modal-img-card img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .modal-img-card:hover img {
            transform: scale(1.08);
        }

        .modal-img-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            background: linear-gradient(to top, rgba(5, 28, 82, 0.85), transparent);
            color: var(--white);
            padding: 15px 12px 10px;
            font-size: 0.9rem;
            font-weight: 500;
        }

        /* Glassmorphic About Section */
        .about-section {
            background: rgba(255, 255, 255, 0.5);
            backdrop-filter: blur(12px);
            padding: 100px 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.6);
            border-bottom: 1px solid rgba(255, 255, 255, 0.6);
        }

        .about-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text h2 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 20px;
            font-weight: 800;
        }

        .about-text p {
            color: var(--text-light);
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .founder-card {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(16px);
            padding: 35px;
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(10, 54, 157, 0.08);
            display: flex;
            align-items: center;
            gap: 25px;
            border: 1px solid rgba(255, 255, 255, 0.9);
        }

        .founder-avatar {
            width: 75px;
            height: 75px;
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: var(--white);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            font-weight: 700;
            box-shadow: 0 8px 20px rgba(10, 54, 157, 0.3);
        }

        .founder-info h4 {
            font-size: 1.3rem;
            color: var(--text-dark);
            margin-bottom: 4px;
        }

        .founder-info span {
            color: var(--accent);
            font-weight: 700;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* Glassmorphic Footer */
        footer {
            background: var(--primary-dark);
            color: var(--white);
            padding: 90px 20px 30px;
            box-shadow: inset 0 20px 30px rgba(0,0,0,0.2);
        }

        .footer-grid {
            max-width: 1200px;
            margin: 0 auto 50px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
        }

        .footer-col h3 {
            font-size: 1.25rem;
            margin-bottom: 22px;
            color: var(--accent);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .footer-col p, .footer-col li {
            color: #cbd5e1;
            margin-bottom: 12px;
            font-size: 0.95rem;
        }

        .footer-col ul li i {
            color: var(--accent);
            margin-right: 10px;
        }

        .footer-bottom {
            max-width: 1200px;
            margin: 0 auto;
            border-top: 1px solid rgba(255,255,255,0.1);
            padding-top: 25px;
            text-align: center;
            color: #94a3b8;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            .hero h1 {
                font-size: 2.3rem;
            }
            .about-container {
                grid-template-columns: 1fr;
            }
            .top-bar .container {
                flex-direction: column;
                gap: 5px;
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <!-- Top Bar -->
    <div class="top-bar">
        <div class="container">
            <div class="top-bar-info">
                <span><i class="fas fa-phone-alt"></i> 03193065878</span>
                <span><i class="fas fa-envelope"></i> aimgill8026@gmail.com</span>
            </div>
            <div class="top-bar-location">
                <span><i class="fas fa-map-marker-alt"></i> Lahore, Pakistan</span>
            </div>
        </div>
    </div>

    <!-- Header / Navbar -->
    <header>
        <div class="navbar">
            <div class="logo">
                <span class="logo-text">RFMS</span>
                <span class="logo-sub">Royal Facility Management Services</span>
            </div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact" class="btn-cta">Get a Quote</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-badge">Reliable • Professional • Trusted Facility Solutions</div>
        <h1>Annual Cleaning Contracts Available</h1>
        <p>Committed to maintaining clean, safe, and efficient environments for your business and home.</p>
        <div class="hero-buttons">
            <a href="#services" class="btn-cta">Explore Services</a>
            <a href="#contact" class="btn-outline">Contact Us</a>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="section">
        <div class="section-header">
            <h2>Our Professional Services</h2>
            <p>Click any service card below to view detailed photos and gallery.</p>
        </div>

        <div class="services-grid">
            <!-- Service 1 -->
            <div class="service-card" onclick="openServiceModal('office')">
                <div class="service-icon"><i class="fas fa-building"></i></div>
                <h3>Office Cleaning</h3>
                <p>Keep your workspace spotless, hygienic, and conducive to maximum employee productivity.</p>
            </div>
            <!-- Service 2 -->
            <div class="service-card" onclick="openServiceModal('house')">
                <div class="service-icon"><i class="fas fa-home"></i></div>
                <h3>House Cleaning</h3>
                <p>Comprehensive residential cleaning services to keep your home fresh, clean, and welcoming.</p>
            </div>
            <!-- Service 3 -->
            <div class="service-card" onclick="openServiceModal('deep')">
                <div class="service-icon"><i class="fas fa-sparkles"></i></div>
                <h3>Deep Cleaning</h3>
                <p>Thorough top-to-bottom sanitization reaching every hard-to-access corner and surface.</p>
            </div>
            <!-- Service 4 -->
            <div class="service-card" onclick="openServiceModal('glass')">
                <div class="service-icon"><i class="fas fa-window-maximize"></i></div>
                <h3>Glass Cleaning</h3>
                <p>Crystal-clear window and glass partition maintenance for a pristine professional look.</p>
            </div>
            <!-- Service 5 -->
            <div class="service-card" onclick="openServiceModal('carpet')">
                <div class="service-icon"><i class="fas fa-couch"></i></div>
                <h3>Carpet & Sofa Cleaning</h3>
                <p>Advanced stain removal, deep steam cleaning, and fabric refreshing for furniture and flooring.</p>
            </div>
            <!-- Service 6 -->
            <div class="service-card" onclick="openServiceModal('pest')">
                <div class="service-icon"><i class="fas fa-shield-alt"></i></div>
                <h3>Pest Control</h3>
                <p>Safe, effective, and long-lasting pest elimination treatments for homes and businesses.</p>
            </div>
            <!-- Service 7 - Perfectly centered across all screen widths -->
            <div class="service-card" onclick="openServiceModal('janitorial')">
                <div class="service-icon"><i class="fas fa-users-cog"></i></div>
                <h3>Janitorial Staff</h3>
                <p>Trained, reliable, and professional janitorial personnel deployed for ongoing facility upkeep.</p>
            </div>
        </div>

        <!-- Contracts & Payment Banner - Center Aligned -->
        <div class="contracts-banner">
            <div class="contracts-content">
                <h3>Annual Maintenance Contracts (AMC)</h3>
                <p>Secure consistent, top-tier facility care with flexible yearly contracts customized to your needs.</p>
            </div>
            <div class="payment-box">
                <h4>Payment Terms</h4>
                <p>50% Advance for First Month</p>
            </div>
        </div>
    </section>

    <!-- Interactive Modal / Gallery Popup -->
    <div class="modal-overlay" id="serviceModal" onclick="closeServiceModal(event)">
        <div class="modal-container" onclick="event.stopPropagation()">
            <div class="modal-header">
                <h3 id="modalTitle">Service Title</h3>
                <button class="modal-close" onclick="closeModalDirect()"><i class="fas fa-times"></i></button>
            </div>
            <div class="modal-body">
                <p class="modal-description" id="modalDescription">Service description goes here...</p>
                <div class="modal-gallery-title">Service Work Gallery</div>
                <div class="modal-gallery-grid" id="modalGallery">
                    <!-- Images will be injected dynamically via JS -->
                </div>
            </div>
        </div>
    </div>

    <!-- About Section -->
    <section id="about" class="about-section">
        <div class="about-container">
            <div class="about-text">
                <h2>Committed to Excellence</h2>
                <p>At <strong>Royal Facility Management Services (RFMS)</strong>, we take pride in delivering uncompromising quality in facility care. Whether it is routine office upkeep or specialized deep cleaning, our trained professionals handle every task with utmost diligence.</p>
                <p>Our mission is simple: to create clean, safe, and efficient environments that elevate your standard of living and business operations.</p>
            </div>
            <div class="founder-card">
                <div class="founder-avatar">S</div>
                <div class="founder-info">
                    <h4>Saim</h4>
                    <span>Proprietor / Lead</span>
                    <p style="margin-top: 5px; color: var(--text-light); font-size: 0.9rem;">Dedicated to providing trusted facility solutions across Lahore.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Footer -->
    <footer id="contact">
        <div class="footer-grid">
            <div class="footer-col">
                <h3>RFMS</h3>
                <p>Royal Facility Management Services</p>
                <p style="margin-top: 15px; color: #94a3b8;">Committed to maintaining clean, safe, and efficient environments for your business and home.</p>
            </div>
            <div class="footer-col">
                <h3>Quick Links</h3>
                <ul>
                    <li><a href="#home"><i class="fas fa-chevron-right"></i> Home</a></li>
                    <li><a href="#services"><i class="fas fa-chevron-right"></i> Our Services</a></li>
                    <li><a href="#about"><i class="fas fa-chevron-right"></i> About Us</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>Contact Info</h3>
                <ul>
                    <li><i class="fas fa-user"></i> Saim</li>
                    <li><i class="fas fa-phone-alt"></i> 03193065878</li>
                    <li><i class="fas fa-envelope"></i> aimgill8026@gmail.com</li>
                    <li><i class="fas fa-map-marker-alt"></i> Lahore, Pakistan</li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2026 Royal Facility Management Services (RFMS). All Rights Reserved.</p>
        </div>
    </footer>

    <!-- Service Data & Interaction Script -->
    <script>
        const serviceData = {
            office: {
                title: "Office Cleaning",
                description: "Our professional office cleaning services ensure your workspace remains immaculate, organized, and hygienic. We manage desks, conference rooms, reception areas, and restrooms to foster a productive and healthy environment for your staff and clients.",
                images: [
                    { url: "https://images.unsplash.com/photo-1497366216548-37526070297c?auto=format&fit=crop&w=600&q=80", caption: "Corporate Workspace" },
                    { url: "https://images.unsplash.com/photo-1524758631624-e2822e304c36?auto=format&fit=crop&w=600&q=80", caption: "Meeting Room Sanitation" },
                    { url: "https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=600&q=80", caption: "Reception Upkeep" }
                ]
            },
            house: {
                title: "House Cleaning",
                description: "Experience a pristine and stress-free home with our comprehensive residential cleaning solutions. From living rooms and bedrooms to kitchens and bathrooms, our team gives your home the royal treatment it deserves.",
                images: [
                    { url: "https://images.unsplash.com/photo-1584622650111-993a426fbf0a?auto=format&fit=crop&w=600&q=80", caption: "Living Room Cleaning" },
                    { url: "https://images.unsplash.com/photo-1556911220-e15b29be8c8f?auto=format&fit=crop&w=600&q=80", caption: "Kitchen Sanitization" },
                    { url: "https://images.unsplash.com/photo-1585421514284-efb74c2b69ba?auto=format&fit=crop&w=600&q=80", caption: "Bedroom Care" }
                ]
            },
            deep: {
                title: "Deep Cleaning",
                description: "Our deep cleaning service reaches every neglected corner, high fixture, baseboard, and hidden surface. Ideal for seasonal refreshes, post-renovation, or move-in/move-out readiness.",
                images: [
                    { url: "https://images.unsplash.com/photo-1628177142898-93e36e4e3a50?auto=format&fit=crop&w=600&q=80", caption: "Detailed Scrubbing" },
                    { url: "https://images.unsplash.com/photo-1581578731548-c64695cc6952?auto=format&fit=crop&w=600&q=80", caption: "Top-to-Bottom Care" },
                    { url: "https://images.unsplash.com/photo-1527515637462-cff94eecc1ac?auto=format&fit=crop&w=600&q=80", caption: "Surface Sanitization" }
                ]
            },
            glass: {
                title: "Glass Cleaning",
                description: "Achieve crystal-clear visibility with our specialized window and glass partition cleaning. We eliminate smudges, streaks, dust, and water marks to enhance natural lighting and professional aesthetics.",
                images: [
                    { url: "https://images.unsplash.com/photo-1513694203232-719a280e022f?auto=format&fit=crop&w=600&q=80", caption: "Glass Partition Polish" },
                    { url: "https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?auto=format&fit=crop&w=600&q=80", caption: "Exterior Window Maintenance" },
                    { url: "https://images.unsplash.com/photo-1545324418-cc1a3fa10c00?auto=format&fit=crop&w=600&q=80", caption: "Streak-Free Finish" }
                ]
            },
            carpet: {
                title: "Carpet & Sofa Cleaning",
                description: "Revive your upholstered furniture and carpets with our deep steam cleaning and advanced stain removal techniques. We extract deep-seated dirt, allergens, and odors to restore fabric vibrancy.",
                images: [
                    { url: "https://images.unsplash.com/photo-1555041469-a586c61ea9bc?auto=format&fit=crop&w=600&q=80", caption: "Sofa Steam Cleaning" },
                    { url: "https://images.unsplash.com/photo-1563453392212-326f5e854473?auto=format&fit=crop&w=600&q=80", caption: "Carpet Stain Treatment" },
                    { url: "https://images.unsplash.com/photo-1540555700478-4be289fbecef?auto=format&fit=crop&w=600&q=80", caption: "Upholstery Refresh" }
                ]
            },
            pest: {
                title: "Pest Control",
                description: "Protect your property from unwanted intruders with our safe, odorless, and certified pest management treatments. Effective against crawling and flying pests for homes and offices.",
                images: [
                    { url: "https://images.unsplash.com/photo-1584467735811-62848fc4a759?auto=format&fit=crop&w=600&q=80", caption: "Safe Treatment Application" },
                    { url: "https://images.unsplash.com/photo-1615870216519-2f9fa575fa5c?auto=format&fit=crop&w=600&q=80", caption: "Preventive Inspection" },
                    { url: "https://images.unsplash.com/photo-1530595467537-0b5996c41f2d?auto=format&fit=crop&w=600&q=80", caption: "Pest Elimination" }
                ]
            },
            janitorial: {
                title: "Janitorial Staff",
                description: "Deploy dependable, vetted, and thoroughly trained janitorial personnel for daily ongoing facility maintenance. Ensure washrooms, corridors, and common spaces remain pristine around the clock.",
                images: [
                    { url: "https://images.unsplash.com/photo-1581578731548-c64695cc6952?auto=format&fit=crop&w=600&q=80", caption: "Dedicated Janitor Team" },
                    { url: "https://images.unsplash.com/photo-1584622650111-993a426fbf0a?auto=format&fit=crop&w=600&q=80", caption: "Corridor & Facility Upkeep" },
                    { url: "https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=600&q=80", caption: "On-Site Management" }
                ]
            }
        };

        function openServiceModal(serviceKey) {
            const data = serviceData[serviceKey];
            if (!data) return;

            document.getElementById('modalTitle').innerText = data.title;
            document.getElementById('modalDescription').innerText = data.description;

            const galleryContainer = document.getElementById('modalGallery');
            galleryContainer.innerHTML = '';

            data.images.forEach(img => {
                const card = document.createElement('div');
                card.className = 'modal-img-card';
                card.innerHTML = `
                    <img src="${img.url}" alt="${img.caption}" onerror="this.src='https://placehold.co/600x400/0a369d/ffffff?text=RFMS+Service'">
                    <div class="modal-img-caption">${img.caption}</div>
                `;
                galleryContainer.appendChild(card);
            });

            document.getElementById('serviceModal').classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function closeModalDirect() {
            document.getElementById('serviceModal').classList.remove('active');
            document.body.style.overflow = 'auto';
        }

        function closeServiceModal(event) {
            if (event.target === document.getElementById('serviceModal')) {
                closeModalDirect();
            }
        }

        // Close modal on ESC key
        document.addEventListener('keydown', function(e) {
            if (e.key === 'Escape') {
                closeModalDirect();
            }
        });
    </script>
</body>
</html>
