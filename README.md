<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<!--
  ============================================================
  MOUNT LITERA ZEE SCHOOL (MLZS), BHAGALPUR &#8212; PREMIUM BLOGGER THEME
  Version: 2.0
  Design: Mobile-First | Dark Blue + White + Yellow
  CBSE Affiliation No.: 330715
  School Est.: 2015 | Balaji Education Trust
  ============================================================
--><html b:version='2' class='v2' expr:dir='data:blog.languageDirection' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>

<head>
  <meta charset='UTF-8'/>
  <meta content='width=device-width, initial-scale=1.0, maximum-scale=5.0' name='viewport'/>
  <meta content='IE=edge' http-equiv='X-UA-Compatible'/>

  <!-- SEO Meta Tags -->
  <b:if cond='data:blog.pageType == &quot;index&quot;'>
    <title><data:blog.title/> | CBSE School in Bhagalpur, Bihar</title>
    <meta expr:content='data:blog.metaDescription' name='description'/>
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

/* ---- One-Time Popup ---- */
#mlzs-popup-overlay {
  position: fixed;
  inset: 0;
  background: rgba(13,27,62,0.75);
  z-index: 9998;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  backdrop-filter: blur(6px);
  animation: popupFadeIn 0.4s ease both;
}
@keyframes popupFadeIn {
  from { opacity: 0; }
  to   { opacity: 1; }
}
#mlzs-popup {
  position: relative;
  background: var(--white);
  border-radius: var(--radius-xl);
  overflow: hidden;
  max-width: 480px;
  width: 100%;
  box-shadow: 0 24px 80px rgba(13,27,62,0.4);
  animation: popupSlideUp 0.45s 0.1s cubic-bezier(0.34,1.56,0.64,1) both;
}
@keyframes popupSlideUp {
  from { opacity: 0; transform: scale(0.88) translateY(30px); }
  to   { opacity: 1; transform: scale(1) translateY(0); }
}
.popup-img-wrap {
  position: relative;
  height: 240px;
  overflow: hidden;
}
.popup-img-wrap img {
  width: 100%; height: 100%;
  object-fit: cover;
  object-position: top center;
}
.popup-img-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(to bottom, transparent 40%, rgba(13,27,62,0.85) 100%);
}
.popup-img-text {
  position: absolute;
  bottom: 16px; left: 20px; right: 50px;
  color: var(--white);
}
.popup-img-text h3 {
  font-family: var(--font-head);
  font-size: 20px;
  font-weight: 800;
  line-height: 1.2;
}
.popup-img-text p { font-size: 12px; color: rgba(255,255,255,0.75); margin-top: 4px; }
.popup-body {
  padding: 22px 24px 26px;
  text-align: center;
}
.popup-school-badge {
  display: inline-flex;
  align-items: center;
  gap: 7px;
  background: rgba(245,168,0,0.12);
  border: 1px solid rgba(245,168,0,0.35);
  color: var(--navy);
  padding: 5px 14px;
  border-radius: 50px;
  font-size: 11.5px;
  font-weight: 700;
  letter-spacing: 0.3px;
  margin-bottom: 12px;
}
.popup-school-badge i { color: var(--gold); }
.popup-body h2 {
  font-family: var(--font-head);
  font-size: 22px;
  font-weight: 800;
  color: var(--navy);
  margin-bottom: 8px;
  line-height: 1.2;
}
.popup-body p {
  font-size: 13.5px;
  color: var(--gray-500);
  line-height: 1.65;
  margin-bottom: 20px;
}
.popup-btns {
  display: flex;
  gap: 10px;
  justify-content: center;
  flex-wrap: wrap;
}
.popup-btns .btn { font-size: 13px; padding: 11px 22px; }
.popup-close {
  position: absolute;
  top: 12px; right: 12px;
  width: 34px; height: 34px;
  background: rgba(255,255,255,0.92);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  font-size: 15px;
  color: var(--navy);
  box-shadow: 0 2px 10px rgba(0,0,0,0.15);
  transition: var(--transition);
  z-index: 10;
  border: none;
}
.popup-close:hover { background: var(--gold); color: var(--navy); transform: rotate(90deg); }

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
   STATS SECTION
   ============================================================ */
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
   WHY CHOOSE US
   ============================================================ */
#gps-why {
  padding: 64px 20px;
  background: var(--white);
}
.why-header { margin-bottom: 36px; }
.features-scroll {
  display: flex;
  gap: 14px;
  overflow-x: auto;
  padding-bottom: 12px;
  scrollbar-width: none;
  -ms-overflow-style: none;
}
.features-scroll::-webkit-scrollbar { display: none; }
@media(min-width:768px) {
  .features-scroll {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    overflow: visible;
  }
}
.feature-card {
  flex-shrink: 0;
  width: 130px;
  background: var(--off-white);
  border-radius: var(--radius-md);
  padding: 24px 16px;
  text-align: center;
  border: 1.5px solid var(--gray-100);
  transition: var(--transition);
  cursor: pointer;
}
@media(min-width:768px) { .feature-card { width: auto; } }
.feature-card:hover {
  background: var(--navy);
  border-color: var(--navy);
  transform: translateY(-6px);
  box-shadow: var(--shadow-lg);
}
.feature-card:hover .feature-icon { background: rgba(245,168,0,0.2); color: var(--gold); }
.feature-card:hover .feature-name { color: var(--white); }
.feature-icon {
  width: 54px;
  height: 54px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 14px;
  font-size: 22px;
  transition: var(--transition);
}
.fi-1 { background: rgba(36,59,110,0.1);  color: var(--navy-light); }
.fi-2 { background: rgba(142,68,173,0.1); color: #8e44ad; }
.fi-3 { background: rgba(39,174,96,0.1);  color: #27ae60; }
.fi-4 { background: rgba(230,126,34,0.1); color: #e67e22; }
.fi-5 { background: rgba(231,76,60,0.1);  color: #e74c3c; }
.feature-name {
  font-size: 13px;
  font-weight: 600;
  color: var(--navy);
  transition: var(--transition);
  line-height: 1.3;
}

/* ============================================================
   LATEST UPDATES
   ============================================================ */
#gps-updates {
  padding: 64px 20px;
  background: var(--gray-100);
}
.section-header {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  margin-bottom: 28px;
  gap: 12px;
}
.view-all {
  font-size: 13px;
  font-weight: 600;
  color: var(--navy);
  display: flex;
  align-items: center;
  gap: 5px;
  white-space: nowrap;
  transition: var(--transition);
}
.view-all:hover { color: var(--gold); }
.updates-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 14px;
}
@media(min-width:600px) { .updates-grid { grid-template-columns: repeat(2, 1fr); } }
@media(min-width:900px) { .updates-grid { grid-template-columns: repeat(3, 1fr); } }
.update-card {
  background: var(--white);
  border-radius: var(--radius-md);
  padding: 22px;
  border: 1px solid var(--gray-200);
  transition: var(--transition);
  display: flex;
  gap: 16px;
  align-items: flex-start;
}
.update-card:hover { transform: translateY(-3px); box-shadow: var(--shadow-md); border-color: var(--gold); }
.update-icon-wrap {
  width: 48px;
  height: 48px;
  border-radius: var(--radius-sm);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  flex-shrink: 0;
}
.ui-blue   { background: rgba(36,59,110,0.1);  color: var(--navy); }
.ui-green  { background: rgba(39,174,96,0.12); color: #27ae60; }
.ui-purple { background: rgba(142,68,173,0.1); color: #8e44ad; }
.update-meta { flex: 1; min-width: 0; }
.update-label {
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: var(--gold);
  margin-bottom: 4px;
}
.update-title {
  font-size: 14px;
  font-weight: 700;
  color: var(--navy);
  line-height: 1.4;
  margin-bottom: 6px;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
.update-date {
  font-size: 12px;
  color: var(--gray-500);
  display: flex;
  align-items: center;
  gap: 5px;
}

/* ============================================================
   GALLERY SECTION
   ============================================================ */
#gps-gallery {
  padding: 64px 20px;
  background: var(--white);
}
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
  margin-top: 28px;
}
@media(min-width:600px) { .gallery-grid { grid-template-columns: repeat(3, 1fr); } }
@media(min-width:900px) { .gallery-grid { grid-template-columns: repeat(4, 1fr); } }
.gallery-item {
  border-radius: var(--radius-md);
  overflow: hidden;
  aspect-ratio: 1;
  position: relative;
  cursor: pointer;
  background: var(--gray-100);
}
.gallery-item:nth-child(1) { grid-column: span 2; grid-row: span 2; }
@media(max-width:599px) { .gallery-item:nth-child(1) { grid-column: span 2; } }
.gallery-item img {
  width: 100%; height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}
.gallery-item:hover img { transform: scale(1.08); }
.gallery-overlay {
  position: absolute;
  inset: 0;
  background: rgba(13,27,62,0.6);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: var(--transition);
  color: white;
  font-size: 26px;
}
.gallery-item:hover .gallery-overlay { opacity: 1; }

/* ============================================================
   TESTIMONIALS
   ============================================================ */
#gps-testimonials {
  padding: 64px 20px;
  background: var(--navy);
  overflow: hidden;
}
#gps-testimonials .section-tag { color: var(--gold-light); }
#gps-testimonials .section-title { color: var(--white); }
.testi-slider {
  position: relative;
  margin-top: 32px;
}
.testi-track {
  display: flex;
  gap: 20px;
  transition: transform 0.5s cubic-bezier(0.4,0,0.2,1);
}
.testi-card {
  flex: 0 0 calc(100% - 0px);
  background: rgba(255,255,255,0.06);
  border: 1px solid rgba(255,255,255,0.1);
  border-radius: var(--radius-lg);
  padding: 32px 28px;
  backdrop-filter: blur(10px);
}
@media(min-width:700px) {
  .testi-card { flex: 0 0 calc(50% - 10px); }
}
@media(min-width:1000px) {
  .testi-card { flex: 0 0 calc(33.333% - 14px); }
}
.testi-stars { color: var(--gold); font-size: 14px; margin-bottom: 16px; display: flex; gap: 3px; }
.testi-text {
  font-size: 15px;
  color: rgba(255,255,255,0.8);
  line-height: 1.75;
  margin-bottom: 24px;
  font-style: italic;
}
.testi-author { display: flex; align-items: center; gap: 13px; }
.testi-avatar {
  width: 46px;
  height: 46px;
  border-radius: 50%;
  background: var(--navy-light);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--gold);
  font-size: 18px;
  font-weight: 700;
  font-family: var(--font-head);
  flex-shrink: 0;
  border: 2px solid rgba(245,168,0,0.3);
}
.testi-name { font-size: 14px; font-weight: 700; color: var(--white); }
.testi-role { font-size: 12px; color: rgba(255,255,255,0.5); }
.testi-controls {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 12px;
  margin-top: 28px;
}
.testi-btn {
  width: 40px; height: 40px;
  border-radius: 50%;
  background: rgba(255,255,255,0.1);
  color: var(--white);
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: var(--transition);
  font-size: 15px;
  border: 1px solid rgba(255,255,255,0.15);
}
.testi-btn:hover { background: var(--gold); color: var(--navy); border-color: var(--gold); }
.testi-dots { display: flex; gap: 6px; }
.testi-dot {
  width: 7px; height: 7px;
  border-radius: 50%;
  background: rgba(255,255,255,0.25);
  cursor: pointer;
  transition: var(--transition);
}
.testi-dot.active { background: var(--gold); width: 22px; border-radius: 4px; }

/* ============================================================
   ADMISSIONS CTA BANNER
   ============================================================ */
#gps-cta {
  padding: 56px 24px;
  background: linear-gradient(135deg, var(--gold) 0%, #ffbe2e 100%);
  text-align: center;
  position: relative;
  overflow: hidden;
}
#gps-cta::before {
  content: '';
  position: absolute;
  top: -50%; right: -20%;
  width: 400px; height: 400px;
  border-radius: 50%;
  background: rgba(255,255,255,0.12);
  pointer-events: none;
}
#gps-cta .section-tag { color: var(--navy); opacity: 0.7; }
#gps-cta .section-title { color: var(--navy); margin-bottom: 8px; }
#gps-cta p { color: rgba(13,27,62,0.7); margin-bottom: 28px; font-size: 15px; }
#gps-cta .btn-navy {
  background: var(--navy);
  color: var(--white);
  padding: 15px 32px;
  border-radius: 50px;
  font-size: 15px;
  font-weight: 700;
  box-shadow: 0 6px 20px rgba(13,27,62,0.3);
  transition: var(--transition);
  display: inline-flex;
  align-items: center;
  gap: 9px;
}
#gps-cta .btn-navy:hover { transform: translateY(-3px); box-shadow: 0 12px 32px rgba(13,27,62,0.4); }

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
@media(min-width:600px) { .footer-grid { grid-template-columns: repeat(2, 1fr); } }
@media(min-width:900px) { .footer-grid { grid-template-columns: 1.5fr 1fr 1fr 1.3fr; gap: 32px; } }

.footer-brand .logo-wrap { margin-bottom: 18px; }
.footer-brand .logo-text .school-name { color: var(--white); }
.footer-brand .logo-text .school-sub { color: rgba(255,255,255,0.5); }
.footer-brand p {
  font-size: 14px;
  line-height: 1.8;
  color: rgba(255,255,255,0.6);
  margin-bottom: 22px;
}
.social-links { display: flex; gap: 10px; }
.social-link {
  width: 38px; height: 38px;
  border-radius: var(--radius-sm);
  background: rgba(255,255,255,0.07);
  display: flex;
  align-items: center;
  justify-content: center;
  color: rgba(255,255,255,0.7);
  font-size: 15px;
  transition: var(--transition);
  border: 1px solid rgba(255,255,255,0.1);
}
.social-link:hover { background: var(--gold); color: var(--navy); border-color: var(--gold); transform: translateY(-2px); }

.footer-col h4 {
  font-size: 14px;
  font-weight: 700;
  color: var(--white);
  margin-bottom: 18px;
  letter-spacing: 0.3px;
  position: relative;
  padding-bottom: 12px;
}
.footer-col h4::after {
  content: '';
  position: absolute;
  bottom: 0; left: 0;
  width: 30px; height: 2px;
  background: var(--gold);
  border-radius: 2px;
}
.footer-links li { margin-bottom: 10px; }
.footer-links a {
  font-size: 14px;
  color: rgba(255,255,255,0.6);
  transition: var(--transition);
  display: flex;
  align-items: center;
  gap: 8px;
}
.footer-links a:hover { color: var(--gold); padding-left: 4px; }
.footer-links a i { font-size: 11px; color: var(--gold); }

.contact-item {
  display: flex;
  gap: 13px;
  margin-bottom: 16px;
  align-items: flex-start;
}
.contact-item i {
  color: var(--gold);
  font-size: 15px;
  margin-top: 2px;
  flex-shrink: 0;
  width: 16px;
}
.contact-item p { font-size: 14px; color: rgba(255,255,255,0.6); line-height: 1.6; }
.contact-item a { color: rgba(255,255,255,0.6); transition: var(--transition); }
.contact-item a:hover { color: var(--gold); }

.map-embed {
  margin-top: 14px;
  border-radius: var(--radius-md);
  overflow: hidden;
  height: 140px;
}
.map-embed iframe { width: 100%; height: 100%; border: none; }

.footer-bottom {
  border-top: 1px solid rgba(255,255,255,0.07);
  padding: 20px 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 10px;
  max-width: 1200px;
  margin: 0 auto;
}
.footer-bottom p { font-size: 13px; color: rgba(255,255,255,0.4); }
.footer-bottom a { color: var(--gold); transition: var(--transition); }
.footer-bottom a:hover { color: var(--gold-light); }

/* ============================================================
   BOTTOM NAV (Mobile)
   ============================================================ */
.bottom-nav {
  position: fixed;
  bottom: 0; left: 0; right: 0;
  background: var(--white);
  border-top: 1px solid var(--gray-200);
  display: flex;
  z-index: 998;
  box-shadow: 0 -4px 20px rgba(13,27,62,0.1);
  padding-bottom: env(safe-area-inset-bottom);
}
@media(min-width:768px) { .bottom-nav { display: none; } }
.bottom-nav-item {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4px;
  padding: 10px 0;
  cursor: pointer;
  color: var(--gray-500);
  font-size: 10px;
  font-weight: 600;
  transition: var(--transition);
  text-decoration: none;
}
.bottom-nav-item i { font-size: 20px; }
.bottom-nav-item.active { color: var(--gold); }
.bottom-nav-item:hover { color: var(--navy); }
body { padding-bottom: 68px; }
@media(min-width:768px) { body { padding-bottom: 0; } }

/* ============================================================
   BLOGGER WIDGET OVERRIDES
   ============================================================ */
.widget { margin: 0 !important; padding: 0 !important; }
.blog-posts-widget-list { padding: 0 !important; }

/* ============================================================
   ANIMATIONS
   ============================================================ */
@keyframes fadeSlideUp {
  from { opacity: 0; transform: translateY(30px); }
  to   { opacity: 1; transform: translateY(0); }
}
@keyframes bounce {
  0%, 100% { transform: translateX(-50%) translateY(0); }
  50%       { transform: translateX(-50%) translateY(8px); }
}
@keyframes countUp {
  from { opacity: 0; transform: scale(0.8); }
  to   { opacity: 1; transform: scale(1); }
}
.animate-in {
  opacity: 0;
  transform: translateY(28px);
  transition: opacity 0.55s ease, transform 0.55s ease;
}
.animate-in.visible {
  opacity: 1;
  transform: translateY(0);
}

/* ============================================================
   SCROLL TO TOP
   ============================================================ */
#scrollTop {
  position: fixed;
  bottom: 90px;
  right: 20px;
  width: 44px;
  height: 44px;
  background: var(--navy);
  color: var(--white);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 16px;
  cursor: pointer;
  z-index: 990;
  box-shadow: var(--shadow-md);
  transition: var(--transition);
  opacity: 0;
  transform: translateY(20px);
  pointer-events: none;
}
#scrollTop.show { opacity: 1; transform: translateY(0); pointer-events: all; }
#scrollTop:hover { background: var(--gold); color: var(--navy); }
@media(min-width:768px) { #scrollTop { bottom: 30px; } }

/* ============================================================
   LOADING BAR
   ============================================================ */
#page-loader {
  position: fixed;
  top: 0; left: 0; right: 0;
  height: 3px;
  background: linear-gradient(90deg, var(--gold), var(--navy));
  z-index: 9999;
  animation: loadingBar 1.2s ease forwards;
}
@keyframes loadingBar {
  from { width: 0; opacity: 1; }
  to   { width: 100%; opacity: 0; }
}

/* ============================================================
   NOTICE BAR
   ============================================================ */
.notice-bar {
  background: var(--navy);
  color: var(--white);
  font-size: 12.5px;
  padding: 8px 16px;
  display: flex;
  align-items: center;
  gap: 10px;
  overflow: hidden;
  position: relative;
}
.notice-bar i { color: var(--gold); flex-shrink: 0; }
.notice-ticker {
  overflow: hidden;
  flex: 1;
}
.notice-ticker-inner {
  display: flex;
  gap: 60px;
  animation: ticker 22s linear infinite;
  white-space: nowrap;
}
@keyframes ticker {
  0%   { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}
.notice-bar .close-notice {
  color: rgba(255,255,255,0.5);
  cursor: pointer;
  padding: 2px 6px;
  flex-shrink: 0;
  font-size: 16px;
  line-height: 1;
}
.notice-bar .close-notice:hover { color: var(--white); }

/* ============================================================
   PAGE CONTENT AREA — Universal Blogger Widget Styles
   ============================================================ */
.page-content-area {
  min-height: 70vh;
  background: var(--off-white);
  padding: 100px 0 60px;
}
body.is-homepage .page-content-area { display: none !important; }
.page-inner { max-width: 900px; margin: 0 auto; padding: 0 20px; }

/* Breadcrumb */
.page-breadcrumb {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 13px;
  color: var(--gray-500);
  margin-bottom: 28px;
  flex-wrap: wrap;
}
.page-breadcrumb a {
  color: var(--navy);
  font-weight: 600;
  transition: var(--transition);
  display: flex;
  align-items: center;
  gap: 5px;
  text-decoration: none;
}
.page-breadcrumb a:hover { color: var(--gold); }
.page-breadcrumb i.fa-chevron-right { font-size: 10px; color: var(--gray-200); }
.page-breadcrumb span { color: var(--gold); font-weight: 500; }

/* Universal Blog Widget reset */
#main, #main .widget, #main .Blog,
#Blog1, .widget.Blog {
  background: transparent !important;
  padding: 0 !important;
  margin: 0 !important;
  box-shadow: none !important;
  border: none !important;
}
/* Card for post/page content */
#main .post-outer,
#main .post,
#main article,
#main .hentry,
.post-outer, .hentry {
  background: var(--white) !important;
  border-radius: var(--radius-lg) !important;
  padding: 40px !important;
  box-shadow: var(--shadow-sm) !important;
  border: 1px solid var(--gray-100) !important;
  margin-bottom: 24px !important;
}
/* Post Title */
h1.post-title, h2.post-title, h3.post-title,
.post-title, .entry-title,
.post-title a, .entry-title a {
  font-family: var(--font-head) !important;
  font-size: clamp(22px, 4vw, 32px) !important;
  font-weight: 800 !important;
  color: var(--navy) !important;
  line-height: 1.25 !important;
  margin-bottom: 20px !important;
  text-decoration: none !important;
  display: block !important;
}
/* Post Body */
.post-body, .entry-content {
  font-size: 15.5px !important;
  line-height: 1.85 !important;
  color: var(--gray-700) !important;
  display: block !important;
}
.post-body h2, .entry-content h2 {
  font-family: var(--font-head);
  font-size: 22px;
  color: var(--navy);
  border-bottom: 2px solid var(--gold);
  padding-bottom: 8px;
  margin: 28px 0 12px;
}
.post-body h3, .entry-content h3 {
  font-family: var(--font-head);
  font-size: 18px;
  color: var(--navy-light);
  margin: 20px 0 10px;
}
.post-body p, .entry-content p { margin-bottom: 16px; color: var(--gray-700); }
.post-body a, .entry-content a {
  color: var(--navy);
  font-weight: 600;
  border-bottom: 1px solid var(--gold);
  text-decoration: none;
  transition: var(--transition);
}
.post-body a:hover, .entry-content a:hover { color: var(--gold); }
.post-body ul, .post-body ol,
.entry-content ul, .entry-content ol { padding-left: 24px; margin-bottom: 16px; }
.post-body li, .entry-content li { margin-bottom: 8px; line-height: 1.7; color: var(--gray-700); }
.post-body img, .entry-content img {
  max-width: 100%; border-radius: var(--radius-md);
  margin: 16px 0; box-shadow: var(--shadow-sm); height: auto;
}
.post-body blockquote, .entry-content blockquote {
  border-left: 4px solid var(--gold); margin: 24px 0;
  padding: 16px 20px; background: rgba(245,168,0,.06);
  border-radius: 0 var(--radius-sm) var(--radius-sm) 0;
  font-style: italic; color: var(--gray-700);
}
.post-body table, .entry-content table {
  width: 100%; border-collapse: collapse; margin: 20px 0;
  font-size: 14px; box-shadow: var(--shadow-sm);
}
.post-body th, .entry-content th {
  background: var(--navy); color: var(--white);
  padding: 12px 16px; text-align: left; font-weight: 600;
}
.post-body td, .entry-content td {
  padding: 11px 16px; border-bottom: 1px solid var(--gray-100); color: var(--gray-700);
}
.post-body tr:nth-child(even) td,
.entry-content tr:nth-child(even) td { background: var(--off-white); }
/* Labels */
.post-labels a, .post-footer .label a {
  display: inline-block; background: rgba(245,168,0,.12);
  color: var(--navy); padding: 3px 10px; border-radius: 50px;
  font-size: 11px; font-weight: 600; margin: 4px 3px;
  text-decoration: none; border-bottom: none !important;
}
.post-labels a:hover { background: var(--gold); color: var(--navy); }
/* Date/meta */
.post-timestamp a, .date-header span, .published {
  font-size: 12px; color: var(--gray-500) !important;
  text-decoration: none; border-bottom: none !important;
}
/* Pager */
.blog-pager { display: flex; justify-content: space-between; gap: 12px; margin-top: 32px; flex-wrap: wrap; }
.blog-pager a {
  display: inline-flex !important; align-items: center; gap: 8px;
  padding: 10px 22px !important; background: var(--navy) !important;
  color: var(--white) !important; border-radius: 50px !important;
  font-size: 13px !important; font-weight: 600 !important;
  text-decoration: none !important; border-bottom: none !important;
  transition: var(--transition) !important;
}
.blog-pager a:hover { background: var(--gold) !important; color: var(--navy) !important; }
/* Comments */
#comments {
  background: var(--white); border-radius: var(--radius-lg);
  padding: 32px 40px; margin-top: 24px;
  box-shadow: var(--shadow-sm); border: 1px solid var(--gray-100);
}
#comments h4 { font-family: var(--font-head); font-size: 20px; color: var(--navy); margin-bottom: 20px; }
@media(max-width:600px) {
  #main .post-outer, #main .post, #main article, .hentry { padding: 24px 18px !important; }
  .page-content-area { padding: 90px 0 48px; }
}
.post-body,
.entry-content,
.post-body p,
.post-body div {
  display: block !important;
  visibility: visible !important;
  opacity: 1 !important;
  height: auto !important;
  max-height: none !important;
  overflow: visible !important;
  color: #000 !important;
  font-size: 16px !important;
  position: relative !important;
  z-index: 999 !important;
}

  ]]></b:skin>
</head>

<body>

<!-- Page Loader -->
<div id='page-loader'/>

<!-- ============================================================
     NOTICE BAR
     ============================================================ -->
<div class='notice-bar' id='noticeBar'>
  <i class='fas fa-bullhorn'/>
  <div class='notice-ticker'>
    <div class='notice-ticker-inner'>
      <span>📢 Admissions Open for Academic Year 2025-26 &#8212; Nursery to Class 10 &#183; Apply Now!</span>
      <span>🏆 MLZS Bhagalpur &#8212; CBSE Affiliated School (Affil. No. 330715) | Est. 2015</span>
      <span>📅 Annual Sports Day &#8212; All parents warmly invited. Stay tuned for the date!</span>
      <span>🎓 Co-Ed &#183; English Medium &#183; Managed by Balaji Education Trust, Bhagalpur</span>
      <span>📢 Admissions Open for Academic Year 2025-26 &#8212; Nursery to Class 10 &#183; Apply Now!</span>
      <span>🏆 MLZS Bhagalpur &#8212; CBSE Affiliated School (Affil. No. 330715) | Est. 2015</span>
      <span>📅 Annual Sports Day &#8212; All parents warmly invited. Stay tuned for the date!</span>
      <span>🎓 Co-Ed &#183; English Medium &#183; Managed by Balaji Education Trust, Bhagalpur</span>
    </div>
  </div>
  <span class='close-notice' onclick='document.getElementById(&apos;noticeBar&apos;).style.display=&apos;none&apos;'>&#215;</span>
</div>

<!-- ============================================================
     STICKY HEADER
     ============================================================ -->
<header id='gps-header'>
  <div class='header-inner'>
    <!-- Logo -->
    <a class='logo-wrap' href='https://demowebschool.blogspot.com/'>
      <div class='logo-icon'>
        <svg fill='none' viewBox='0 0 26 26' xmlns='http://www.w3.org/2000/svg'>
          <path d='M13 2L3 7v6c0 5.55 4.27 10.74 10 12 5.73-1.26 10-6.45 10-12V7L13 2z' fill='#F5A800'/>
          <path d='M10 13l2 2 4-4' stroke='#0D1B3E' stroke-linecap='round' stroke-linejoin='round' stroke-width='2'/>
        </svg>
      </div>
      <div class='logo-text'>
        <span class='school-name'>Mount Litera Zee</span>
        <span class='school-sub'>CBSE Affiliated &#183; Bhagalpur</span>
      </div>
    </a>

    <!-- Desktop Nav -->
    <nav class='nav-desktop'>
      <a class='active' href='https://demowebschool.blogspot.com/'>Home</a>

      <!-- About Us dropdown -->
      <div class='has-dropdown'>
        <a href='https://demowebschool.blogspot.com/p/about-us.html'>About Us <i class='fas fa-chevron-down dd-arrow'/></a>
        <div class='dropdown-menu'>
          <a href='https://demowebschool.blogspot.com/p/about-us.html'><i class='fas fa-info-circle'/> About MLZS</a>
          <a href='https://demowebschool.blogspot.com/p/principal-message.html'><i class='fas fa-user-tie'/> Principal&#39;s Message</a>
          <a href='https://demowebschool.blogspot.com/p/vision-mission.html'><i class='fas fa-eye'/> Vision &amp; Mission</a>
          <a href='https://demowebschool.blogspot.com/p/management.html'><i class='fas fa-users'/> Management</a>
        </div>
      </div>

      <!-- Academics dropdown -->
      <div class='has-dropdown'>
        <a href='https://demowebschool.blogspot.com/search/label/Academics'>Academics <i class='fas fa-chevron-down dd-arrow'/></a>
        <div class='dropdown-menu'>
          <a href='https://demowebschool.blogspot.com/p/school-timings.html'><i class='fas fa-clock'/> School Timings</a>
          <a href='https://demowebschool.blogspot.com/p/belief-philosophy.html'><i class='fas fa-lightbulb'/> Our Belief / Philosophy &amp; Practice</a>
          <a href='https://demowebschool.blogspot.com/p/term-examinations.html'><i class='fas fa-file-alt'/> Term Examinations</a>
          <a href='https://demowebschool.blogspot.com/p/syllabus.html'><i class='fas fa-book'/> Syllabus</a>
          <a href='https://demowebschool.blogspot.com/p/assignments.html'><i class='fas fa-tasks'/> Assignments</a>
          <a href='https://demowebschool.blogspot.com/search/label/Results'><i class='fas fa-chart-bar'/> Results</a>
          <a href='https://demowebschool.blogspot.com/search/label/Toppers'><i class='fas fa-trophy'/> Toppers</a>
        </div>
      </div>

      <!-- Admissions dropdown -->
      <div class='has-dropdown'>
        <a href='https://demowebschool.blogspot.com/p/admissions.html'>Admissions <i class='fas fa-chevron-down dd-arrow'/></a>
        <div class='dropdown-menu'>
          <a href='https://demowebschool.blogspot.com/p/admissions.html'><i class='fas fa-door-open'/> Apply for Admission</a>
          <a href='https://demowebschool.blogspot.com/p/fee-structure.html'><i class='fas fa-rupee-sign'/> Fee Structure</a>
          <a href='https://demowebschool.blogspot.com/p/admission-procedure.html'><i class='fas fa-list-ol'/> Admission Procedure</a>
          <a href='https://demowebschool.blogspot.com/p/scholarship.html'><i class='fas fa-award'/> Litera Shakti Scholarship</a>
        </div>
      </div>

      <a href='https://demowebschool.blogspot.com/p/facilities.html'>Facilities</a>
      <a href='https://demowebschool.blogspot.com/search/label/Gallery'>Gallery</a>
      <a href='https://demowebschool.blogspot.com/p/careers.html'>Careers</a>
      <a href='https://demowebschool.blogspot.com/p/cbse-corner.html'>CBSE Corner</a>
    </nav>

    <!-- Hamburger -->
    <div class='hamburger' id='hamburger' onclick='toggleMenu()'>
      <span/><span/><span/>
    </div>
  </div>
</header>

<!-- Mobile Menu -->
<div class='mobile-menu' id='mobileMenu'>
  <a href='https://demowebschool.blogspot.com/'><i class='fas fa-home'/> Home</a>

  <!-- About Us Accordion -->
  <div>
    <button class='mobile-acc-toggle' onclick='toggleAcc(this)'>
      <span style='display:flex;align-items:center;gap:14px'><i class='fas fa-school icon-left'/> About Us</span>
      <i class='fas fa-chevron-down acc-arrow'/>
    </button>
    <div class='mobile-acc-body'>
      <a href='https://demowebschool.blogspot.com/p/about-us.html'><i class='fas fa-info-circle'/> About MLZS</a>
      <a href='https://demowebschool.blogspot.com/p/principal-message.html'><i class='fas fa-user-tie'/> Principal&#39;s Message</a>
      <a href='https://demowebschool.blogspot.com/p/vision-mission.html'><i class='fas fa-eye'/> Vision &amp; Mission</a>
      <a href='https://demowebschool.blogspot.com/p/management.html'><i class='fas fa-users'/> Management</a>
    </div>
  </div>

  <!-- Academics Accordion -->
  <div>
    <button class='mobile-acc-toggle' onclick='toggleAcc(this)'>
      <span style='display:flex;align-items:center;gap:14px'><i class='fas fa-book-open icon-left'/> Academics</span>
      <i class='fas fa-chevron-down acc-arrow'/>
    </button>
    <div class='mobile-acc-body'>
      <a href='https://demowebschool.blogspot.com/p/school-timings.html'><i class='fas fa-clock'/> School Timings</a>
      <a href='https://demowebschool.blogspot.com/p/belief-philosophy.html'><i class='fas fa-lightbulb'/> Our Belief / Philosophy &amp; Practice</a>
      <a href='https://demowebschool.blogspot.com/p/term-examinations.html'><i class='fas fa-file-alt'/> Term Examinations</a>
      <a href='https://demowebschool.blogspot.com/p/syllabus.html'><i class='fas fa-book'/> Syllabus</a>
      <a href='https://demowebschool.blogspot.com/p/assignments.html'><i class='fas fa-tasks'/> Assignments</a>
      <a href='https://demowebschool.blogspot.com/search/label/Results'><i class='fas fa-chart-bar'/> Results</a>
      <a href='https://demowebschool.blogspot.com/search/label/Toppers'><i class='fas fa-trophy'/> Toppers</a>
    </div>
  </div>

  <!-- Admissions Accordion -->
  <div>
    <button class='mobile-acc-toggle' onclick='toggleAcc(this)'>
      <span style='display:flex;align-items:center;gap:14px'><i class='fas fa-graduation-cap icon-left'/> Admissions</span>
      <i class='fas fa-chevron-down acc-arrow'/>
    </button>
    <div class='mobile-acc-body'>
      <a href='https://demowebschool.blogspot.com/p/admissions.html'><i class='fas fa-door-open'/> Apply for Admission</a>
      <a href='https://demowebschool.blogspot.com/p/fee-structure.html'><i class='fas fa-rupee-sign'/> Fee Structure</a>
      <a href='https://demowebschool.blogspot.com/p/admission-procedure.html'><i class='fas fa-list-ol'/> Admission Procedure</a>
      <a href='https://demowebschool.blogspot.com/p/scholarship.html'><i class='fas fa-award'/> Litera Shakti Scholarship</a>
    </div>
  </div>

  <a href='https://demowebschool.blogspot.com/p/facilities.html'><i class='fas fa-building'/> Facilities</a>
  <a href='https://demowebschool.blogspot.com/search/label/Gallery'><i class='fas fa-images'/> Gallery</a>
  <a href='https://demowebschool.blogspot.com/p/careers.html'><i class='fas fa-briefcase'/> Careers</a>
  <a href='https://demowebschool.blogspot.com/p/cbse-corner.html'><i class='fas fa-certificate'/> CBSE Corner</a>
  <a href='https://demowebschool.blogspot.com/p/contact.html'><i class='fas fa-phone'/> Contact Us</a>
  <div class='mobile-menu-cta'>
    <a class='btn btn-primary' href='https://demowebschool.blogspot.com/p/admissions.html'><i class='fas fa-file-alt'/> Apply Now</a>
    <a class='btn btn-outline' href='https://demowebschool.blogspot.com/p/contact.html'><i class='fas fa-calendar-alt'/> Book a Visit</a>
  </div>
</div>

<!-- ============================================================
     MAIN CONTENT
     ============================================================ -->
<main>

<!-- ================================================================
     BLOGGER PAGE TYPE CONDITIONAL
     Homepage sections ONLY show on index/home page.
     All other pages (static pages, posts, labels) show Blog widget.
     ================================================================ -->
<b:if cond='data:blog.pageType == &quot;index&quot;'>

<!-- ============================================================
     HERO SECTION
     ============================================================ -->
<section id='gps-hero'>
  <div class='hero-bg'/>
  <div class='hero-overlay'/>
  <div class='hero-content'>
    <div class='hero-badge'>
      <i class='fas fa-award'/> CBSE Affiliated &#183; Affil. No. 330715 &#183; Est. 2015
    </div>
    <h1 class='hero-title'>
      Shaping Young Minds<br/>for a <span>Better Tomorrow</span>
    </h1>
    <p class='hero-subtitle'>
      Nurturing curiosity, building confidence, and preparing students for a bright future through excellence in education.
    </p>
    <div class='hero-btns'>
      <a class='btn btn-primary' href='https://demowebschool.blogspot.com/p/admissions.html'>
        <i class='fas fa-file-alt'/> Apply Now
      </a>
      <a class='btn btn-outline' href='https://demowebschool.blogspot.com/p/contact.html'>
        <i class='fas fa-calendar-alt'/> Book a Visit
      </a>
    </div>
  </div>
  <div class='hero-scroll'>
    <span>Scroll</span>
    <i class='fas fa-chevron-down'/>
  </div>
</section>

<!-- ============================================================
     STATS SECTION
     ============================================================ -->
<section id='gps-stats'>
  <div class='stats-grid'>
    <div class='stat-card animate-in'>
      <div class='stat-icon yellow'><i class='fas fa-user-graduate'/></div>
      <span class='stat-number' data-target='1500'>0</span>
      <span class='stat-label'>Students Enrolled</span>
    </div>
    <div class='stat-card animate-in' style='transition-delay:0.1s'>
      <div class='stat-icon blue'><i class='fas fa-chalkboard-teacher'/></div>
      <span class='stat-number' data-target='80'>0</span>
      <span class='stat-label'>Expert Teachers</span>
    </div>
    <div class='stat-card animate-in' style='transition-delay:0.2s'>
      <div class='stat-icon green'><i class='fas fa-trophy'/></div>
      <span class='stat-number' data-target='20'>0</span>
      <span class='stat-label'>Awards Won</span>
    </div>
    <div class='stat-card animate-in' style='transition-delay:0.3s'>
      <div class='stat-icon purple'><i class='fas fa-building-columns'/></div>
      <span class='stat-number' data-target='20'>0</span>
      <span class='stat-label'>Years of Excellence</span>
    </div>
  </div>
</section>

<!-- ============================================================
     MLZS AFFILIATION INFO STRIP
     ============================================================ -->
<div style='background:var(--navy);padding:18px 20px;'>
  <div style='max-width:1200px;margin:0 auto;display:flex;flex-wrap:wrap;gap:10px 28px;align-items:center;justify-content:center;'>
    <div style='display:flex;align-items:center;gap:8px;color:rgba(255,255,255,0.85);font-size:13px;font-weight:500;'>
      <i class='fas fa-certificate' style='color:#F5A800'/> <span>CBSE Affiliated</span>
      <span style='color:rgba(255,255,255,0.35)'>|</span>
      <span style='color:#F5A800;font-weight:700'>Affil. No. 330715</span>
    </div>
    <div style='display:flex;align-items:center;gap:8px;color:rgba(255,255,255,0.85);font-size:13px;font-weight:500;'>
      <i class='fas fa-school' style='color:#F5A800'/> <span>Est. 2015 &#183; Balaji Education Trust</span>
    </div>
    <div style='display:flex;align-items:center;gap:8px;color:rgba(255,255,255,0.85);font-size:13px;font-weight:500;'>
      <i class='fas fa-venus-mars' style='color:#F5A800'/> <span>Co-Ed &#183; English Medium</span>
    </div>
    <div style='display:flex;align-items:center;gap:8px;color:rgba(255,255,255,0.85);font-size:13px;font-weight:500;'>
      <i class='fas fa-book-open' style='color:#F5A800'/> <span>Nursery to Class 10</span>
    </div>
    <div style='display:flex;align-items:center;gap:8px;color:rgba(255,255,255,0.85);font-size:13px;font-weight:500;'>
      <i class='fas fa-map-pin' style='color:#F5A800'/> <span>Bhagalpur, Bihar</span>
    </div>
  </div>
</div>

<!-- ============================================================
     WHY CHOOSE US
     ============================================================ -->
<section id='gps-why'>
  <div class='container'>
    <div class='why-header animate-in'>
      <span class='section-tag'>Why Choose Us</span>
      <h2 class='section-title'>Providing the Best<br/>for Our Students</h2>
      <p class='section-subtitle'>We combine modern infrastructure with dedicated faculty to deliver a holistic educational experience.</p>
    </div>
    <div class='features-scroll'>
      <div class='feature-card animate-in'>
        <div class='feature-icon fi-1'><i class='fas fa-desktop'/></div>
        <span class='feature-name'>Smart Classes</span>
      </div>
      <div class='feature-card animate-in' style='transition-delay:0.08s'>
        <div class='feature-icon fi-2'><i class='fas fa-flask'/></div>
        <span class='feature-name'>Science Lab</span>
      </div>
      <div class='feature-card animate-in' style='transition-delay:0.16s'>
        <div class='feature-icon fi-3'><i class='fas fa-futbol'/></div>
        <span class='feature-name'>Sports Facilities</span>
      </div>
      <div class='feature-card animate-in' style='transition-delay:0.24s'>
        <div class='feature-icon fi-4'><i class='fas fa-book'/></div>
        <span class='feature-name'>Library</span>
      </div>
      <div class='feature-card animate-in' style='transition-delay:0.32s'>
        <div class='feature-icon fi-5'><i class='fas fa-shield-halved'/></div>
        <span class='feature-name'>Safe &amp; Secure Campus</span>
      </div>
    </div>
  </div>
</section>

<!-- ============================================================
     LATEST UPDATES &#8212; Dynamic Blogger Posts
     ============================================================ -->
<section id='gps-updates'>
  <div class='container'>
    <div class='section-header animate-in'>
      <div>
        <span class='section-tag'>Stay Informed</span>
        <h2 class='section-title' style='margin-bottom:0'>Latest Updates</h2>
      </div>
      <a class='view-all' href='https://demowebschool.blogspot.com/'>View All <i class='fas fa-arrow-right'/></a>
    </div>

    <!-- Blogger Recent Posts Widget -->
    <div class='updates-grid' id='dynamicUpdates'>
      <!-- Static fallback cards shown until JS loads -->
      <div class='update-card animate-in'>
        <div class='update-icon-wrap ui-blue'><i class='fas fa-bullhorn'/></div>
        <div class='update-meta'>
          <div class='update-label'>Admissions</div>
          <div class='update-title'>Admissions Open for 2025-26 &#8212; Nursery to Class 10</div>
          <div class='update-date'><i class='far fa-calendar'/> 1 May, 2025</div>
        </div>
      </div>
      <div class='update-card animate-in' style='transition-delay:0.1s'>
        <div class='update-icon-wrap ui-green'><i class='fas fa-sun'/></div>
        <div class='update-meta'>
          <div class='update-label'>Notice</div>
          <div class='update-title'>Summer Vacation Notice &#8212; School Closed During Vacation Period</div>
          <div class='update-date'><i class='far fa-calendar'/> 28 Apr, 2025</div>
        </div>
      </div>
      <div class='update-card animate-in' style='transition-delay:0.2s'>
        <div class='update-icon-wrap ui-purple'><i class='fas fa-clipboard-list'/></div>
        <div class='update-meta'>
          <div class='update-label'>Exams</div>
          <div class='update-title'>Annual Examination Schedule Released &#8212; Download from School App</div>
          <div class='update-date'><i class='far fa-calendar'/> 25 Apr, 2025</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- Blogger Posts Feed Script &#8212; loads real posts dynamically -->
<script>
//<![CDATA[
(function() {
  var blogUrl = '<data:blog.homepageUrl/>';
  var feedUrl = blogUrl + 'feeds/posts/summary?alt=json&max-results=6';
  var iconMap = [
    {wrap:'ui-blue',  icon:'fas fa-bullhorn', label:'News'},
    {wrap:'ui-green', icon:'fas fa-calendar', label:'Event'},
    {wrap:'ui-purple',icon:'fas fa-clipboard-list', label:'Notice'},
    {wrap:'ui-blue',  icon:'fas fa-star', label:'Update'},
    {wrap:'ui-green', icon:'fas fa-trophy', label:'Achievement'},
    {wrap:'ui-purple',icon:'fas fa-book', label:'Academics'}
  ];

  function formatDate(str) {
    var d = new Date(str);
    return d.toLocaleDateString('en-IN', {day:'numeric', month:'short', year:'numeric'});
  }

  function renderPosts(data) {
    var entries = (data.feed && data.feed.entry) ? data.feed.entry : [];
    if (!entries.length) return;
    var container = document.getElementById('dynamicUpdates');
    if (!container) return;
    container.innerHTML = '';
    entries.slice(0, 6).forEach(function(e, i) {
      var title = e.title.$t;
      var link = '';
      if (e.link) {
        e.link.forEach(function(l){ if (l.rel === 'alternate') link = l.href; });
      }
      var date = e.published ? formatDate(e.published.$t) : '';
      var m = iconMap[i % iconMap.length];
      var card = document.createElement('a');
      card.href = link;
      card.className = 'update-card animate-in';
      card.style.transitionDelay = (i * 0.1) + 's';
      card.innerHTML = '<div class="update-icon-wrap ' + m.wrap + '"><i class="' + m.icon + '"></i></div>' +
        '<div class="update-meta">' +
        '<div class="update-label">' + m.label + '</div>' +
        '<div class="update-title">' + title + '</div>' +
        '<div class="update-date"><i class="far fa-calendar"></i> ' + date + '</div>' +
        '</div>';
      container.appendChild(card);
    });
    observeAnimations();
  }

  var s = document.createElement('script');
  s.src = feedUrl + '&callback=gpsLoadPosts';
  window.gpsLoadPosts = renderPosts;
  document.head.appendChild(s);
})();
//]]>
</script>

<!-- ============================================================
     GALLERY SECTION
     ============================================================ -->
<section id='gps-gallery'>
  <div class='container'>
    <div class='animate-in'>
      <span class='section-tag'>Our Campus Life</span>
      <h2 class='section-title'>Moments That Matter</h2>
      <p class='section-subtitle'>A glimpse into the vibrant life at Greenfield &#8212; from classrooms to sports grounds.</p>
    </div>
    <div class='gallery-grid'>
      <div class='gallery-item animate-in'>
        <img alt='Students in classroom' loading='lazy' src='https://images.pexels.com/photos/5212345/pexels-photo-5212345.jpeg?auto=compress&amp;w=600'/>
        <div class='gallery-overlay'><i class='fas fa-expand'/></div>
      </div>
      <div class='gallery-item animate-in'>
        <img alt='Science lab' loading='lazy' src='https://images.pexels.com/photos/8471835/pexels-photo-8471835.jpeg?auto=compress&amp;w=400'/>
        <div class='gallery-overlay'><i class='fas fa-expand'/></div>
      </div>
      <div class='gallery-item animate-in'>
        <img alt='Library' loading='lazy' src='https://images.pexels.com/photos/1181671/pexels-photo-1181671.jpeg?auto=compress&amp;w=400'/>
        <div class='gallery-overlay'><i class='fas fa-expand'/></div>
      </div>
      <div class='gallery-item animate-in'>
        <img alt='Sports' loading='lazy' src='https://images.pexels.com/photos/3621104/pexels-photo-3621104.jpeg?auto=compress&amp;w=400'/>
        <div class='gallery-overlay'><i class='fas fa-expand'/></div>
      </div>
      <div class='gallery-item animate-in'>
        <img alt='Students outdoors' loading='lazy' src='https://images.pexels.com/photos/8471759/pexels-photo-8471759.jpeg?auto=compress&amp;w=400'/>
        <div class='gallery-overlay'><i class='fas fa-expand'/></div>
      </div>
      <div class='gallery-item animate-in'>
        <img alt='Cultural event' loading='lazy' src='https://images.pexels.com/photos/8471831/pexels-photo-8471831.jpeg?auto=compress&amp;w=400'/>
        <div class='gallery-overlay'><i class='fas fa-expand'/></div>
      </div>
    </div>
  </div>
</section>

<!-- ============================================================
     TESTIMONIALS SLIDER
     ============================================================ -->
<section id='gps-testimonials'>
  <div class='container'>
    <div class='animate-in'>
      <span class='section-tag'>Parent Testimonials</span>
      <h2 class='section-title' style='color:var(--white)'>What Parents Say</h2>
    </div>
    <div class='testi-slider' id='testiSlider'>
      <div class='testi-track' id='testiTrack'>

        <div class='testi-card'>
          <div class='testi-stars'>
            <i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star'/>
          </div>
          <p class='testi-text'>&quot;Greenfield has transformed my daughter&#39;s approach to learning. The teachers are incredibly dedicated and the smart classroom technology keeps students engaged like never before.&quot;</p>
          <div class='testi-author'>
            <div class='testi-avatar'>P</div>
            <div>
              <div class='testi-name'>Priya Sharma</div>
              <div class='testi-role'>Parent of Class VIII Student</div>
            </div>
          </div>
        </div>

        <div class='testi-card'>
          <div class='testi-stars'>
            <i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star'/>
          </div>
          <p class='testi-text'>&quot;The sports facilities and extracurricular activities at Greenfield are exceptional. My son has grown not just academically but as a confident individual ready for the real world.&quot;</p>
          <div class='testi-author'>
            <div class='testi-avatar'>R</div>
            <div>
              <div class='testi-name'>Rajesh Kumar</div>
              <div class='testi-role'>Parent of Class X Student</div>
            </div>
          </div>
        </div>

        <div class='testi-card'>
          <div class='testi-stars'>
            <i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star'/>
          </div>
          <p class='testi-text'>&quot;The safe campus environment and the constant communication from teachers gives me complete peace of mind. Greenfield truly feels like a second home for our children.&quot;</p>
          <div class='testi-author'>
            <div class='testi-avatar'>A</div>
            <div>
              <div class='testi-name'>Anita Verma</div>
              <div class='testi-role'>Parent of Class VI Student</div>
            </div>
          </div>
        </div>

        <div class='testi-card'>
          <div class='testi-stars'>
            <i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star'/><i class='fas fa-star-half-alt'/>
          </div>
          <p class='testi-text'>&quot;Twenty years of excellence is not just a tagline &#8212; it&#39;s something you feel the moment you walk through the gates. The discipline and values instilled here are priceless.&quot;</p>
          <div class='testi-author'>
            <div class='testi-avatar'>S</div>
            <div>
              <div class='testi-name'>Suresh Patel</div>
              <div class='testi-role'>Parent of Class XII Student</div>
            </div>
          </div>
        </div>

      </div>

      <div class='testi-controls'>
        <button class='testi-btn' id='testiPrev'><i class='fas fa-chevron-left'/></button>
        <div class='testi-dots' id='testiDots'/>
        <button class='testi-btn' id='testiNext'><i class='fas fa-chevron-right'/></button>
      </div>
    </div>
  </div>
</section>

<!-- ============================================================
     ADMISSIONS CTA
     ============================================================ -->
<section class='animate-in' id='gps-cta'>
  <div class='container'>
    <span class='section-tag'>Join Our Family</span>
    <h2 class='section-title'>Admissions Open for 2025-26</h2>
    <p>Nursery to Class 10 &#183; Co-Ed &#183; English Medium &#183; CBSE Affiliated (No. 330715) &#183; Limited seats available.</p>
    <a class='btn-navy' href='https://demowebschool.blogspot.com/p/admissions.html'>
      <i class='fas fa-graduation-cap'/> Apply for Admission
    </a>
  </div>
</section>

<!-- ============================================================
     DYNAMIC BLOGGER POSTS &#8212; JSON Feed (no widget needed)
     ============================================================ -->

<!-- END of Homepage conditional -->
</b:if>

<!-- ================================================================
     BLOG WIDGET &#8212; Always present (Blog1 is Blogger's required widget)
     Hidden on homepage via CSS class added by JS
     Shows full page content on static pages, posts, labels
     ================================================================ -->
<div class='page-content-area' id='gps-page-area'>
  <div class='page-inner container'>
    <!-- Page Breadcrumb -->
    <div class='page-breadcrumb'>
      <a href='https://demowebschool.blogspot.com/'><i class='fas fa-home'/> Home</a>
      <i class='fas fa-chevron-right'/>
      <span><data:blog.pageName/></span>
    </div>
    <!-- Blogger renders page/post/label content here -->
    <b:section class='main' id='main' maxwidgets='1' showaddelement='no'>
      <b:widget id='Blog1' locked='true' title='Blog Posts' type='Blog'>
        <b:widget-settings>
          <b:widget-setting name='showDateHeader'>true</b:widget-setting>
          <b:widget-setting name='style.textcolor'>#ffffff</b:widget-setting>
          <b:widget-setting name='showShareButtons'>true</b:widget-setting>
          <b:widget-setting name='authorLabel'>By</b:widget-setting>
          <b:widget-setting name='showCommentLink'>true</b:widget-setting>
          <b:widget-setting name='style.urlcolor'>#ffffff</b:widget-setting>
          <b:widget-setting name='showAuthor'>false</b:widget-setting>
          <b:widget-setting name='style.linkcolor'>#ffffff</b:widget-setting>
          <b:widget-setting name='style.unittype'>TextAndImage</b:widget-setting>
          <b:widget-setting name='style.bgcolor'>#ffffff</b:widget-setting>
          <b:widget-setting name='reactionsLabel'/>
          <b:widget-setting name='showAuthorProfile'>false</b:widget-setting>
          <b:widget-setting name='style.layout'>1x1</b:widget-setting>
          <b:widget-setting name='showLabels'>true</b:widget-setting>
          <b:widget-setting name='showLocation'>false</b:widget-setting>
          <b:widget-setting name='showTimestamp'>true</b:widget-setting>
          <b:widget-setting name='postsPerAd'>3</b:widget-setting>
          <b:widget-setting name='showBacklinks'>false</b:widget-setting>
          <b:widget-setting name='style.bordercolor'>#ffffff</b:widget-setting>
          <b:widget-setting name='showInlineAds'>true</b:widget-setting>
          <b:widget-setting name='showReactions'>false</b:widget-setting>
        </b:widget-settings>
        <b:includable id='main' var='top'>
  <b:if cond='!data:mobile'>
    <!-- posts -->
    <div class='blog-posts hfeed'>

      <b:include data='top' name='status-message'/>

      <b:loop values='data:posts' var='post'>
        <b:if cond='data:post.isDateStart and not data:post.isFirstPost'>
          &lt;/div&gt;&lt;/div&gt;
        </b:if>
        <b:if cond='data:post.isDateStart'>
          &lt;div class=&quot;date-outer&quot;&gt;
        </b:if>
        <b:if cond='data:post.dateHeader'>
          <h2 class='date-header'><span><data:post.dateHeader/></span></h2>
        </b:if>
        <b:if cond='data:post.isDateStart'>
          &lt;div class=&quot;date-posts&quot;&gt;
        </b:if>
        <div class='post-outer'>
          <b:include data='post' name='post'/>
          <b:include cond='data:blog.pageType in {&quot;static_page&quot;,&quot;item&quot;}' data='post' name='comment_picker'/>
        </div>

        <!-- Ad -->
        <b:if cond='data:post.includeAd'>
          <div class='inline-ad'>
            <data:adCode/>
          </div>
        </b:if>
      </b:loop>
      <b:if cond='data:numPosts != 0'>
        &lt;/div&gt;&lt;/div&gt;
      </b:if>
    </div>

    <!-- navigation -->
    <b:include name='nextprev'/>

    <!-- feed links -->
    <b:include name='feedLinks'/>

  <b:else/>
    <b:include name='mobile-main'/>
  </b:if>
</b:includable>
        <b:includable id='backlinkDeleteIcon' var='backlink'/>
        <b:includable id='backlinks' var='post'/>
        <b:includable id='comment-form' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <b:if cond='data:mobile'>
      <h4 id='comment-post-message'>
        <a expr:id='data:widget.instanceId + &quot;_comment-editor-toggle-link&quot;' href='javascript:void(0)'><data:postCommentMsg/></a></h4>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' style='display: none' width='100%'/>
    <b:else/>
      <h4 id='comment-post-message'><data:postCommentMsg/></h4>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
    </b:if>
    <data:post.cmtfpIframe/>
    <script type='text/javascript'>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
    </script>
  </div>
</b:includable>
        <b:includable id='commentDeleteIcon' var='comment'>
  <span expr:class='&quot;item-control &quot; + data:comment.adminClass'>
    <b:if cond='data:showCmtPopup'>
      <div class='goog-toggle-button'>
        <div class='goog-inline-block comment-action-icon'/>
      </div>
    <b:else/>
      <a class='comment-delete' expr:href='data:comment.deleteUrl' expr:title='data:top.deleteCommentMsg'>
        <img src='https://resources.blogblog.com/img/icon_delete13.gif'/>
      </a>
    </b:if>
  </span>
</b:includable>
        <b:includable id='comment_count_picker' var='post'>
  <a class='comment-link' expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'>
    <data:post.commentLabelFull/>:
  </a>
</b:includable>
        <b:includable id='comment_picker' var='post'>
  <b:if cond='data:post.showThreadedComments'>
    <b:include data='post' name='threaded_comments'/>
  <b:else/>
    <b:include data='post' name='comments'/>
  </b:if>
</b:includable>
        <b:includable id='comments' var='post'>
  <div class='comments' id='comments'>
    <a name='comments'/>
    <b:if cond='data:post.allowComments'>
      <h4><data:post.commentLabelFull/>:</h4>

      <b:if cond='data:post.commentPagingRequired'>
        <span class='paging-control-container'>
          <b:if cond='data:post.hasOlderLinks'>
            <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'><data:post.oldestLinkText/></a>
              &#160;
            <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'><data:post.olderLinkText/></a>
              &#160;
          </b:if>

          <data:post.commentRangeText/>

          <b:if cond='data:post.hasNewerLinks'>
            &#160;
            <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'><data:post.newerLinkText/></a>
            &#160;
            <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'><data:post.newestLinkText/></a>
          </b:if>
        </span>
      </b:if>

      <div expr:id='data:widget.instanceId + &quot;_comments-block-wrapper&quot;'>
        <dl expr:class='data:post.avatarIndentClass' id='comments-block'>
          <b:loop values='data:post.comments' var='comment'>
            <dt expr:class='&quot;comment-author &quot; + data:comment.authorClass' expr:id='data:comment.anchorName'>
              <b:if cond='data:comment.favicon'>
                <img expr:src='data:comment.favicon' height='16px' style='margin-bottom:-2px;' width='16px'/>
              </b:if>
              <a expr:name='data:comment.anchorName'/>
              <b:if cond='data:blog.enabledCommentProfileImages'>
                <data:comment.authorAvatarImage/>
              </b:if>
              <b:if cond='data:comment.authorUrl'>
                <a expr:href='data:comment.authorUrl' rel='nofollow'><data:comment.author/></a>
              <b:else/>
                <data:comment.author/>
              </b:if>
              <data:commentPostedByMsg/>
            </dt>
            <dd class='comment-body' expr:id='data:widget.instanceId + data:comment.cmtBodyIdPostfix'>
              <b:if cond='data:comment.isDeleted'>
                <span class='deleted-comment'><data:comment.body/></span>
              <b:else/>
                <p>
                  <data:comment.body/>
                </p>
              </b:if>
            </dd>
            <dd class='comment-footer'>
              <span class='comment-timestamp'>
                <a expr:href='data:comment.url' title='comment permalink'>
                  <data:comment.timestamp/>
                </a>
                <b:include data='comment' name='commentDeleteIcon'/>
              </span>
            </dd>
          </b:loop>
        </dl>
      </div>

      <b:if cond='data:post.commentPagingRequired'>
        <span class='paging-control-container'>
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.oldestLinkUrl'>
            <data:post.oldestLinkText/>
          </a>
          <a expr:class='data:post.oldLinkClass' expr:href='data:post.olderLinkUrl'>
            <data:post.olderLinkText/>
          </a>
          &#160;
          <data:post.commentRangeText/>
          &#160;
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newerLinkUrl'>
            <data:post.newerLinkText/>
          </a>
          <a expr:class='data:post.newLinkClass' expr:href='data:post.newestLinkUrl'>
            <data:post.newestLinkText/>
          </a>
        </span>
      </b:if>

      <p class='comment-footer'>
        <b:if cond='data:post.embedCommentForm'>
          <b:if cond='data:post.allowNewComments'>
            <b:include data='post' name='comment-form'/>
          <b:else/>
            <data:post.noNewCommentsText/>
          </b:if>
        <b:elseif cond='data:post.allowComments'/>
          <a expr:href='data:post.addCommentUrl' expr:onclick='data:post.addCommentOnclick'><data:postCommentMsg/></a>
        </b:if>
      </p>
    </b:if>
    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='true' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>

  </div>
</b:includable>
        <b:includable id='feedLinks'>
  <b:if cond='data:blog.pageType != &quot;item&quot;'> <!-- Blog feed links -->
    <b:if cond='data:feedLinks'>
      <div class='blog-feeds'>
        <b:include data='feedLinks' name='feedLinksBody'/>
      </div>
    </b:if>

  <b:else/> <!--Post feed links -->
    <div class='post-feeds'>
      <b:loop values='data:posts' var='post'>
        <b:include cond='data:post.allowComments and data:post.feedLinks' data='post.feedLinks' name='feedLinksBody'/>
      </b:loop>
    </div>
  </b:if>
</b:includable>
        <b:includable id='feedLinksBody' var='links'>
  <div class='feed-links'>
  <data:feedLinksMsg/>
  <b:loop values='data:links' var='f'>
     <a class='feed-link' expr:href='data:f.url' expr:type='data:f.mimeType' target='_blank'><data:f.name/> (<data:f.feedType/>)</a>
  </b:loop>
  </div>
</b:includable>
        <b:includable id='iframe_comments' var='post'>
  <!-- G+ comments, no longer available. The includable is retained for backwards-compatibility. -->
</b:includable>
        <b:includable id='mobile-index-post' var='post'>
  <div class='mobile-date-outer date-outer'>
    <b:if cond='data:post.dateHeader'>
      <div class='date-header'>
        <span><data:post.dateHeader/></span>
      </div>
    </b:if>

    <div class='mobile-post-outer'>
      <a expr:href='data:post.url'>
        <h3 class='mobile-index-title entry-title' itemprop='name'>
          <data:post.title/>
        </h3>

        <div class='mobile-index-arrow'>&amp;rsaquo;</div>

        <div class='mobile-index-contents'>
          <b:if cond='data:post.thumbnailUrl'>
            <div class='mobile-index-thumbnail'>
              <div class='Image'>
                <img expr:src='data:post.thumbnailUrl'/>
              </div>
            </div>
          </b:if>

          <div class='post-body'>
            <b:if cond='data:post.snippet'><data:post.snippet/></b:if>
          </div>
        </div>

        <div style='clear: both;'/>
      </a>

      <div class='mobile-index-comment'>
        <b:include cond='data:blog.pageType != &quot;static_page&quot;                          and data:post.allowComments                          and data:post.numComments != 0' data='post' name='comment_count_picker'/>
      </div>
    </div>
  </div>
</b:includable>
        <b:includable id='mobile-main' var='top'>
    <!-- posts -->
    <div class='blog-posts hfeed'>

      <b:include data='top' name='status-message'/>

      <b:if cond='data:blog.pageType == &quot;index&quot;'>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='mobile-index-post'/>
        </b:loop>
      <b:else/>
        <b:loop values='data:posts' var='post'>
          <b:include data='post' name='mobile-post'/>
        </b:loop>
      </b:if>
    </div>

   <b:include name='mobile-nextprev'/>
</b:includable>
        <b:includable id='mobile-nextprev'>
  <div class='blog-pager' id='blog-pager'>
    <b:if cond='data:newerPageUrl'>
      <div class='mobile-link-button' id='blog-pager-newer-link'>
      <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'>&amp;lsaquo;</a>
      </div>
    </b:if>

    <b:if cond='data:olderPageUrl'>
      <div class='mobile-link-button' id='blog-pager-older-link'>
      <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'>&amp;rsaquo;</a>
      </div>
    </b:if>

    <div class='mobile-link-button' id='blog-pager-home-link'>
    <a class='home-link' expr:href='data:blog.homepageUrl'><data:homeMsg/></a>
    </div>

    <div class='mobile-desktop-link'>
      <a class='home-link' expr:href='data:desktopLinkUrl'><data:desktopLinkMsg/></a>
    </div>

  </div>
  <div class='clear'/>
</b:includable>
        <b:includable id='mobile-post' var='post'>
  <div class='date-outer'>
    <b:if cond='data:post.dateHeader'>
      <h2 class='date-header'><span><data:post.dateHeader/></span></h2>
    </b:if>
    <div class='date-posts'>
      <div class='post-outer'>

        <div class='post hentry uncustomized-post-template' itemscope='itemscope' itemtype='http://schema.org/BlogPosting'>
          <b:if cond='data:post.thumbnailUrl'>
            <meta expr:content='data:post.thumbnailUrl' itemprop='image_url'/>
          </b:if>
          <meta expr:content='data:blog.blogId' itemprop='blogId'/>
          <meta expr:content='data:post.id' itemprop='postId'/>

          <a expr:name='data:post.id'/>
          <b:if cond='data:post.title'>
            <h3 class='post-title entry-title' itemprop='name'>
              <b:if cond='data:post.link'>
                <a expr:href='data:post.link'><data:post.title/></a>
              <b:elseif cond='data:post.url and data:blog.url != data:post.url'/>
                <a expr:href='data:post.url'><data:post.title/></a>
              <b:else/>
                <data:post.title/>
              </b:if>
            </h3>
          </b:if>

          <div class='post-header'>
            <div class='post-header-line-1'/>
          </div>

          <div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id' itemprop='articleBody'>
            <data:post.body/>
            <div style='clear: both;'/> <!-- clear for photos floats -->
          </div>

          <div class='post-footer'>
            <div class='post-footer-line post-footer-line-1'>
              <span class='post-author vcard'>
                <b:if cond='data:top.showAuthor'>
                  <b:if cond='data:post.authorProfileUrl'>
                    <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                      <meta expr:content='data:post.authorProfileUrl' itemprop='url'/>
                      <a expr:href='data:post.authorProfileUrl' rel='author' title='author profile'>
                        <span itemprop='name'><data:post.author/></span>
                      </a>
                    </span>
                  <b:else/>
                    <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                      <span itemprop='name'><data:post.author/></span>
                    </span>
                  </b:if>
                </b:if>
              </span>

              <span class='post-timestamp'>
                <b:if cond='data:top.showTimestamp'>
                  <data:top.timestampLabel/>
                  <b:if cond='data:post.url'>
                    <meta expr:content='data:post.url.canonical' itemprop='url'/>
                    <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'><abbr class='published' expr:title='data:post.timestampISO8601' itemprop='datePublished'><data:post.timestamp/></abbr></a>
                  </b:if>
                </b:if>
              </span>

              <span class='post-comment-link'>
                <b:include cond='data:blog.pageType not in {&quot;item&quot;,&quot;static_page&quot;}                                  and data:post.allowComments' data='post' name='comment_count_picker'/>
              </span>
            </div>

            <div class='post-footer-line post-footer-line-2'>
              <b:if cond='data:top.showMobileShare'>
                <div class='mobile-link-button goog-inline-block' id='mobile-share-button'>
                  <a href='javascript:void(0);'><data:shareMsg/></a>
                </div>
              </b:if>
            </div>

          </div>
        </div>

        <b:include cond='data:blog.pageType in {&quot;static_page&quot;,&quot;item&quot;}' data='post' name='comment_picker'/>
      </div>
    </div>
  </div>
</b:includable>
        <b:includable id='nextprev'>
  <div class='blog-pager' id='blog-pager'>
    <b:if cond='data:newerPageUrl'>
      <span id='blog-pager-newer-link'>
      <a class='blog-pager-newer-link' expr:href='data:newerPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-newer-link&quot;' expr:title='data:newerPageTitle'><data:newerPageTitle/></a>
      </span>
    </b:if>

    <b:if cond='data:olderPageUrl'>
      <span id='blog-pager-older-link'>
      <a class='blog-pager-older-link' expr:href='data:olderPageUrl' expr:id='data:widget.instanceId + &quot;_blog-pager-older-link&quot;' expr:title='data:olderPageTitle'><data:olderPageTitle/></a>
      </span>
    </b:if>

    <a class='home-link' expr:href='data:blog.homepageUrl'><data:homeMsg/></a>

    <b:if cond='data:mobileLinkUrl'>
      <div class='blog-mobile-link'>
        <a expr:href='data:mobileLinkUrl'><data:mobileLinkMsg/></a>
      </div>
    </b:if>

  </div>
  <div class='clear'/>
</b:includable>
        <b:includable id='post' var='post'>
  <div class='post hentry uncustomized-post-template' itemprop='blogPost' itemscope='itemscope' itemtype='http://schema.org/BlogPosting'>
    <b:if cond='data:post.firstImageUrl'>
      <meta expr:content='data:post.firstImageUrl' itemprop='image_url'/>
    </b:if>
    <meta expr:content='data:blog.blogId' itemprop='blogId'/>
    <meta expr:content='data:post.id' itemprop='postId'/>

    <a expr:name='data:post.id'/>
    <b:if cond='data:post.title'>
      <h3 class='post-title entry-title' itemprop='name'>
      <b:if cond='data:post.link or (data:post.url and data:blog.url != data:post.url)'>
        <a expr:href='data:post.link ? data:post.link : data:post.url'><data:post.title/></a>
      <b:else/>
        <data:post.title/>
      </b:if>
      </h3>
    </b:if>

    <div class='post-header'>
    <div class='post-header-line-1'/>
    </div>

    <!-- Then use the post body as the schema.org description, for good G+/FB snippeting. -->
    <div class='post-body entry-content' expr:id='&quot;post-body-&quot; + data:post.id' expr:itemprop='(data:blog.metaDescription ? &quot;&quot; : &quot;description &quot;) + &quot;articleBody&quot;'>
      <data:post.body/>
      <div style='clear: both;'/> <!-- clear for photos floats -->
    </div>

    <b:if cond='data:post.hasJumpLink'>
      <div class='jump-link'>
        <a expr:href='data:post.url + &quot;#more&quot;' expr:title='data:post.title'><data:post.jumpText/></a>
      </div>
    </b:if>

    <div class='post-footer'>
    <div class='post-footer-line post-footer-line-1'>
      <span class='post-author vcard'>
        <b:if cond='data:top.showAuthor'>
          <data:top.authorLabel/>
            <b:if cond='data:post.authorProfileUrl'>
              <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                <meta expr:content='data:post.authorProfileUrl' itemprop='url'/>
                <a class='g-profile' expr:href='data:post.authorProfileUrl' rel='author' title='author profile'>
                  <span itemprop='name'><data:post.author/></span>
                </a>
              </span>
            <b:else/>
              <span class='fn' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
                <span itemprop='name'><data:post.author/></span>
              </span>
            </b:if>
        </b:if>
      </span>

      <span class='post-timestamp'>
        <b:if cond='data:top.showTimestamp'>
          <data:top.timestampLabel/>
          <b:if cond='data:post.url'>
            <meta expr:content='data:post.url.canonical' itemprop='url'/>
            <a class='timestamp-link' expr:href='data:post.url' rel='bookmark' title='permanent link'><abbr class='published' expr:title='data:post.timestampISO8601' itemprop='datePublished'><data:post.timestamp/></abbr></a>
          </b:if>
        </b:if>
      </span>

      <span class='post-comment-link'>
        <b:include cond='data:blog.pageType not in {&quot;item&quot;,&quot;static_page&quot;}                          and data:post.allowComments' data='post' name='comment_count_picker'/>
      </span>

      <span class='post-icons'>
        <!-- email post links -->
        <b:if cond='data:post.emailPostUrl'>
          <span class='item-action'>
          <a expr:href='data:post.emailPostUrl' expr:title='data:top.emailPostMsg'>
            <img alt='' class='icon-action' height='13' src='https://resources.blogblog.com/img/icon18_email.gif' width='18'/>
          </a>
          </span>
        </b:if>

        <!-- quickedit pencil -->
        <b:include data='post' name='postQuickEdit'/>
      </span>

      <!-- share buttons -->
      <div class='post-share-buttons goog-inline-block'>
        <b:include cond='data:post.sharePostUrl' data='post' name='shareButtons'/>
      </div>

      </div>

      <div class='post-footer-line post-footer-line-2'>
      <span class='post-labels'>
        <b:if cond='data:top.showPostLabels and data:post.labels'>
          <data:postLabelsLabel/>
          <b:loop values='data:post.labels' var='label'>
            <a expr:href='data:label.url' rel='tag'><data:label.name/></a><b:if cond='not data:label.isLast'>,</b:if>
          </b:loop>
        </b:if>
      </span>
      </div>

      <div class='post-footer-line post-footer-line-3'>
      <span class='post-location'>
        <b:if cond='data:top.showLocation and data:post.location'>
          <data:postLocationLabel/>
          <a expr:href='data:post.location.mapsUrl' target='_blank'><data:post.location.name/></a>
        </b:if>
      </span>
      </div>
      <b:if cond='data:post.authorAboutMe'>
        <div class='author-profile' itemprop='author' itemscope='itemscope' itemtype='http://schema.org/Person'>
          <b:if cond='data:post.authorPhoto.url'>
            <img expr:src='data:post.authorPhoto.url' itemprop='image' width='50px'/>
          </b:if>
          <div>
            <a class='g-profile' expr:href='data:post.authorProfileUrl' itemprop='url' rel='author' title='author profile'>
              <span itemprop='name'><data:post.author/></span>
            </a>
          </div>
          <span itemprop='description'><data:post.authorAboutMe/></span>
        </div>
      </b:if>
    </div>
  </div>
</b:includable>
        <b:includable id='postQuickEdit' var='post'>
  <b:if cond='data:post.editUrl'>
    <span expr:class='&quot;item-control &quot; + data:post.adminClass'>
      <a expr:href='data:post.editUrl' expr:title='data:top.editPostMsg'>
        <img alt='' class='icon-action' height='18' src='https://resources.blogblog.com/img/icon18_edit_allbkg.gif' width='18'/>
      </a>
    </span>
  </b:if>
</b:includable>
        <b:includable id='shareButtons' var='post'>
  <b:if cond='data:top.showEmailButton'><a class='goog-inline-block share-button sb-email' expr:href='data:post.sharePostUrl + &quot;&amp;target=email&quot;' expr:title='data:top.emailThisMsg' target='_blank'><span class='share-button-link-text'><data:top.emailThisMsg/></span></a></b:if><b:if cond='data:top.showBlogThisButton'><a class='goog-inline-block share-button sb-blog' expr:href='data:post.sharePostUrl + &quot;&amp;target=blog&quot;' expr:onclick='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=270,width=475\&quot;); return false;&quot;' expr:title='data:top.blogThisMsg' target='_blank'><span class='share-button-link-text'><data:top.blogThisMsg/></span></a></b:if><b:if cond='data:top.showTwitterButton'><a class='goog-inline-block share-button sb-twitter' expr:href='data:post.sharePostUrl + &quot;&amp;target=twitter&quot;' expr:title='data:top.shareToTwitterMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToTwitterMsg/></span></a></b:if><b:if cond='data:top.showFacebookButton'><a class='goog-inline-block share-button sb-facebook' expr:href='data:post.sharePostUrl + &quot;&amp;target=facebook&quot;' expr:onclick='&quot;window.open(this.href, \&quot;_blank\&quot;, \&quot;height=430,width=640\&quot;); return false;&quot;' expr:title='data:top.shareToFacebookMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToFacebookMsg/></span></a></b:if><b:if cond='data:top.showPinterestButton'><a class='goog-inline-block share-button sb-pinterest' expr:href='data:post.sharePostUrl + &quot;&amp;target=pinterest&quot;' expr:title='data:top.shareToPinterestMsg' target='_blank'><span class='share-button-link-text'><data:top.shareToPinterestMsg/></span></a></b:if>
</b:includable>
        <b:includable id='status-message'>
  <b:if cond='data:navMessage'>
  <div class='status-msg-wrap'>
    <div class='status-msg-body'>
      <data:navMessage/>
    </div>
    <div class='status-msg-border'>
      <div class='status-msg-bg'>
        <div class='status-msg-hidden'><data:navMessage/></div>
      </div>
    </div>
  </div>
  <div style='clear: both;'/>
  </b:if>
</b:includable>
        <b:includable id='threaded-comment-form' var='post'>
  <div class='comment-form'>
    <a name='comment-form'/>
    <b:if cond='data:mobile'>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' style='display: none' width='100%'/>
    <b:else/>
      <p><data:blogCommentMessage/></p>
      <data:blogTeamBlogMessage/>
      <a expr:href='data:post.commentFormIframeSrc' id='comment-editor-src'/>
      <iframe allowtransparency='true' class='blogger-iframe-colorize blogger-comment-from-post' expr:height='data:cmtIframeInitialHeight' frameborder='0' id='comment-editor' name='comment-editor' src='' width='100%'/>
    </b:if>
    <data:post.cmtfpIframe/>
    <script type='text/javascript'>
      BLOG_CMT_createIframe(&#39;<data:post.appRpcRelayPath/>&#39;);
    </script>
  </div>
</b:includable>
        <b:includable id='threaded_comment_js' var='post'>
  <script async='async' expr:src='data:post.commentSrc' type='text/javascript'/>

  <script type='text/javascript'>
    (function() {
      var items = <data:post.commentJso/>;
      var msgs = <data:post.commentMsgs/>;
      var config = <data:post.commentConfig/>;

// <![CDATA[
      var cursor = null;
      if (items && items.length > 0) {
        cursor = parseInt(items[items.length - 1].timestamp) + 1;
      }

      var bodyFromEntry = function(entry) {
        var text = (entry &&
                    ((entry.content && entry.content.$t) ||
                     (entry.summary && entry.summary.$t))) ||
            '';
        if (entry && entry.gd$extendedProperty) {
          for (var k in entry.gd$extendedProperty) {
            if (entry.gd$extendedProperty[k].name == 'blogger.contentRemoved') {
              return '<span class="deleted-comment">' + text + '</span>';
            }
          }
        }
        return text;
      }

      var parse = function(data) {
        cursor = null;
        var comments = [];
        if (data && data.feed && data.feed.entry) {
          for (var i = 0, entry; entry = data.feed.entry[i]; i++) {
            var comment = {};
            // comment ID, parsed out of the original id format
            var id = /blog-(\d+).post-(\d+)/.exec(entry.id.$t);
            comment.id = id ? id[2] : null;
            comment.body = bodyFromEntry(entry);
            comment.timestamp = Date.parse(entry.published.$t) + '';
            if (entry.author && entry.author.constructor === Array) {
              var auth = entry.author[0];
              if (auth) {
                comment.author = {
                  name: (auth.name ? auth.name.$t : undefined),
                  profileUrl: (auth.uri ? auth.uri.$t : undefined),
                  avatarUrl: (auth.gd$image ? auth.gd$image.src : undefined)
                };
              }
            }
            if (entry.link) {
              if (entry.link[2]) {
                comment.link = comment.permalink = entry.link[2].href;
              }
              if (entry.link[3]) {
                var pid = /.*comments\/default\/(\d+)\?.*/.exec(entry.link[3].href);
                if (pid && pid[1]) {
                  comment.parentId = pid[1];
                }
              }
            }
            comment.deleteclass = 'item-control blog-admin';
            if (entry.gd$extendedProperty) {
              for (var k in entry.gd$extendedProperty) {
                if (entry.gd$extendedProperty[k].name == 'blogger.itemClass') {
                  comment.deleteclass += ' ' + entry.gd$extendedProperty[k].value;
                } else if (entry.gd$extendedProperty[k].name == 'blogger.displayTime') {
                  comment.displayTime = entry.gd$extendedProperty[k].value;
                }
              }
            }
            comments.push(comment);
          }
        }
        return comments;
      };

      var paginator = function(callback) {
        if (hasMore()) {
          var url = config.feed + '?alt=json&v=2&orderby=published&reverse=false&max-results=50';
          if (cursor) {
            url += '&published-min=' + new Date(cursor).toISOString();
          }
          window.bloggercomments = function(data) {
            var parsed = parse(data);
            cursor = parsed.length < 50 ? null
                : parseInt(parsed[parsed.length - 1].timestamp) + 1
            callback(parsed);
            window.bloggercomments = null;
          }
          url += '&callback=bloggercomments';
          var script = document.createElement('script');
          script.type = 'text/javascript';
          script.src = url;
          document.getElementsByTagName('head')[0].appendChild(script);
        }
      };
      var hasMore = function() {
        return !!cursor;
      };
      var getMeta = function(key, comment) {
        if ('iswriter' == key) {
          var matches = !!comment.author
              && comment.author.name == config.authorName
              && comment.author.profileUrl == config.authorUrl;
          return matches ? 'true' : '';
        } else if ('deletelink' == key) {
          return config.baseUri + '/comment/delete/'
               + config.blogId + '/' + comment.id;
        } else if ('deleteclass' == key) {
          return comment.deleteclass;
        }
        return '';
      };

      var replybox = null;
      var replyUrlParts = null;
      var replyParent = undefined;

      var onReply = function(commentId, domId) {
        if (replybox == null) {
          // lazily cache replybox, and adjust to suit this style:
          replybox = document.getElementById('comment-editor');
          if (replybox != null) {
            replybox.height = '250px';
            replybox.style.display = 'block';
            replyUrlParts = replybox.src.split('#');
          }
        }
        if (replybox && (commentId !== replyParent)) {
          replybox.src = '';
          document.getElementById(domId).insertBefore(replybox, null);
          replybox.src = replyUrlParts[0]
              + (commentId ? '&parentID=' + commentId : '')
              + '#' + replyUrlParts[1];
          replyParent = commentId;
        }
      };

      var hash = (window.location.hash || '#').substring(1);
      var startThread, targetComment;
      if (/^comment-form_/.test(hash)) {
        startThread = hash.substring('comment-form_'.length);
      } else if (/^c[0-9]+$/.test(hash)) {
        targetComment = hash.substring(1);
      }

      // Configure commenting API:
      var configJso = {
        'maxDepth': config.maxThreadDepth
      };
      var provider = {
        'id': config.postId,
        'data': items,
        'loadNext': paginator,
        'hasMore': hasMore,
        'getMeta': getMeta,
        'onReply': onReply,
        'rendered': true,
        'initComment': targetComment,
        'initReplyThread': startThread,
        'config': configJso,
        'messages': msgs
      };

      var render = function() {
        if (window.goog && window.goog.comments) {
          var holder = document.getElementById('comment-holder');
          window.goog.comments.render(holder, provider);
        }
      };

      // render now, or queue to render when library loads:
      if (window.goog && window.goog.comments) {
        render();
      } else {
        window.goog = window.goog || {};
        window.goog.comments = window.goog.comments || {};
        window.goog.comments.loadQueue = window.goog.comments.loadQueue || [];
        window.goog.comments.loadQueue.push(render);
      }
    })();
// ]]>
  </script>
</b:includable>
        <b:includable id='threaded_comments' var='post'>
  <div class='comments' id='comments'>
    <a name='comments'/>
    <h4><data:post.commentLabelFull/>:</h4>

    <div class='comments-content'>
      <b:include cond='data:post.embedCommentForm' data='post' name='threaded_comment_js'/>
      <div id='comment-holder'>
         <data:post.commentHtml/>
      </div>
    </div>

    <p class='comment-footer'>
      <b:if cond='data:post.allowNewComments'>
        <b:include data='post' name='threaded-comment-form'/>
      <b:else/>
        <data:post.noNewCommentsText/>
      </b:if>
    </p>

    <b:if cond='data:showCmtPopup'>
      <div id='comment-popup'>
        <iframe allowtransparency='true' frameborder='0' id='comment-actions' name='comment-actions' scrolling='no'>
        </iframe>
      </div>
    </b:if>

    <div id='backlinks-container'>
    <div expr:id='data:widget.instanceId + &quot;_backlinks-container&quot;'>
    </div>
    </div>
  </div>
</b:includable>
      </b:widget>
    </b:section>
  </div>
</div>

</main>

<!-- ============================================================
     ONE-TIME WELCOME POPUP
     ============================================================ -->
<div id='mlzs-popup-overlay' style='display:none'>
  <div id='mlzs-popup'>
    <button class='popup-close' id='mlzs-popup-close' title='Close'>
      <i class='fas fa-times'/>
    </button>
    <div class='popup-img-wrap'>
      <img alt='MLZS Student' loading='eager' src='https://images.pexels.com/photos/5212665/pexels-photo-5212665.jpeg?auto=compress&amp;cs=tinysrgb&amp;w=600'/>
      <div class='popup-img-overlay'/>
      <div class='popup-img-text'>
        <h3>Admissions Open<br/>2025-26</h3>
        <p>Nursery to Class 10 &#183; CBSE Affiliated</p>
      </div>
    </div>
    <div class='popup-body'>
      <div class='popup-school-badge'>
        <i class='fas fa-certificate'/> CBSE Affil. No. 330715
      </div>
      <h2>Welcome to<br/>Mount Litera Zee School</h2>
      <p>Bhagalpur&#39;s premier CBSE school, shaping thought leaders since 2015. Limited seats available for 2025-26.</p>
      <div class='popup-btns'>
        <a class='btn btn-primary' href='https://demowebschool.blogspot.com/p/admissions.html'>
          <i class='fas fa-graduation-cap'/> Apply Now
        </a>
        <a class='btn btn-outline' href='https://demowebschool.blogspot.com/p/contact.html' style='background:var(--navy);border-color:var(--navy);color:white;'>
          <i class='fas fa-phone'/> Contact Us
        </a>
      </div>
    </div>
  </div>
</div>

<!-- ============================================================
     FOOTER
     ============================================================ -->
<footer id='gps-footer'>
  <div class='footer-grid'>

    <!-- Brand -->
    <div class='footer-brand'>
      <div class='logo-wrap'>
        <div class='logo-icon'>
          <svg fill='none' viewBox='0 0 26 26' xmlns='http://www.w3.org/2000/svg'>
            <path d='M13 2L3 7v6c0 5.55 4.27 10.74 10 12 5.73-1.26 10-6.45 10-12V7L13 2z' fill='#F5A800'/>
            <path d='M10 13l2 2 4-4' stroke='#0D1B3E' stroke-linecap='round' stroke-linejoin='round' stroke-width='2'/>
          </svg>
        </div>
        <div class='logo-text'>
          <span class='school-name'><data:blog.title/></span>
          <span class='school-sub'>Est. 2015 &#183; CBSE Affiliated &#183; Bhagalpur</span>
        </div>
      </div>
      <p>Mount Litera Zee School, Bhagalpur, is managed by Balaji Education Trust and affiliated to CBSE (Affil. No. 330715). We offer co-ed, English medium education from Nursery to Class 10, shaping the next generation of thought leaders since 2015.</p>
      <div class='social-links'>
        <a class='social-link' href='https://facebook.com/mlzsbhagalpur' rel='noopener' target='_blank'><i class='fab fa-facebook-f'/></a>
        <a class='social-link' href='https://twitter.com/' rel='noopener' target='_blank'><i class='fab fa-x-twitter'/></a>
        <a class='social-link' href='https://instagram.com/' rel='noopener' target='_blank'><i class='fab fa-instagram'/></a>
        <a class='social-link' href='https://youtube.com/' rel='noopener' target='_blank'><i class='fab fa-youtube'/></a>
        <a class='social-link' href='https://wa.me/919031343411' rel='noopener' target='_blank'><i class='fab fa-whatsapp'/></a>
      </div>
    </div>

    <!-- Quick Links -->
    <div class='footer-col'>
      <h4>Quick Links</h4>
      <ul class='footer-links'>
        <li><a href='https://demowebschool.blogspot.com/'><i class='fas fa-chevron-right'/> Home</a></li>
        <li><a href='https://demowebschool.blogspot.com/p/about-us.html'><i class='fas fa-chevron-right'/> About Us</a></li>
        <li><a href='https://demowebschool.blogspot.com/search/label/Academics'><i class='fas fa-chevron-right'/> Academics</a></li>
        <li><a href='https://demowebschool.blogspot.com/p/admissions.html'><i class='fas fa-chevron-right'/> Admissions</a></li>
        <li><a href='https://demowebschool.blogspot.com/search/label/Gallery'><i class='fas fa-chevron-right'/> Gallery</a></li>
        <li><a href='https://demowebschool.blogspot.com/p/contact.html'><i class='fas fa-chevron-right'/> Contact Us</a></li>
        <li><a href='https://demowebschool.blogspot.com/p/careers.html'><i class='fas fa-chevron-right'/> Careers</a></li>
      </ul>
    </div>

    <!-- Academics -->
    <div class='footer-col'>
      <h4>Academics</h4>
      <ul class='footer-links'>
        <li><a href='https://demowebschool.blogspot.com/search/label/Primary'><i class='fas fa-chevron-right'/> Pre-Primary (Nursery&#8211;KG)</a></li>
        <li><a href='https://demowebschool.blogspot.com/search/label/Primary'><i class='fas fa-chevron-right'/> Primary School (I&#8211;V)</a></li>
        <li><a href='https://demowebschool.blogspot.com/search/label/Middle'><i class='fas fa-chevron-right'/> Middle School (VI&#8211;VIII)</a></li>
        <li><a href='https://demowebschool.blogspot.com/search/label/Secondary'><i class='fas fa-chevron-right'/> Secondary (IX&#8211;X)</a></li>
        <li><a href='https://demowebschool.blogspot.com/search/label/Sports'><i class='fas fa-chevron-right'/> Sports &amp; Activities</a></li>
        <li><a href='https://demowebschool.blogspot.com/search/label/Results'><i class='fas fa-chevron-right'/> Results &amp; Achievements</a></li>
      </ul>
    </div>

    <!-- Contact -->
    <div class='footer-col'>
      <h4>Get in Touch</h4>
      <div class='contact-item'>
        <i class='fas fa-map-marker-alt'/>
        <p>Jamni More, Near Khiribandh, Bhagalpur, Bihar &#8211; 812005, India</p>
      </div>
      <div class='contact-item'>
        <i class='fas fa-phone'/>
        <p>
          <a href='tel:+919031343411'>+91 90313 43411</a> /
          <a href='tel:+919031343422'> 43422</a>
        </p>
      </div>
      <div class='contact-item'>
        <i class='fas fa-envelope'/>
        <p><a href='mailto:mlzs.bhagalpur@mountlitera.com'>mlzs.bhagalpur@mountlitera.com</a></p>
      </div>
      <div class='contact-item'>
        <i class='fas fa-clock'/>
        <p>Mon &#8211; Sat: 8:00 AM &#8211; 4:00 PM</p>
      </div>
      <div class='contact-item'>
        <i class='fas fa-id-badge'/>
        <p>CBSE Affil. No.: <strong style='color:var(--gold-light)'>330715</strong></p>
      </div>
      <!-- Google Maps Embed &#8212; Bhagalpur, Bihar -->
      <div class='map-embed'>
        <iframe allowfullscreen='' loading='lazy' referrerpolicy='no-referrer-when-downgrade' src='https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3621.3!2d86.975!3d25.245!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x39f07d!2sBhagalpur!5e0!3m2!1sen!2sin!4v1700000000000!5m2!1sen!2sin' title='Mount Litera Zee School Bhagalpur Location'/>
      </div>
    </div>

  </div>

  <div class='footer-bottom'>
    <p>&#169; 2025 Mount Litera Zee School, Bhagalpur. All Rights Reserved.</p>
    <p>Managed by Balaji Education Trust &#183; <a href='https://demowebschool.blogspot.com/p/privacy-policy.html' rel='noopener' target='_blank'>Privacy Policy</a> &#183; <a href='https://demowebschool.blogspot.com/p/sitemap.html'>Sitemap</a></p>
  </div>
</footer>

<!-- ============================================================
     BOTTOM NAVIGATION (Mobile)
     ============================================================ -->
<nav class='bottom-nav'>
  <a class='bottom-nav-item active' href='https://demowebschool.blogspot.com/'>
    <i class='fas fa-house'/><span>Home</span>
  </a>
  <a class='bottom-nav-item' href='https://demowebschool.blogspot.com/p/about-us.html'>
    <i class='fas fa-school'/><span>About</span>
  </a>
  <a class='bottom-nav-item' href='https://demowebschool.blogspot.com/search/label/Academics'>
    <i class='fas fa-graduation-cap'/><span>Academics</span>
  </a>
  <a class='bottom-nav-item' href='https://demowebschool.blogspot.com/search/label/Gallery'>
    <i class='fas fa-images'/><span>Gallery</span>
  </a>
  <a class='bottom-nav-item' href='https://demowebschool.blogspot.com/p/contact.html'>
    <i class='fas fa-phone'/><span>Contact</span>
  </a>
</nav>

<!-- Scroll to Top -->
<div id='scrollTop' onclick='window.scrollTo({top:0,behavior:&quot;smooth&quot;})'>
  <i class='fas fa-arrow-up'/>
</div>

<!-- ============================================================
     JAVASCRIPT
     ============================================================ -->
<script>
//<![CDATA[

/* ---- Homepage Detection — hide page-content-area on homepage ---- */
(function() {
  var path = window.location.pathname;
  var isHome = (path === '/' || path === '/index.html' || path === '');
  if (isHome) {
    document.body.classList.add('is-homepage');
  }
})();

/* ---- Header Scroll Effect ---- */
var header = document.getElementById('gps-header');
window.addEventListener('scroll', function() {
  if (window.scrollY > 40) {
    header.classList.add('scrolled');
    document.getElementById('scrollTop').classList.add('show');
  } else {
    header.classList.remove('scrolled');
    document.getElementById('scrollTop').classList.remove('show');
  }
}, {passive: true});

/* ---- Mobile Menu Toggle ---- */
function toggleMenu() {
  var menu = document.getElementById('mobileMenu');
  var ham  = document.getElementById('hamburger');
  var open = menu.classList.toggle('open');
  ham.classList.toggle('open', open);
  document.body.style.overflow = open ? 'hidden' : '';
}

/* ---- Close menu on backdrop click ---- */
document.getElementById('mobileMenu').addEventListener('click', function(e) {
  if (e.target === this) toggleMenu();
});

/* ---- Intersection Observer for animations ---- */
function observeAnimations() {
  var items = document.querySelectorAll('.animate-in');
  if ('IntersectionObserver' in window) {
    var io = new IntersectionObserver(function(entries) {
      entries.forEach(function(entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
          io.unobserve(entry.target);
        }
      });
    }, { threshold: 0.1, rootMargin: '0px 0px -40px 0px' });
    items.forEach(function(el) { io.observe(el); });
  } else {
    items.forEach(function(el) { el.classList.add('visible'); });
  }
}
observeAnimations();

/* ---- Counter Animation ---- */
function animateCounters() {
  var counters = document.querySelectorAll('.stat-number[data-target]');
  var observed = false;
  var io2 = new IntersectionObserver(function(entries) {
    entries.forEach(function(entry) {
      if (entry.isIntersecting && !observed) {
        observed = true;
        counters.forEach(function(el) {
          var target = parseInt(el.dataset.target);
          var suffix = target >= 1000 ? '+' : '+';
          var duration = 1600;
          var step = Math.ceil(target / (duration / 16));
          var current = 0;
          var timer = setInterval(function() {
            current = Math.min(current + step, target);
            el.textContent = current.toLocaleString() + suffix;
            if (current >= target) clearInterval(timer);
          }, 16);
        });
      }
    });
  }, { threshold: 0.3 });
  var statsSection = document.getElementById('gps-stats');
  if (statsSection) io2.observe(statsSection);
}
animateCounters();

/* ---- Testimonials Slider ---- */
(function() {
  var track  = document.getElementById('testiTrack');
  var dotsEl = document.getElementById('testiDots');
  if (!track) return;

  var cards      = track.querySelectorAll('.testi-card');
  var total      = cards.length;
  var current    = 0;
  var autoTimer;

  // Responsive cards per view
  function perView() {
    if (window.innerWidth >= 1000) return 3;
    if (window.innerWidth >= 700)  return 2;
    return 1;
  }

  // Build dots
  function buildDots() {
    dotsEl.innerHTML = '';
    var pages = Math.ceil(total / perView());
    for (var i = 0; i < pages; i++) {
      var d = document.createElement('span');
      d.className = 'testi-dot' + (i === 0 ? ' active' : '');
      (function(idx) { d.onclick = function() { goTo(idx); }; })(i);
      dotsEl.appendChild(d);
    }
  }

  function updateDots() {
    var page = Math.floor(current / perView());
    var dots = dotsEl.querySelectorAll('.testi-dot');
    dots.forEach(function(d, i) { d.classList.toggle('active', i === page); });
  }

  function goTo(page) {
    var pv   = perView();
    current  = Math.max(0, Math.min(page * pv, total - pv));
    var cardW = track.parentElement.offsetWidth;
    var gap   = 20;
    var offset = current * (cardW / pv + gap / pv);
    track.style.transform = 'translateX(-' + offset + 'px)';
    updateDots();
    resetAuto();
  }

  function next() {
    var pv   = perView();
    var page = Math.floor(current / pv);
    var maxP = Math.ceil(total / pv) - 1;
    goTo(page >= maxP ? 0 : page + 1);
  }
  function prev() {
    var pv   = perView();
    var page = Math.floor(current / pv);
    var maxP = Math.ceil(total / pv) - 1;
    goTo(page <= 0 ? maxP : page - 1);
  }

  function resetAuto() {
    clearInterval(autoTimer);
    autoTimer = setInterval(next, 5000);
  }

  document.getElementById('testiNext').onclick = next;
  document.getElementById('testiPrev').onclick = prev;

  buildDots();
  resetAuto();
  window.addEventListener('resize', function() { buildDots(); goTo(0); });

  // Touch swipe
  var touchStart = 0;
  track.addEventListener('touchstart', function(e) { touchStart = e.touches[0].clientX; }, {passive:true});
  track.addEventListener('touchend', function(e) {
    var diff = touchStart - e.changedTouches[0].clientX;
    if (Math.abs(diff) > 50) { if (diff > 0) next(); else prev(); }
  }, {passive:true});
})();

/* ---- Active bottom nav ---- */
(function() {
  var path   = window.location.pathname;
  var navBtns = document.querySelectorAll('.bottom-nav-item');
  navBtns.forEach(function(a) {
    if (a.getAttribute('href') === path ||
        (path !== '/' && a.getAttribute('href') !== '/' && path.indexOf(a.getAttribute('href')) > -1)) {
      navBtns.forEach(function(b) { b.classList.remove('active'); });
      a.classList.add('active');
    }
  });
})();

/* ---- Mobile Accordion (mobile menu dropdowns) ---- */
function toggleAcc(btn) {
  var body = btn.nextElementSibling;
  var isOpen = body.classList.contains('open');
  document.querySelectorAll('.mobile-acc-body.open').forEach(function(b) {
    b.classList.remove('open');
    b.previousElementSibling.classList.remove('open');
  });
  if (!isOpen) {
    body.classList.add('open');
    btn.classList.add('open');
  }
}

/* ---- One-Time Welcome Popup ---- */
(function() {
  var isHomepage = (window.location.pathname === '/'
    || window.location.href.replace(/https?:\/\/[^\/]+/, '') === '/');
  if (!isHomepage) return;
  try {
    if (localStorage.getItem('mlzs_popup_seen')) return;
  } catch(e) {}
  var overlay = document.getElementById('mlzs-popup-overlay');
  if (!overlay) return;
  setTimeout(function() {
    overlay.style.display = 'flex';
    document.body.style.overflow = 'hidden';
  }, 1000);
  function closePopup() {
    overlay.style.opacity = '0';
    overlay.style.transition = 'opacity 0.3s ease';
    setTimeout(function() {
      overlay.style.display = 'none';
      document.body.style.overflow = '';
    }, 300);
    try { localStorage.setItem('mlzs_popup_seen', '1'); } catch(e) {}
  }
  var closeBtn = document.getElementById('mlzs-popup-close');
  if (closeBtn) closeBtn.onclick = closePopup;
  overlay.addEventListener('click', function(e) {
    if (e.target === overlay) closePopup();
  });
  document.addEventListener('keydown', function(e) {
    if (e.key === 'Escape') closePopup();
  });
})();

//]]>
</script>

<!-- ============================================================
     BLOGGER XML REQUIRED SECTIONS
     ============================================================ -->
<b:include data='blog' name='all-head-content'/>

</body>
</html>
