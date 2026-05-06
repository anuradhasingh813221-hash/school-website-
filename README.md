<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<!--
  ============================================================
  MOUNT LITERA ZEE SCHOOL (MLZS), BHAGALPUR &#8212; PREMIUM BLOGGER THEME
  Version: 2.2 - FIXED XML ENTITY ERROR
  Design: Mobile-First | Dark Blue + White + Yellow
  CBSE Affiliation No.: 330715
  School Est.: 2015 | Balaji Education Trust
  ============================================================
--><html b:version='2' class='v2' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data'>

<head>
  <meta charset='UTF-8'/>
  <meta content='width=device-width, initial-scale=1.0, maximum-scale=5.0' name='viewport'/>
  <meta content='IE=edge' http-equiv='X-UA-Compatible'/>

  <!-- SEO Meta Tags -->
  <b:if cond='data:blog.pageType == &quot;index&quot;'>
    <title><data:blog.title/> | CBSE School in Bhagalpur, Bihar</title>
    <meta expr:content='data:blog.metaDescription' name='description'/>
  <b:elseif cond='data:blog.pageType == &quot;item&quot;'/>
    <title><data:blog.pageName/> | <data:blog.title/></title>
    <meta content='Page | Mount Litera Zee School' name='description'/>
  <b:elseif cond='data:blog.pageType == &quot;archive&quot;'/>
    <title><data:blog.pageTitle/> | <data:blog.title/></title>
  <b:else/>
    <title><data:blog.pageName/> | <data:blog.title/></title>
  </b:if>

  <meta expr:content='data:blog.title' name='og:site_name'/>
  <meta content='website' name='og:type'/>
  <link expr:href='data:blog.url' rel='canonical'/>

  <!-- Fonts -->
  <link href='https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;800&amp;family=DM+Sans:wght@300;400;500;600;700&amp;display=swap' rel='stylesheet'/>
  <link href='https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css' rel='stylesheet'/>

  <b:skin><![CDATA[
/* ============================================================
   CSS VARIABLES & RESET
   ============================================================ */
:root {
  --navy:       #0D1B3E;
  --navy-mid:   #1a2d5a;
  --navy-light: #243b6e;
  --gold:       #F5A800;
  --gold-dark:  #d48f00;
  --gold-light: #FFD166;
  --white:      #FFFFFF;
  --off-white:  #F7F9FC;
  --gray-100:   #EEF1F7;
  --gray-200:   #D8DEEA;
  --gray-500:   #8896A5;
  --gray-700:   #4A5568;
  --gray-900:   #1A202C;
  --shadow-sm:  0 2px 8px rgba(13,27,62,0.08);
  --shadow-md:  0 6px 24px rgba(13,27,62,0.12);
  --shadow-lg:  0 16px 48px rgba(13,27,62,0.18);
  --radius-sm:  8px;
  --radius-md:  16px;
  --radius-lg:  24px;
  --radius-xl:  32px;
  --transition: 0.3s cubic-bezier(0.4,0,0.2,1);
  --font-head:  'Playfair Display', Georgia, serif;
  --font-body:  'DM Sans', -apple-system, sans-serif;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; font-size: 16px; }

body {
  font-family: var(--font-body);
  background: var(--off-white);
  color: var(--gray-900);
  line-height: 1.6;
  overflow-x: hidden;
  -webkit-font-smoothing: antialiased;
}

a { text-decoration: none; color: inherit; }
img { max-width: 100%; height: auto; display: block; }
ul { list-style: none; }
button { border: none; cursor: pointer; font-family: var(--font-body); }

/* ============================================================
   UTILITY CLASSES
   ============================================================ */
.container { max-width: 1200px; margin: 0 auto; padding: 0 16px; }
.section-tag {
  display: inline-block;
  font-size: 12px;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 10px;
}
.section-title {
  font-family: var(--font-head);
  font-size: clamp(24px, 5vw, 38px);
  font-weight: 800;
  color: var(--navy);
  line-height: 1.2;
  margin-bottom: 12px;
}
.section-subtitle {
  font-size: 15px;
  color: var(--gray-500);
  max-width: 560px;
  line-height: 1.7;
}
.btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 13px 26px;
  border-radius: 50px;
  font-size: 14px;
  font-weight: 600;
  transition: var(--transition);
  cursor: pointer;
  white-space: nowrap;
}
.btn-primary {
  background: var(--gold);
  color: var(--navy);
  box-shadow: 0 4px 16px rgba(245,168,0,0.4);
}
.btn-primary:hover {
  background: var(--gold-dark);
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(245,168,0,0.5);
}
.btn-outline {
  background: transparent;
  color: var(--white);
  border: 2px solid rgba(255,255,255,0.7);
  backdrop-filter: blur(8px);
}
.btn-outline:hover {
  background: rgba(255,255,255,0.15);
  border-color: var(--white);
  transform: translateY(-2px);
}

/* ============================================================
   HEADER / NAVBAR
   ============================================================ */
#gps-header {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 1000;
  background: var(--white);
  box-shadow: var(--shadow-sm);
  transition: var(--transition);
}
#gps-header.scrolled {
  background: rgba(255,255,255,0.97);
  backdrop-filter: blur(16px);
  box-shadow: var(--shadow-md);
}
.header-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 68px;
  padding: 0 20px;
  max-width: 1200px;
  margin: 0 auto;
}
.logo-wrap {
  display: flex;
  align-items: center;
  gap: 11px;
}
.logo-icon {
  width: 44px;
  height: 44px;
  background: var(--navy);
  border-radius: var(--radius-sm);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  overflow: hidden;
}
.logo-icon svg { width: 26px; height: 26px; }
.logo-text .school-name {
  font-family: var(--font-head);
  font-size: 16px;
  font-weight: 800;
  color: var(--navy);
  display: block;
  line-height: 1.1;
}
.logo-text .school-sub {
  font-size: 11px;
  color: var(--gray-500);
  font-weight: 500;
  letter-spacing: 0.5px;
}

/* Desktop nav */
.nav-desktop {
  display: none;
  align-items: center;
  gap: 4px;
}
@media(min-width:768px) {
  .nav-desktop { display: flex; }
}
.nav-desktop a {
  padding: 8px 14px;
  border-radius: 8px;
  font-size: 14px;
  font-weight: 500;
  color: var(--gray-700);
  transition: var(--transition);
}
.nav-desktop a:hover, .nav-desktop a.active {
  background: var(--gray-100);
  color: var(--navy);
}
.nav-desktop .nav-cta {
  background: var(--navy);
  color: var(--white);
  padding: 9px 20px;
  border-radius: 50px;
  margin-left: 8px;
}
.nav-desktop .nav-cta:hover {
  background: var(--gold);
  color: var(--navy);
}

/* ---- Dropdown Menus ---- */
.nav-desktop .has-dropdown {
  position: relative;
}
.nav-desktop .has-dropdown > a {
  display: flex;
  align-items: center;
  gap: 5px;
}
.nav-desktop .has-dropdown > a .dd-arrow {
  font-size: 10px;
  transition: transform var(--transition);
  margin-top: 1px;
}
.nav-desktop .has-dropdown:hover > a .dd-arrow {
  transform: rotate(180deg);
}
.dropdown-menu {
  position: absolute;
  top: calc(100% + 8px);
  left: 0;
  min-width: 230px;
  background: var(--white);
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-lg);
  padding: 8px 0;
  opacity: 0;
  visibility: hidden;
  transform: translateY(10px);
  transition: opacity 0.25s ease, transform 0.25s ease, visibility 0.25s;
  z-index: 2000;
  border: 1px solid var(--gray-100);
}
.has-dropdown:hover .dropdown-menu,
.has-dropdown:focus-within .dropdown-menu {
  opacity: 1;
  visibility: visible;
  transform: translateY(0);
}
.dropdown-menu a {
  display: flex !important;
  align-items: center;
  gap: 10px;
  padding: 10px 18px !important;
  border-radius: 0 !important;
  font-size: 13.5px !important;
  color: var(--gray-700) !important;
  background: transparent !important;
  border-bottom: 1px solid var(--gray-100);
  transition: var(--transition);
}
.dropdown-menu a:last-child { border-bottom: none; }
.dropdown-menu a i { color: var(--gold); width: 16px; font-size: 13px; }
.dropdown-menu a:hover {
  background: var(--off-white) !important;
  color: var(--navy) !important;
  padding-left: 24px !important;
}

/* Mobile accordion for mobile menu */
.mobile-acc-toggle {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  padding: 16px 0;
  color: rgba(255,255,255,0.8);
  font-size: 17px;
  font-weight: 500;
  border-bottom: 1px solid rgba(255,255,255,0.07);
  background: none;
  cursor: pointer;
  transition: var(--transition);
}
.mobile-acc-toggle i.icon-left { width: 20px; color: var(--gold); }
.mobile-acc-toggle .acc-arrow { font-size: 12px; color: rgba(255,255,255,0.4); transition: transform 0.3s; }
.mobile-acc-toggle.open .acc-arrow { transform: rotate(180deg); }
.mobile-acc-toggle:hover { color: var(--gold); }
.mobile-acc-body {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.35s ease;
  background: rgba(255,255,255,0.04);
  border-radius: 0 0 var(--radius-sm) var(--radius-sm);
}
.mobile-acc-body.open { max-height: 600px; }
.mobile-acc-body a {
  padding: 12px 20px 12px 44px !important;
  font-size: 14px !important;
  border-bottom: 1px solid rgba(255,255,255,0.04) !important;
  color: rgba(255,255,255,0.65) !important;
}
.mobile-acc-body a:hover { color: var(--gold) !important; padding-left: 52px !important; }

/* Hamburger */
.hamburger {
  width: 40px;
  height: 40px;
  background: var(--gray-100);
  border-radius: var(--radius-sm);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 5px;
  cursor: pointer;
  transition: var(--transition);
}
@media(min-width:768px) { .hamburger { display: none; } }
.hamburger span {
  display: block;
  width: 20px;
  height: 2px;
  background: var(--navy);
  border-radius: 2px;
  transition: var(--transition);
}
.hamburger.open span:nth-child(1) { transform: translateY(7px) rotate(45deg); }
.hamburger.open span:nth-child(2) { opacity: 0; transform: scaleX(0); }
.hamburger.open span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

/* Mobile Menu */
.mobile-menu {
  position: fixed;
  top: 68px; left: 0; right: 0; bottom: 0;
  background: var(--navy);
  z-index: 999;
  transform: translateX(100%);
  transition: transform 0.35s cubic-bezier(0.4,0,0.2,1);
  overflow-y: auto;
  padding: 24px 20px;
}
.mobile-menu.open { transform: translateX(0); }
.mobile-menu a {
  display: flex;
  align-items: center;
  gap: 14px;
  padding: 16px 0;
  color: rgba(255,255,255,0.8);
  font-size: 17px;
  font-weight: 500;
  border-bottom: 1px solid rgba(255,255,255,0.07);
  transition: var(--transition);
}
.mobile-menu a:hover { color: var(--gold); padding-left: 8px; }
.mobile-menu a i { width: 20px; color: var(--gold); }
.mobile-menu-cta {
  margin-top: 28px;
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.mobile-menu-cta .btn { justify-content: center; font-size: 15px; padding: 15px 20px; }

/* ============================================================
   HERO SECTION
   ============================================================ */
#gps-hero {
  position: relative;
  min-height: 100svh;
  display: flex;
  align-items: flex-end;
  padding-top: 68px;
  overflow: hidden;
}
.hero-bg {
  position: absolute;
  inset: 0;
  background: url('https://images.pexels.com/photos/8457822/pexels-photo-8457822.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2') center center / cover no-repeat;
}
.hero-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(
    170deg,
    rgba(13,27,62,0.55) 0%,
    rgba(13,27,62,0.82) 55%,
    rgba(13,27,62,0.97) 100%
  );
}
.hero-content {
  position: relative;
  z-index: 2;
  padding: 60px 24px 56px;
  max-width: 680px;
}
.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(245,168,0,0.2);
  border: 1px solid rgba(245,168,0,0.4);
  color: var(--gold-light);
  padding: 6px 14px;
  border-radius: 50px;
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 0.5px;
  margin-bottom: 20px;
  animation: fadeSlideUp 0.6s ease both;
}
.hero-badge i { font-size: 11px; }
.hero-title {
  font-family: var(--font-head);
  font-size: clamp(32px, 8vw, 58px);
  font-weight: 800;
  color: var(--white);
  line-height: 1.12;
  margin-bottom: 18px;
  animation: fadeSlideUp 0.6s 0.1s ease both;
}
.hero-title span { color: var(--gold-light); }
.hero-subtitle {
  font-size: clamp(14px, 3.5vw, 17px);
  color: rgba(255,255,255,0.78);
  line-height: 1.75;
  margin-bottom: 36px;
  animation: fadeSlideUp 0.6s 0.2s ease both;
  max-width: 480px;
}
.hero-btns {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  animation: fadeSlideUp 0.6s 0.3s ease both;
}
.hero-scroll {
  position: absolute;
  bottom: 28px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 6px;
  color: rgba(255,255,255,0.5);
  font-size: 11px;
  letter-spacing: 1px;
  text-transform: uppercase;
  animation: bounce 2s infinite;
}
.hero-scroll i { font-size: 14px; }

/* ============================================================
   PAGE SECTION (FOR PAGES LIKE PRIVACY POLICY)
   ============================================================ */
#gps-page-content {
  padding-top: 68px;
  min-height: 100vh;
  background: var(--white);
}
.page-wrapper {
  max-width: 900px;
  margin: 0 auto;
  padding: 60px 24px;
}
.page-header {
  margin-bottom: 40px;
  border-bottom: 2px solid var(--gray-100);
  padding-bottom: 24px;
}
.page-title {
  font-family: var(--font-head);
  font-size: clamp(28px, 6vw, 48px);
  font-weight: 800;
  color: var(--navy);
  margin-bottom: 12px;
}
.page-meta {
  font-size: 13px;
  color: var(--gray-500);
  display: flex;
  align-items: center;
  gap: 16px;
}

/* Page content styling */
.post-body, .page-body {
  font-size: 15px;
  line-height: 1.8;
  color: var(--gray-900);
}
.post-body p, .page-body p {
  margin-bottom: 18px;
}
.post-body h2, .page-body h2,
.post-body h3, .page-body h3 {
  font-family: var(--font-head);
  color: var(--navy);
  margin: 28px 0 16px 0;
  font-weight: 700;
}
.post-body h2, .page-body h2 {
  font-size: 28px;
  border-bottom: 2px solid var(--gold);
  padding-bottom: 10px;
}
.post-body h3, .page-body h3 {
  font-size: 22px;
}
.post-body ul, .page-body ul,
.post-body ol, .page-body ol {
  margin-left: 20px;
  margin-bottom: 18px;
}
.post-body li, .page-body li {
  margin-bottom: 10px;
}
.post-body blockquote, .page-body blockquote {
  border-left: 4px solid var(--gold);
  padding-left: 20px;
  margin: 20px 0;
  color: var(--gray-700);
  font-style: italic;
}

/* Stats Section - kept same as homepage */
#gps-stats {
  background: var(--white);
  padding: 0 16px;
  margin-top: -1px;
}
.stats-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 12px;
  padding: 28px 0;
  max-width: 700px;
  margin: 0 auto;
}
@media(min-width:600px) { .stats-grid { grid-template-columns: repeat(4, 1fr); } }
.stat-card {
  background: var(--off-white);
  border-radius: var(--radius-md);
  padding: 22px 16px;
  text-align: center;
  border: 1px solid var(--gray-100);
  transition: var(--transition);
  position: relative;
  overflow: hidden;
}
.stat-card::before {
  content: '';
  position: absolute;
  bottom: 0; left: 0; right: 0;
  height: 3px;
  background: var(--gold);
  transform: scaleX(0);
  transition: var(--transition);
}
.stat-card:hover { transform: translateY(-4px); box-shadow: var(--shadow-md); }
.stat-card:hover::before { transform: scaleX(1); }
.stat-icon {
  width: 48px;
  height: 48px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 12px;
  font-size: 22px;
}
.stat-icon.yellow { background: rgba(245,168,0,0.12); color: var(--gold); }
.stat-icon.blue   { background: rgba(36,59,110,0.1);  color: var(--navy-light); }
.stat-icon.green  { background: rgba(39,174,96,0.1);  color: #27ae60; }
.stat-icon.purple { background: rgba(142,68,173,0.1); color: #8e44ad; }
.stat-number {
  font-family: var(--font-head);
  font-size: 28px;
  font-weight: 800;
  color: var(--navy);
  line-height: 1;
  display: block;
}
.stat-label {
  font-size: 12px;
  color: var(--gray-500);
  font-weight: 500;
  margin-top: 4px;
  display: block;
}

/* ============================================================
   FOOTER
   ============================================================ */
#gps-footer {
  background: var(--navy);
  color: rgba(255,255,255,0.8);
  padding: 60px 24px 0;
}
.footer-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 40px;
  max-width: 1200px;
  margin: 0 auto;
  padding-bottom: 48px;
}
@media(min-width:768px) { .footer-grid { grid-template-columns: repeat(3, 1fr); } }
.footer-col h4 {
  font-family: var(--font-head);
  font-size: 16px;
  font-weight: 700;
  color: var(--white);
  margin-bottom: 16px;
}
.footer-col ul { display: flex; flex-direction: column; gap: 10px; }
.footer-col a {
  font-size: 14px;
  color: rgba(255,255,255,0.7);
  transition: var(--transition);
}
.footer-col a:hover { color: var(--gold); }
.footer-divider {
  height: 1px;
  background: rgba(255,255,255,0.1);
  margin: 32px 0;
}
.footer-bottom {
  display: flex;
  flex-direction: column;
  gap: 12px;
  align-items: center;
  text-align: center;
  padding: 24px 0;
  border-top: 1px solid rgba(255,255,255,0.1);
}
.footer-bottom p {
  font-size: 13px;
  color: rgba(255,255,255,0.6);
}

/* Animations */
@keyframes fadeSlideUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-8px); }
}
  ]]></b:skin>
</head>

<body>
  <!-- ============================================================
       HEADER / NAVBAR - FIXED ON ALL PAGES
       ============================================================ -->
  <header id='gps-header'>
    <div class='header-inner'>
      <div class='logo-wrap'>
        <a href='/' style='display: flex; align-items: center; gap: 11px;'>
          <div class='logo-icon'>
            <i class='fas fa-graduation-cap' style='color: var(--gold);'></i>
          </div>
          <div class='logo-text'>
            <span class='school-name'>MLZS</span>
            <span class='school-sub'>School</span>
          </div>
        </a>
      </div>

      <!-- Desktop Navigation -->
      <nav class='nav-desktop'>
        <a href='/' style='display: flex; align-items: center;'>
          <i class='fas fa-home' style='margin-right: 5px; font-size: 14px;'></i> Home
        </a>
        <div class='has-dropdown'>
          <a href='#' style='display: flex; align-items: center;'>
            <i class='fas fa-graduation-cap' style='margin-right: 5px; font-size: 14px;'></i> Academics
            <i class='fas fa-chevron-down dd-arrow'></i>
          </a>
          <div class='dropdown-menu'>
            <a href='/#gps-why'><i class='fas fa-star'></i> Why Choose Us</a>
            <a href='/#gps-gallery'><i class='fas fa-images'></i> Gallery</a>
            <a href='/#gps-updates'><i class='fas fa-bell'></i> Updates</a>
          </div>
        </div>
        <a href='#gps-testimonials' style='display: flex; align-items: center;'>
          <i class='fas fa-comment' style='margin-right: 5px; font-size: 14px;'></i> Testimonials
        </a>
        <a href='https://demowebschool.blogspot.com/p/privacy-policy.html' style='display: flex; align-items: center;'>
          <i class='fas fa-lock' style='margin-right: 5px; font-size: 14px;'></i> Privacy
        </a>
        <a href='#gps-cta' class='nav-cta' style='display: flex; align-items: center;'>
          <i class='fas fa-paper-plane' style='font-size: 13px;'></i> Contact
        </a>
      </nav>

      <!-- Hamburger Menu -->
      <div class='hamburger' onclick='toggleMobileMenu()'>
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div class='mobile-menu' id='mobileMenu'>
      <a href='/' style='display: flex; align-items: center;'><i class='fas fa-home'></i> Home</a>
      
      <button class='mobile-acc-toggle' onclick='toggleAccordion(this)'>
        <span style='display: flex; align-items: center;'><i class='fas fa-graduation-cap icon-left'></i> Academics</span>
        <i class='fas fa-chevron-down acc-arrow'></i>
      </button>
      <div class='mobile-acc-body'>
        <a href='/#gps-why'><i class='fas fa-star'></i> Why Choose Us</a>
        <a href='/#gps-gallery'><i class='fas fa-images'></i> Gallery</a>
        <a href='/#gps-updates'><i class='fas fa-bell'></i> Updates</a>
      </div>

      <a href='#gps-testimonials'><i class='fas fa-comment'></i> Testimonials</a>
      <a href='https://demowebschool.blogspot.com/p/privacy-policy.html'><i class='fas fa-lock'></i> Privacy Policy</a>
      <a href='#gps-cta'><i class='fas fa-paper-plane'></i> Contact</a>

      <div class='mobile-menu-cta'>
        <a href='https://demowebschool.blogspot.com/p/privacy-policy.html' class='btn btn-primary'>Open Privacy Policy</a>
      </div>
    </div>
  </header>

  <!-- ============================================================
       MAIN CONTENT - CONDITIONAL FOR HOMEPAGE VS PAGES
       ============================================================ -->
  <main>
    <b:if cond='data:blog.pageType == &quot;index&quot;'>
      <!-- HOMEPAGE - Keep all original sections -->
      <section id='gps-hero'>
        <div class='hero-bg'></div>
        <div class='hero-overlay'></div>
        <div class='hero-content'>
          <div class='hero-badge'>
            <i class='fas fa-star'></i> Welcome to Excellence
          </div>
          <h1 class='hero-title'>Mount Litera Zee <span>School</span></h1>
          <p class='hero-subtitle'>Nurturing young minds through quality education, holistic development, and world-class facilities since 2015.</p>
          <div class='hero-btns'>
            <a href='#gps-why' class='btn btn-primary'>
              <i class='fas fa-arrow-right'></i> Learn More
            </a>
            <a href='#gps-cta' class='btn btn-outline'>
              <i class='fas fa-phone'></i> Contact Us
            </a>
          </div>
        </div>
        <div class='hero-scroll'>
          <span>Scroll Down</span>
          <i class='fas fa-chevron-down'></i>
        </div>
      </section>

      <section id='gps-stats'>
        <div class='container'>
          <div class='stats-grid'>
            <div class='stat-card'>
              <div class='stat-icon yellow'><i class='fas fa-users'></i></div>
              <span class='stat-number'>5000+</span>
              <span class='stat-label'>Students</span>
            </div>
            <div class='stat-card'>
              <div class='stat-icon blue'><i class='fas fa-chalkboard-user'></i></div>
              <span class='stat-number'>200+</span>
              <span class='stat-label'>Faculty</span>
            </div>
            <div class='stat-card'>
              <div class='stat-icon green'><i class='fas fa-medal'></i></div>
              <span class='stat-number'>95%</span>
              <span class='stat-label'>Pass Rate</span>
            </div>
            <div class='stat-card'>
              <div class='stat-icon purple'><i class='fas fa-trophy'></i></div>
              <span class='stat-number'>150+</span>
              <span class='stat-label'>Awards</span>
            </div>
          </div>
        </div>
      </section>

      <section id='gps-cta'>
        <div class='container' style='text-align: center;'>
          <span class='section-tag'>Get In Touch</span>
          <h2 class='section-title'>Ready to Join Us?</h2>
          <p>Admission open for new session. Contact us for more information.</p>
          <a href='mailto:info@mlzschool.com' class='btn btn-navy'>
            <i class='fas fa-envelope'></i> Send Email
          </a>
        </div>
      </section>
    <b:else/>
      <!-- PAGE CONTENT (PRIVACY POLICY, ABOUT, ETC) -->
      <section id='gps-page-content'>
        <div class='page-wrapper'>
          <div class='page-header'>
            <h1 class='page-title'><data:blog.pageName/></h1>
            <div class='page-meta'>
              <span><i class='fas fa-calendar' style='color: var(--gold); margin-right: 6px;'></i> Last Updated: <data:post.timestamp expr:format='MMM dd, yyyy'/></span>
            </div>
          </div>
          
          <div class='post-body'>
            <data:post.body/>
          </div>
        </div>
      </section>
    </b:if>
  </main>

  <!-- ============================================================
       FOOTER - ON ALL PAGES
       ============================================================ -->
  <footer id='gps-footer'>
    <div class='container'>
      <div class='footer-grid'>
        <div class='footer-col'>
          <h4>About School</h4>
          <p style='font-size: 14px; line-height: 1.6;'>Mount Litera Zee School provides quality education with modern infrastructure and experienced faculty since 2015.</p>
        </div>
        <div class='footer-col'>
          <h4>Quick Links</h4>
          <ul>
            <li><a href='/'>Home</a></li>
            <li><a href='/#gps-gallery'>Gallery</a></li>
            <li><a href='#'>About Us</a></li>
            <li><a href='https://demowebschool.blogspot.com/p/privacy-policy.html'>Privacy Policy</a></li>
            <li><a href='#'>Contact</a></li>
          </ul>
        </div>
        <div class='footer-col'>
          <h4>Contact Info</h4>
          <p style='font-size: 14px;'><i class='fas fa-map-marker-alt' style='color: var(--gold); margin-right: 8px;'></i> Bhagalpur, Bihar</p>
          <p style='font-size: 14px; margin-top: 10px;'><i class='fas fa-phone' style='color: var(--gold); margin-right: 8px;'></i> +91 1234567890</p>
          <p style='font-size: 14px; margin-top: 10px;'><i class='fas fa-envelope' style='color: var(--gold); margin-right: 8px;'></i> info@mlzschool.com</p>
        </div>
      </div>

      <div class='footer-divider'></div>

      <div class='footer-bottom'>
        <p>&#169; 2024 Mount Litera Zee School. All Rights Reserved.</p>
        <p>Designed with <i class='fas fa-heart' style='color: var(--gold);'></i> for Educational Excellence</p>
      </div>
    </div>
  </footer>

  <!-- ============================================================
       JAVASCRIPT - MOBILE MENU & HEADER SCROLL
       ============================================================ -->
  <script>
    // Mobile Menu Toggle
    function toggleMobileMenu() {
      const hamburger = document.querySelector('.hamburger');
      const mobileMenu = document.getElementById('mobileMenu');
      hamburger.classList.toggle('open');
      mobileMenu.classList.toggle('open');
    }

    // Mobile Accordion Toggle
    function toggleAccordion(btn) {
      const body = btn.nextElementSibling;
      btn.classList.toggle('open');
      body.classList.toggle('open');
    }

    // Header Scroll Effect
    window.addEventListener('scroll', () => {
      const header = document.getElementById('gps-header');
      if (window.scrollY > 10) {
        header.classList.add('scrolled');
      } else {
        header.classList.remove('scrolled');
      }
    });

    // Close mobile menu on link click
    document.querySelectorAll('.mobile-menu a').forEach(link => {
      link.addEventListener('click', () => {
        document.querySelector('.hamburger').classList.remove('open');
        document.getElementById('mobileMenu').classList.remove('open');
      });
    });
  </script>
</body>
</html>