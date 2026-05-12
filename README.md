# Baliyan-ghee-2  ```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <title>BALIYAN GHEE | Pure Bilona A2 Cow Ghee by Baliyan Dairy</title>
  <meta name="description" content="BALIYAN GHEE by Baliyan Dairy offers pure Bilona Desi A2 Cow Ghee, traditionally crafted with village purity, rich aroma, granular texture, and no preservatives." />

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@600;700;800&family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">

  <style>
    :root {
      --cream: #fff7e8;
      --milk: #fffdf8;
      --soft: #f4e2bd;
      --gold: #c89635;
      --gold-light: #f3d98b;
      --dark: #35230f;
      --brown: #6f4619;
      --muted: rgba(53, 35, 15, 0.68);
      --shadow: 0 30px 90px rgba(111, 70, 25, 0.16);
      --shadow-strong: 0 35px 110px rgba(111, 70, 25, 0.28);
    }

    * { box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      font-family: Inter, sans-serif;
      background: var(--cream);
      color: var(--dark);
      overflow-x: hidden;
    }

    body.no-scroll { overflow: hidden; }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
      display: block;
    }

    button,
    input,
    textarea {
      font: inherit;
    }

    .container {
      width: min(1180px, 92%);
      margin: auto;
    }

    .loader {
      position: fixed;
      inset: 0;
      z-index: 999;
      display: grid;
      place-items: center;
      background: var(--milk);
      transition: opacity 0.6s ease, visibility 0.6s ease;
    }

    .loader.hide {
      opacity: 0;
      visibility: hidden;
    }

    .loader-ring {
      width: 64px;
      height: 64px;
      border-radius: 50%;
      border: 4px solid rgba(200, 150, 53, 0.25);
      border-top-color: var(--gold);
      animation: spin 1s linear infinite;
      margin: 0 auto 18px;
    }

    .loader-title {
      font-family: Cinzel, serif;
      font-size: 26px;
      font-weight: 800;
      text-align: center;
    }

    @keyframes spin {
      to { transform: rotate(360deg); }
    }

    .navbar {
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 100;
      background: rgba(255, 247, 232, 0.82);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid rgba(200, 150, 53, 0.22);
      transition: 0.3s ease;
    }

    .navbar.scrolled {
      background: rgba(255, 253, 248, 0.92);
      box-shadow: 0 12px 40px rgba(111, 70, 25, 0.12);
    }

    nav {
      height: 78px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 22px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .logo-mark {
      width: 46px;
      height: 46px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: linear-gradient(135deg, #fff, var(--soft));
      border: 1px solid rgba(200, 150, 53, 0.35);
      box-shadow: 0 12px 34px rgba(111, 70, 25, 0.16);
      color: var(--gold);
      font-weight: 900;
    }

    .logo-title {
      font-family: Cinzel, serif;
      font-size: 21px;
      font-weight: 800;
      line-height: 1.05;
    }

    .logo-sub {
      font-size: 11px;
      color: var(--brown);
      font-weight: 900;
      letter-spacing: 2px;
      text-transform: uppercase;
    }

    .nav-links {
      display: flex;
      gap: 28px;
      align-items: center;
      font-weight: 800;
      font-size: 14px;
      color: rgba(53, 35, 15, 0.74);
    }

    .nav-links a {
      position: relative;
      padding: 8px 0;
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: 2px;
      width: 0;
      height: 2px;
      background: var(--gold);
      transition: width 0.3s ease;
    }

    .nav-links a:hover::after { width: 100%; }

    .menu-btn {
      display: none;
      width: 46px;
      height: 46px;
      border-radius: 50%;
      border: 1px solid rgba(200, 150, 53, 0.24);
      background: rgba(255, 255, 255, 0.6);
      color: var(--dark);
      font-size: 24px;
      cursor: pointer;
    }

    .mobile-menu {
      position: fixed;
      inset: 0;
      z-index: 120;
      background: rgba(53, 35, 15, 0.35);
      backdrop-filter: blur(8px);
      opacity: 0;
      visibility: hidden;
      transition: 0.3s ease;
    }

    .mobile-menu.active {
      opacity: 1;
      visibility: visible;
    }

    .mobile-panel {
      margin-left: auto;
      width: min(340px, 88vw);
      height: 100%;
      background: var(--milk);
      padding: 24px;
      transform: translateX(100%);
      transition: transform 0.3s ease;
      box-shadow: var(--shadow-strong);
    }

    .mobile-menu.active .mobile-panel { transform: translateX(0); }

    .mobile-panel-top {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 28px;
    }

    .mobile-panel a {
      display: block;
      padding: 16px;
      border-radius: 18px;
      background: rgba(246, 226, 189, 0.42);
      margin-bottom: 12px;
      font-weight: 800;
      border: 1px solid rgba(200, 150, 53, 0.2);
    }

    .btn {
      position: relative;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
      padding: 14px 24px;
      border-radius: 999px;
      border: 0;
      font-weight: 900;
      cursor: pointer;
      overflow: hidden;
      transition: 0.28s ease;
      white-space: nowrap;
    }

    .btn:hover {
      transform: translateY(-3px);
      box-shadow: var(--shadow);
    }

    .btn::after {
      content: "";
      position: absolute;
      top: 0;
      left: -130%;
      width: 90%;
      height: 100%;
      background: linear-gradient(120deg, transparent, rgba(255,255,255,0.48), transparent);
      transition: 0.6s ease;
    }

    .btn:hover::after { left: 130%; }

    .btn-gold {
      background: linear-gradient(135deg, var(--gold), var(--gold-light));
      color: var(--dark);
      box-shadow: 0 18px 45px rgba(111, 70, 25, 0.22);
    }

    .btn-dark {
      background: var(--dark);
      color: white;
    }

    .btn-light {
      background: rgba(255, 255, 255, 0.58);
      border: 1px solid rgba(200,150,53,0.28);
      color: var(--dark);
      backdrop-filter: blur(14px);
    }

    .hero {
      position: relative;
      min-height: 100vh;
      padding: 140px 0 80px;
      overflow: hidden;
      background:
        radial-gradient(circle at 73% 35%, rgba(243, 217, 139, 0.58), transparent 32%),
        radial-gradient(circle at 12% 15%, rgba(255,255,255,0.78), transparent 28%),
        linear-gradient(120deg, #fffaf0, #f3dfba);
    }

    .hero::before {
      content: "";
      position: absolute;
      inset: 0;
      background: repeating-linear-gradient(90deg, rgba(111,70,25,0.035) 0 1px, transparent 1px 90px);
      pointer-events: none;
    }

    .hero-grid {
      position: relative;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      align-items: center;
    }

    .tag {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 10px 16px;
      border-radius: 999px;
      background: rgba(255,255,255,0.58);
      border: 1px solid rgba(200,150,53,0.35);
      color: var(--brown);
      font-weight: 900;
      font-size: 13px;
      letter-spacing: 1px;
      text-transform: uppercase;
      backdrop-filter: blur(12px);
    }

    h1, h2, h3 {
      font-family: Cinzel, serif;
      margin: 0;
      line-height: 1.08;
    }

    h1 {
      margin-top: 22px;
      font-size: clamp(46px, 7vw, 86px);
      max-width: 720px;
    }

    .hero p {
      margin-top: 22px;
      font-size: 19px;
      line-height: 1.8;
      color: var(--muted);
      max-width: 620px;
    }

    .hero-actions {
      margin-top: 34px;
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
    }

    .trust-row {
      margin-top: 38px;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 14px;
      max-width: 620px;
    }

    .trust-box {
      padding: 18px;
      border-radius: 22px;
      text-align: center;
      background: rgba(255,255,255,0.52);
      border: 1px solid rgba(255,255,255,0.78);
      backdrop-filter: blur(16px);
      box-shadow: 0 15px 40px rgba(111,70,25,0.08);
    }

    .trust-box strong {
      display: block;
      font-family: Cinzel, serif;
      font-size: 28px;
      color: var(--brown);
    }

    .trust-box span {
      font-size: 12px;
      font-weight: 900;
      text-transform: uppercase;
      color: rgba(53,35,15,0.58);
    }

    .image-card {
      position: relative;
      padding: 18px;
      border-radius: 36px;
      background: rgba(255,255,255,0.44);
      border: 1px solid rgba(255,255,255,0.76);
      box-shadow: var(--shadow-strong);
      backdrop-filter: blur(16px);
      transform-style: preserve-3d;
      transition: transform 0.2s ease;
    }

    .image-card::before {
      content: "";
      position: absolute;
      inset: -40px;
      background: radial-gradient(circle, rgba(232, 179, 62, 0.35), transparent 65%);
      z-index: -1;
    }

    .product-main-img {
      width: 100%;
      border-radius: 28px;
      object-fit: cover;
      box-shadow: 0 24px 70px rgba(111, 70, 25, 0.2);
      border: 1px solid rgba(255, 255, 255, 0.75);
    }

    .floating-img {
      animation: luxuryFloat 4.8s ease-in-out infinite;
    }

    @keyframes luxuryFloat {
      0%, 100% { transform: translateY(0) scale(1); }
      50% { transform: translateY(-14px) scale(1.012); }
    }

    section { padding: 96px 0; }

    .section-title {
      text-align: center;
      max-width: 800px;
      margin: 0 auto 55px;
    }

    .section-title small {
      color: var(--brown);
      font-weight: 900;
      letter-spacing: 4px;
      text-transform: uppercase;
      font-size: 13px;
    }

    .section-title h2 {
      margin-top: 13px;
      font-size: clamp(34px, 5vw, 56px);
    }

    .section-title p {
      margin-top: 16px;
      font-size: 17px;
      line-height: 1.8;
      color: var(--muted);
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1.1fr;
      gap: 42px;
      align-items: center;
    }

    .panel,
    .card,
    .gallery-card,
    .contact-box,
    .faq-item {
      border-radius: 28px;
      background: rgba(255,255,255,0.58);
      border: 1px solid rgba(255,255,255,0.78);
      box-shadow: var(--shadow);
      backdrop-filter: blur(18px);
    }

    .panel { padding: 34px; }

    .about-image {
      overflow: hidden;
      padding: 14px;
    }

    .about-image img {
      border-radius: 22px;
      max-height: 720px;
      object-fit: cover;
    }

    .about-copy h2 {
      font-size: clamp(34px, 4.4vw, 54px);
    }

    .about-copy p {
      font-size: 17px;
      line-height: 1.85;
      color: var(--muted);
    }

    .mini-features {
      margin-top: 28px;
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 14px;
    }

    .mini-feature {
      padding: 16px;
      border-radius: 18px;
      background: rgba(255,255,255,0.62);
      border: 1px solid rgba(200,150,53,0.2);
      font-weight: 900;
    }

    .benefits {
      background: linear-gradient(180deg, rgba(246, 226, 189, 0.62), var(--milk));
    }

    .card-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 24px;
    }

    .card {
      padding: 30px;
      transition: 0.35s ease;
    }

    .card:hover,
    .gallery-card:hover,
    .contact-box:hover {
      transform: translateY(-9px);
      box-shadow: 0 35px 95px rgba(111,70,25,0.22);
    }

    .icon {
      width: 58px;
      height: 58px;
      display: grid;
      place-items: center;
      border-radius: 20px;
      background: rgba(200,150,53,0.12);
      color: var(--brown);
      font-size: 28px;
      margin-bottom: 20px;
    }

    .card h3 { font-size: 23px; }

    .card p {
      color: var(--muted);
      line-height: 1.75;
    }

    .dark-section {
      background:
        radial-gradient(circle at 50% 10%, rgba(243,217,139,0.2), transparent 36%),
        var(--dark);
      color: white;
    }

    .dark-section .section-title p { color: rgba(255,255,255,0.68); }
    .dark-section .section-title small { color: var(--gold-light); }

    .product-tabs {
      display: flex;
      justify-content: center;
      gap: 12px;
      flex-wrap: wrap;
      margin-bottom: 34px;
    }

    .tab-btn {
      border: 1px solid rgba(255,255,255,0.18);
      background: rgba(255,255,255,0.08);
      color: white;
      border-radius: 999px;
      padding: 12px 18px;
      cursor: pointer;
      font-weight: 900;
      transition: 0.25s ease;
    }

    .tab-btn.active,
    .tab-btn:hover {
      background: linear-gradient(135deg, var(--gold), var(--gold-light));
      color: var(--dark);
    }

    .showcase-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 36px;
      align-items: center;
    }

    .label-image {
      padding: 18px;
      border-radius: 28px;
      background: rgba(255,255,255,0.08);
      border: 1px solid rgba(255,255,255,0.18);
      box-shadow: 0 30px 80px rgba(0,0,0,0.28);
      transition: 0.35s ease;
    }

    .label-image img { border-radius: 18px; }

    .product-info h3 { font-size: 42px; }

    .product-info p {
      line-height: 1.8;
      color: rgba(255,255,255,0.72);
      font-size: 17px;
    }

    .price {
      font-size: 25px;
      color: var(--gold-light);
      font-weight: 900;
      margin: 20px 0;
    }

    .why-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 42px;
      align-items: center;
    }

    .why-list {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 14px;
      margin-top: 34px;
    }

    .testimonials {
      background: linear-gradient(180deg, rgba(246, 226, 189, 0.62), var(--milk));
    }

    .stars {
      color: var(--gold);
      letter-spacing: 3px;
      font-size: 18px;
      margin-bottom: 18px;
    }

    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
    }

    .gallery-card {
      overflow: hidden;
      transition: 0.35s ease;
    }

    .gallery-img {
      height: 220px;
      display: grid;
      place-items: center;
      font-size: 54px;
      color: var(--brown);
      background:
        radial-gradient(circle at 52% 40%, rgba(255,255,255,0.54), transparent 26%),
        linear-gradient(135deg, #f7ead0, #d6b15d 58%, #fffaf0);
    }

    .gallery-card div:last-child { padding: 22px; }

    .faq { background: var(--milk); }

    .faq-list {
      max-width: 860px;
      margin: auto;
      display: grid;
      gap: 14px;
    }

    .faq-item { overflow: hidden; }

    .faq-question {
      width: 100%;
      padding: 22px;
      background: transparent;
      border: 0;
      color: var(--dark);
      display: flex;
      align-items: center;
      justify-content: space-between;
      cursor: pointer;
      font-weight: 900;
      text-align: left;
    }

    .faq-answer {
      max-height: 0;
      overflow: hidden;
      transition: max-height 0.3s ease;
    }

    .faq-answer p {
      margin: 0;
      padding: 0 22px 22px;
      color: var(--muted);
      line-height: 1.75;
    }

    .faq-item.active .faq-answer { max-height: 180px; }

    .contact {
      background: linear-gradient(180deg, #fff7e8, #f2ddba);
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 34px;
      align-items: start;
    }

    .contact-box {
      padding: 34px;
      transition: 0.35s ease;
    }

    input,
    textarea {
      width: 100%;
      margin-bottom: 14px;
      padding: 16px;
      border-radius: 16px;
      border: 1px solid rgba(200,150,53,0.28);
      background: rgba(255,255,255,0.78);
      outline: none;
      color: var(--dark);
    }

    input:focus,
    textarea:focus {
      border-color: var(--gold);
      box-shadow: 0 0 0 4px rgba(200,150,53,0.12);
    }

    textarea {
      min-height: 120px;
      resize: vertical;
    }

    iframe {
      width: 100%;
      height: 280px;
      border: 0;
      border-radius: 24px;
      margin-top: 20px;
      box-shadow: var(--shadow);
    }

    footer {
      background: var(--dark);
      color: white;
      padding: 55px 0 25px;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr;
      gap: 30px;
    }

    footer h2 { font-size: 34px; }

    footer p,
    footer a {
      color: rgba(255,255,255,0.68);
      line-height: 1.8;
    }

    .floating-actions {
      position: fixed;
      right: 22px;
      bottom: 22px;
      z-index: 80;
      display: grid;
      gap: 12px;
    }

    .floating-btn {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      display: grid;
      place-items: center;
      background: linear-gradient(135deg, var(--gold), var(--gold-light));
      color: var(--dark);
      font-size: 23px;
      box-shadow: 0 18px 50px rgba(111,70,25,0.35);
      transition: 0.25s ease;
    }

    .floating-btn:hover {
      transform: translateY(-4px) scale(1.04);
    }

    .reveal {
      opacity: 0;
      transform: translateY(42px);
      transition: opacity 0.85s ease, transform 0.85s ease;
    }

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }

    .hero h1,
    .hero p,
    .hero-actions,
    .trust-row {
      opacity: 0;
      animation: fadeSlideUp 1s ease forwards;
    }

    .hero p { animation-delay: 0.15s; }
    .hero-actions { animation-delay: 0.3s; }
    .trust-row { animation-delay: 0.45s; }

    @keyframes fadeSlideUp {
      from {
        opacity: 0;
        transform: translateY(34px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 960px) {
      .nav-links,
      nav > .btn {
        display: none;
      }

      .menu-btn {
        display: grid;
        place-items: center;
      }

      .hero-grid,
      .about-grid,
      .showcase-grid,
      .why-grid,
      .contact-grid,
      .footer-grid {
        grid-template-columns: 1fr;
      }

      .card-grid,
      .gallery-grid {
        grid-template-columns: 1fr 1fr;
      }

      .hero {
        padding-top: 115px;
      }
    }

    @media (max-width: 640px) {
      nav { height: 70px; }

      .logo-title { font-size: 17px; }

      .logo-mark {
        width: 42px;
        height: 42px;
      }

      section { padding: 72px 0; }

      .hero { padding-top: 105px; }

      .hero-actions,
      .product-tabs {
        flex-direction: column;
      }

      .btn,
      .tab-btn {
        width: 100%;
      }

      .trust-row,
      .mini-features,
      .card-grid,
      .gallery-grid,
      .why-list {
        grid-template-columns: 1fr;
      }

      .contact-box { padding: 24px; }

      .image-card {
        border-radius: 26px;
        padding: 12px;
      }

      .product-main-img { border-radius: 20px; }
    }
  </style>
</head>

<body>
  <div class="loader" id="loader">
    <div>
      <div class="loader-ring"></div>
      <div class="loader-title">BALIYAN GHEE</div>
    </div>
  </div>

  <header class="navbar" id="navbar">
    <div class="container">
      <nav>
        <a href="#home" class="logo">
          <span class="logo-mark">✦</span>
          <span>
            <span class="logo-title">BALIYAN GHEE</span><br>
            <span class="logo-sub">Baliyan Dairy</span>
          </span>
        </a>

        <div class="nav-links">
          <a href="#about">About</a>
          <a href="#benefits">Benefits</a>
          <a href="#products">Products</a>
          <a href="#why">Why Us</a>
          <a href="#gallery">Gallery</a>
          <a href="#contact">Contact</a>
        </div>

        <a class="btn btn-dark" href="tel:+917300640520">Call Now</a>
        <button class="menu-btn" id="menuOpen" aria-label="Open menu">☰</button>
      </nav>
    </div>
  </header>

  <div class="mobile-menu" id="mobileMenu">
    <div class="mobile-panel">
      <div class="mobile-panel-top">
        <strong>BALIYAN GHEE</strong>
        <button class="menu-btn" id="menuClose" aria-label="Close menu">×</button>
      </div>
      <a href="#about">About</a>
      <a href="#benefits">Benefits</a>
      <a href="#products">Products</a>
      <a href="#why">Why Us</a>
      <a href="#gallery">Gallery</a>
      <a href="#contact">Contact</a>
      <a href="tel:+917300640520">Call +91 7300640520</a>
    </div>
  </div>

  <main>
    <section id="home" class="hero">
      <div class="container hero-grid">
        <div>
          <span class="tag">Premium Bilona A2 Cow Ghee</span>
          <h1>Pure Bilona A2 Cow Ghee</h1>
          <p>
            Traditionally crafted with purity, nutrition, and authentic village richness.
            A luxury Indian dairy experience by Baliyan Dairy.
          </p>

          <div class="hero-actions">
            <a class="btn btn-gold" href="https://wa.me/917300640520?text=Namaste%20Baliyan%20Dairy%2C%20I%20want%20to%20order%20Baliyan%20Ghee.">Order Now</a>
            <a class="btn btn-light" href="#products">Explore Products</a>
          </div>

          <div class="trust-row">
            <div class="trust-box">
              <strong class="counter" data-target="100">0</strong>
              <span>% Pure A2</span>
            </div>
            <div class="trust-box">
              <strong class="counter" data-target="0">0</strong>
              <span>Preservatives</span>
            </div>
            <div class="trust-box">
              <strong class="counter" data-target="5000">0</strong>
              <span>Happy Homes</span>
            </div>
          </div>
        </div>

        <div class="image-card reveal tilt-card">
          <img
            class="product-main-img floating-img"
            src="file:///C:/Users/hp/Downloads/WhatsApp%20Image%202026-05-10%20at%2010.21.25%20AM.jpeg"
            alt="Baliyan Dairy A2 Desi Cow Bilona Ghee Label"
          />
        </div>
      </div>
    </section>

    <section id="about">
      <div class="container about-grid">
        <div class="panel about-image reveal">
          <img
            class="product-main-img"
            src="file:///C:/Users/hp/Downloads/WhatsApp%20Image%202026-05-10%20at%2010.21.25%20AM%20%281%29.jpeg"
            alt="Baliyan Dairy A2 Desi Cow Bilona Ghee Jar"
          />
        </div>

        <div class="about-copy reveal">
          <span class="tag">About Baliyan Dairy</span>
          <h2 style="margin-top:18px;">Village purity with luxury dairy craftsmanship</h2>
          <p>
            Baliyan Dairy brings authentic desi dairy heritage from Bhanera Jat, Shamli, Uttar Pradesh.
            Our ghee is inspired by traditional bilona preparation, premium cow milk sourcing,
            chemical-free purity, rich aroma, and granular texture.
          </p>

          <div class="mini-features">
            <div class="mini-feature">✓ Traditional Bilona Method</div>
            <div class="mini-feature">✓ A2 Desi Cow Ghee</div>
            <div class="mini-feature">✓ No Preservatives</div>
            <div class="mini-feature">✓ Premium Village Quality</div>
          </div>
        </div>
      </div>
    </section>

    <section id="benefits" class="benefits">
      <div class="container">
        <div class="section-title reveal">
          <small>Premium Benefits</small>
          <h2>Golden wellness for every home</h2>
          <p>Designed for families who value purity, authentic Indian preparation, and premium dairy quality.</p>
        </div>

        <div class="card-grid">
          <div class="card reveal"><div class="icon">✓</div><h3>100% Pure A2 Ghee</h3><p>Crafted for customers who want pure, trustworthy, premium desi ghee.</p></div>
          <div class="card reveal"><div class="icon">◷</div><h3>Traditional Bilona</h3><p>Inspired by the hand-churned bilona method for aroma and texture.</p></div>
          <div class="card reveal"><div class="icon">☘</div><h3>Farm Fresh Quality</h3><p>Rooted in village dairy values and careful milk sourcing.</p></div>
          <div class="card reveal"><div class="icon">◉</div><h3>Rich Aroma</h3><p>Golden, fragrant, and granular with a premium homemade feel.</p></div>
          <div class="card reveal"><div class="icon">✦</div><h3>No Preservatives</h3><p>No artificial color, no chemicals, and no unnecessary additives.</p></div>
          <div class="card reveal"><div class="icon">♥</div><h3>Nutritious</h3><p>A traditional Indian wellness staple for daily cooking and rituals.</p></div>
        </div>
      </div>
    </section>

    <section id="products" class="dark-section">
      <div class="container">
        <div class="section-title reveal">
          <small>Product Showcase</small>
          <h2>A2 Desi Cow Bilona Ghee</h2>
          <p>Premium quality, limited batch production, hand churned, rich aroma, granular texture, and no preservatives.</p>
        </div>

        <div class="product-tabs reveal">
          <button class="tab-btn active" data-tab="jar">Premium Label</button>
          <button class="tab-btn" data-tab="quality">Quality Promise</button>
          <button class="tab-btn" data-tab="order">Order Details</button>
        </div>

        <div class="showcase-grid">
          <div class="label-image reveal">
            <img
              class="product-main-img"
              src="file:///C:/Users/hp/Downloads/WhatsApp%20Image%202026-05-10%20at%2010.21.25%20AM.jpeg"
              alt="Baliyan Dairy Ghee Product Label"
            />
          </div>

          <div class="product-info reveal">
            <div class="tab-content active" id="tab-jar">
              <h3>A2 Desi Cow Bilona Ghee</h3>
              <p>
                A premium Indian dairy product crafted with traditional bilona inspiration, hand-churned purity,
                rich natural aroma, granular texture, and trusted quality.
              </p>
              <div class="price">Price on request</div>
            </div>

            <div class="tab-content" id="tab-quality" style="display:none;">
              <h3>Quality You Can Trust</h3>
              <p>
                No preservatives, rich aroma, granular texture, lab-tested purity approach,
                and A2 milk-focused sourcing for an authentic premium experience.
              </p>
              <div class="price">Pure. Premium. Traditional.</div>
            </div>

            <div class="tab-content" id="tab-order" style="display:none;">
              <h3>Order Directly</h3>
              <p>
                Contact Baliyan Dairy directly for fresh availability, pricing, bulk orders,
                and delivery support.
              </p>
              <div class="price">Call +91 7300640520</div>
            </div>

            <div class="hero-actions">
              <a class="btn btn-gold" href="https://wa.me/917300640520?text=I%20want%20to%20buy%20Baliyan%20Dairy%20A2%20Desi%20Cow%20Bilona%20Ghee.">Buy Now</a>
              <a class="btn btn-light" href="tel:+917300640520">Call 7300640520</a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="why">
      <div class="container why-grid">
        <div class="reveal">
          <span class="tag">Why Choose Us</span>
          <h2 style="margin-top:18px;font-size:clamp(34px,5vw,56px);">A brand built on taste, trust, and tradition.</h2>

          <div class="why-list">
            <div class="mini-feature">★ Village-made authenticity</div>
            <div class="mini-feature">★ Trusted dairy quality</div>
            <div class="mini-feature">★ Traditional preparation</div>
            <div class="mini-feature">★ Rich golden texture</div>
            <div class="mini-feature">★ Natural aroma and taste</div>
            <div class="mini-feature">★ High nutrition value</div>
          </div>
        </div>

        <div class="panel reveal">
          <h2>Luxury packaging, pure Indian soul</h2>
          <p style="line-height:1.8;color:var(--muted);">
            The Baliyan Dairy label reflects premium quality, heritage-inspired design,
            and the promise of purity from village to home.
          </p>
          <img
            class="product-main-img"
            src="file:///C:/Users/hp/Downloads/WhatsApp%20Image%202026-05-10%20at%2010.21.25%20AM.jpeg"
            alt="Baliyan Dairy Packaging"
          />
        </div>
      </div>
    </section>

    <section class="testimonials">
      <div class="container">
        <div class="section-title reveal">
          <small>Customer Love</small>
          <h2>Trusted by Indian families</h2>
        </div>

        <div class="card-grid">
          <div class="card reveal"><div class="stars">★★★★★</div><p>"The aroma feels traditional and rich. The packaging looks premium and trustworthy."</p><h3>Priya Sharma</h3><p>Delhi</p></div>
          <div class="card reveal"><div class="stars">★★★★★</div><p>"Golden texture, rich taste, and clean quality. It feels like real desi ghee."</p><h3>Amit Chaudhary</h3><p>Meerut</p></div>
          <div class="card reveal"><div class="stars">★★★★★</div><p>"Perfect for roti, dal, sweets, and daily cooking. The fragrance is beautiful."</p><h3>Neha Tyagi</h3><p>Noida</p></div>
        </div>
      </div>
    </section>

    <section id="gallery">
      <div class="container">
        <div class="section-title reveal">
          <small>Gallery</small>
          <h2>From tradition to premium jar</h2>
          <p>A visual experience inspired by bilona craft, village dairy heritage, and luxury product presentation.</p>
        </div>

        <div class="gallery-grid">
          <div class="gallery-card reveal"><div class="gallery-img">☘</div><div><h3>Dairy Heritage</h3><p>Rooted in authentic village values.</p></div></div>
          <div class="gallery-card reveal"><div class="gallery-img">◷</div><div><h3>Bilona Method</h3><p>Inspired by slow traditional preparation.</p></div></div>
          <div class="gallery-card reveal"><div class="gallery-img">☀</div><div><h3>Golden Texture</h3><p>Rich, granular, and aromatic.</p></div></div>
          <div class="gallery-card reveal"><div class="gallery-img">⌂</div><div><h3>Village Purity</h3><p>From Bhanera Jat, Shamli.</p></div></div>
          <div class="gallery-card reveal"><div class="gallery-img">◉</div><div><h3>Premium Quality</h3><p>Clean, trustworthy, and refined.</p></div></div>
          <div class="gallery-card reveal"><div class="gallery-img">✦</div><div><h3>Luxury Packaging</h3><p>Elegant label and brand identity.</p></div></div>
        </div>
      </div>
    </section>

    <section class="faq">
      <div class="container">
        <div class="section-title reveal">
          <small>Questions</small>
          <h2>Helpful information</h2>
        </div>

        <div class="faq-list">
          <div class="faq-item reveal">
            <button class="faq-question">Is Baliyan Ghee made with A2 cow milk? <span>+</span></button>
            <div class="faq-answer"><p>Yes, the brand positioning is focused on A2 Desi Cow Bilona Ghee with premium dairy quality.</p></div>
          </div>

          <div class="faq-item reveal">
            <button class="faq-question">Does it contain preservatives? <span>+</span></button>
            <div class="faq-answer"><p>No. The product highlights no preservatives, rich aroma, granular texture, and traditional purity.</p></div>
          </div>

          <div class="faq-item reveal">
            <button class="faq-question">How can I order? <span>+</span></button>
            <div class="faq-answer"><p>You can order directly through WhatsApp or call Baliyan Dairy at +91 7300640520.</p></div>
          </div>
        </div>
      </div>
    </section>

    <section id="contact" class="contact">
      <div class="container contact-grid">
        <div class="contact-box reveal">
          <span class="tag">Contact Baliyan Dairy</span>
          <h2 style="margin-top:18px;">Order pure ghee directly</h2>

          <p><strong>Phone:</strong> <a href="tel:+917300640520">+91 7300640520</a></p>
          <p><strong>Phone:</strong> <a href="tel:+916396077580">+91 6396077580</a></p>
          <p><strong>Location:</strong> Bhanera Jat, Shamli, Uttar Pradesh, India</p>
          <p><strong>Instagram:</strong> <a href="https://www.instagram.com/baliyan_dairy_01" target="_blank">@baliyan_dairy_01</a></p>

          <div class="hero-actions">
            <a class="btn btn-gold" href="https://wa.me/917300640520">WhatsApp 7300640520</a>
            <a class="btn btn-dark" href="tel:+917300640520">Call Now</a>
          </div>
        </div>

        <div class="reveal">
          <form class="contact-box" onsubmit="sendEnquiry(event)">
            <input id="name" type="text" placeholder="Your Name" required>
            <input id="phone" type="tel" placeholder="Phone Number" required>
            <input id="product" type="text" placeholder="Product Requirement" required>
            <textarea id="message" placeholder="Message"></textarea>
            <button class="btn btn-gold" type="submit">Send Enquiry on WhatsApp</button>
          </form>

          <iframe
            loading="lazy"
            src="https://www.google.com/maps?q=Bhanera%20Jat%2C%20Shamli%2C%20Uttar%20Pradesh%2C%20India&output=embed">
          </iframe>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-grid">
      <div>
        <h2>BALIYAN GHEE</h2>
        <p>Baliyan Dairy</p>
        <p><strong>Purity You Can Trust</strong></p>
      </div>

      <div>
        <h3>Quick Links</h3>
        <p><a href="#about">About</a></p>
        <p><a href="#benefits">Benefits</a></p>
        <p><a href="#products">Products</a></p>
        <p><a href="#contact">Contact</a></p>
      </div>

      <div>
        <h3>Contact</h3>
        <p><a href="tel:+917300640520">+91 7300640520</a></p>
        <p><a href="tel:+916396077580">+91 6396077580</a></p>
        <p><a href="https://www.instagram.com/baliyan_dairy_01" target="_blank">Instagram</a></p>
      </div>
    </div>

    <div class="container" style="margin-top:38px;border-top:1px solid rgba(255,255,255,0.12);padding-top:22px;color:rgba(255,255,255,0.45);font-size:14px;">
      © 2026 Baliyan Dairy. Premium Bilona A2 Cow Ghee.
    </div>
  </footer>

  <div class="floating-actions">
    <a class="floating-btn" href="https://wa.me/917300640520" aria-label="WhatsApp">☘</a>
    <a class="floating-btn" href="tel:+917300640520" aria-label="Call">☎</a>
  </div>

  <script>
    window.addEventListener("load", () => {
      document.getElementById("loader").classList.add("hide");
    });

    const navbar = document.getElementById("navbar");
    window.addEventListener("scroll", () => {
      navbar.classList.toggle("scrolled", window.scrollY > 20);
    });

    const mobileMenu = document.getElementById("mobileMenu");
    const menuOpen = document.getElementById("menuOpen");
    const menuClose = document.getElementById("menuClose");

    menuOpen.addEventListener("click", () => {
      mobileMenu.classList.add("active");
      document.body.classList.add("no-scroll");
    });

    menuClose.addEventListener("click", closeMenu);

    mobileMenu.addEventListener("click", event => {
      if (event.target === mobileMenu || event.target.tagName === "A") closeMenu();
    });

    function closeMenu() {
      mobileMenu.classList.remove("active");
      document.body.classList.remove("no-scroll");
    }

    const revealElements = document.querySelectorAll(".reveal");

    const revealObserver = new IntersectionObserver(
      entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) entry.target.classList.add("active");
        });
      },
      { threshold: 0.14 }
    );

    revealElements.forEach(element => revealObserver.observe(element));

    const counters = document.querySelectorAll(".counter");
    let countersStarted = false;

    const counterObserver = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting && !countersStarted) {
          countersStarted = true;
          counters.forEach(counter => animateCounter(counter));
        }
      });
    }, { threshold: 0.4 });

    counters.forEach(counter => counterObserver.observe(counter));

    function animateCounter(counter) {
      const target = Number(counter.dataset.target);
      const duration = 1400;
      const start = performance.now();

      function update(now) {
        const progress = Math.min((now - start) / duration, 1);
        const value = Math.floor(progress * target);

        if (target === 5000) {
          counter.textContent = value >= 5000 ? "5k+" : value;
        } else {
          counter.textContent = value;
        }

        if (progress < 1) requestAnimationFrame(update);
      }

      requestAnimationFrame(update);
    }

    const tabButtons = document.querySelectorAll(".tab-btn");
    const tabContents = document.querySelectorAll(".tab-content");

    tabButtons.forEach(button => {
      button.addEventListener("click", () => {
        tabButtons.forEach(btn => btn.classList.remove("active"));
        button.classList.add("active");

        tabContents.forEach(content => {
          content.style.display = "none";
          content.classList.remove("active");
        });

        const activeContent = document.getElementById("tab-" + button.dataset.tab);
        activeContent.style.display = "block";
        activeContent.classList.add("active");
      });
    });

    const faqItems = document.querySelectorAll(".faq-item");

    faqItems.forEach(item => {
      const question = item.querySelector(".faq-question");
      question.addEventListener("click", () => {
        faqItems.forEach(other => {
          if (other !== item) other.classList.remove("active");
        });
        item.classList.toggle("active");
      });
    });

    const tiltCards = document.querySelectorAll(".tilt-card");

    tiltCards.forEach(card => {
      card.addEventListener("mousemove", event => {
        const rect = card.getBoundingClientRect();
        const x = event.clientX - rect.left;
        const y = event.clientY - rect.top;
        const rotateY = ((x / rect.width) - 0.5) * 8;
        const rotateX = ((y / rect.height) - 0.5) * -8;
        card.style.transform = `perspective(900px) rotateX(${rotateX}deg) rotateY(${rotateY}deg)`;
      });

      card.addEventListener("mouseleave", () => {
        card.style.transform = "perspective(900px) rotateX(0deg) rotateY(0deg)";
      });
    });

    function sendEnquiry(event) {
      event.preventDefault();

      const name = document.getElementById("name").value;
      const phone = document.getElementById("phone").value;
      const product = document.getElementById("product").value;
      const message = document.getElementById("message").value;

      const text =
        `Namaste Baliyan Dairy,%0A%0AName: ${encodeURIComponent(name)}%0APhone: ${encodeURIComponent(phone)}%0ARequirement: ${encodeURIComponent(product)}%0AMessage: ${encodeURIComponent(message)}%0A%0AI want to enquire about Baliyan Ghee.`;

      window.open(`https://wa.me/917300640520?text=${text}`, "_blank");
    }
  </script>
</body>
</html>
```
