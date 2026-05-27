# BAHLAPING MASH 2.0 | QUICK REFERENCE & IMPLEMENTATION GUIDE

## 🚀 START HERE: 5-MINUTE OVERVIEW

### What We're Doing
Converting `bahlapingmash.com` from **WordPress → Modern HTML5 Template**  
Using the **Axima Factory/Manufacturing Template** from Envato

### Why
- 🚀 10x faster (2.5s vs 5s+ page load)
- 💰 85% cheaper over 5 years
- 🎨 Modern, professional design
- 📱 Better mobile experience
- 🔒 More secure (no database)
- ✨ Full customization control

### Timeline
**4 weeks to launch** (25-30 days)

---

## 📁 FOLDER STRUCTURE REFERENCE

```
BahlapingWeb/
└── axima/                          # ← Main template folder
    ├── index.html                  # ← HOME PAGE
    ├── about-us.html               # ← ABOUT COMPANY
    ├── why-us.html                 # ← VALUE PROPOSITION
    ├── leadership-team.html        # ← TEAM/SHARON
    ├── Industries-industry-served.html  # ← SERVICES (3 main)
    ├── industries-single-industry.html  # ← SERVICE DETAIL
    ├── case-studies-grid.html      # ← PORTFOLIO
    ├── case-studies-single.html    # ← PROJECT DETAIL
    ├── news.html                   # ← NEWS/BLOG
    ├── news-single-post.html       # ← ARTICLE DETAIL
    ├── request-quote.html          # ← QUOTE REQUEST
    ├── contacs.html                # ← CONTACT PAGE
    │
    ├── assets/
    │   ├── css/
    │   │   ├── libraries.css       # Bootstrap, FontAwesome, etc.
    │   │   └── style.css           # COMPILED from SCSS
    │   │
    │   ├── scss/                   # SOURCE STYLESHEETS (Edit these!)
    │   │   ├── global/
    │   │   │   ├── _vars.scss      # ← COLOR/FONT VARIABLES
    │   │   │   ├── _mixins.scss
    │   │   │   └── _global.scss
    │   │   ├── layout/
    │   │   ├── module/
    │   │   └── style.scss          # Main import file
    │   │
    │   ├── js/
    │   │   ├── jquery-3.3.1.min.js # jQuery library
    │   │   ├── plugins.js          # Bootstrap, Owl, Waypoints, etc.
    │   │   └── main.js             # ← CUSTOM JAVASCRIPT
    │   │
    │   └── images/
    │       ├── logo/               # Logos
    │       ├── banners/            # Hero images
    │       ├── services/           # Service icons
    │       ├── team/               # Team member photos
    │       ├── clients/            # Client logos
    │       └── [other folders]
    │
    └── Documentation/              # Template documentation
```

---

## 🎨 KEY FILES TO CUSTOMIZE

### 1. COLORS & VARIABLES
**File:** `assets/scss/global/_vars.scss`
```scss
// Current values (all confirmed ✅)
$color-theme: #ff5e14;      // Orange (Primary)
$color-heading: #0b2653;    // Dark Blue (Headings)
$color-body: #51668a;       // Gray (Body text)
$color-white: #ffffff;      // White (Backgrounds)
$color-gray: #f9f9f9;       // Light gray (Alt backgrounds)

// To modify: Just change the hex codes
// Recompile SCSS → CSS and all pages update!
```

### 2. FONTS
**File:** Same `_vars.scss`
```scss
$font-heading: 'Rajdhani', sans-serif;
$font-body: 'Heebo', sans-serif;
$body-font-size: 15px;
```

**Already linked in HTML head:**
```html
<link rel="stylesheet" 
  href="https://fonts.googleapis.com/css?family=Heebo:400,500,700%7cRajdhani:400,500,600,700&display=swap">
```

### 3. MAIN STYLESHEET COMPILATION
**File:** `assets/scss/style.scss`
```scss
// This file IMPORTS all other SCSS files
// Order matters! Top-level is imported first

@import "global/vars";        // Colors, fonts
@import "global/mixins";      // Helper functions
@import "global/global";      // Base styles

@import "layout/helpers";     // Utility classes
@import "layout/typography";  // Text styles
@import "layout/buttons";     // Button styles
// ... more imports ...
```

**HOW TO COMPILE:**
Option 1 (Manual):
```bash
sass --watch assets/scss:assets/css
```

Option 2 (VS Code Extension):
- Install "Live Sass Compiler"
- Click "Watch Sass" in status bar
- CSS auto-compiles on save

### 4. CUSTOM JAVASCRIPT
**File:** `assets/js/main.js`
```javascript
$(function () {
    "use strict";
    
    // Global variables
    var $win = $(window);
    
    // Mobile Menu
    var $navToggler = $('.navbar-toggler');
    $navToggler.on('click', function () {
        // Mobile menu toggle logic
    });
    
    // Sticky Navbar
    $win.on('scroll', function () {
        // Sticky nav logic
    });
    
    // ... more functionality ...
});
```

---

## 📝 CONTENT BLOCKS TO CUSTOMIZE

### Block 1: HEADER/NAVBAR
**File:** `index.html` (lines 20-60)
```html
<!-- Promo text banner at very top -->
<div class="header__promo-text text-center">
    <strong>Need Help:</strong>
    <span>Providing Innovative Mining & Engineering Solutions, Call +27 60 877 5153</span>
</div>

<!-- Navigation menu -->
<nav class="navbar">
    <!-- Logo, menu items, etc. -->
</nav>
```

**To Change:**
- Update phone number
- Change tagline
- Add/remove menu items

### Block 2: HERO SECTION
**File:** `index.html` (around line 100+)
```html
<section class="hero" style="background-image: url('assets/images/banners/mining-ops.jpg')">
    <h1>Innovative Mining & Engineering Solutions</h1>
    <p>BBBEE Level 1 | Trusted by Industry Leaders</p>
    <a href="#services" class="btn btn-primary">Explore Services</a>
</section>
```

**To Change:**
- Update background image
- Change headline
- Update CTA button text/links

### Block 3: SERVICES SHOWCASE
**File:** `Industries-industry-served.html`
```html
<!-- 3 Service cards displayed in grid -->
<div class="services-grid">
    <!-- Card 1: Cable Pit -->
    <div class="service-card">
        <img src="icon-electrical.png" alt="Cable Pit">
        <h3>Cable Pit Reticulation</h3>
        <p>4-shift continuous service on 6.6KV electrical networks...</p>
        <a href="#" class="btn">Learn More</a>
    </div>
    
    <!-- Card 2: Chrome Export -->
    <div class="service-card">
        <!-- Similar structure -->
    </div>
    
    <!-- Card 3: Civil & Construction -->
    <div class="service-card">
        <!-- Similar structure -->
    </div>
</div>
```

### Block 4: CONTACT SECTION
**File:** `contacs.html`
```html
<section class="contact">
    <h2>Get In Touch</h2>
    
    <!-- Contact Info -->
    <div class="contact-info">
        <p><strong>Address:</strong> House 060175, Ga-chaba village, Mapela 0610</p>
        <p><strong>Phone:</strong> <a href="tel:+27608775153">+27 60 877 5153</a></p>
        <p><strong>Email:</strong> <a href="mailto:Sharon@bahlapingmash.com">Sharon@bahlapingmash.com</a></p>
        <p><strong>Hours:</strong> Mon-Fri 8:00 AM - 5:00 PM</p>
    </div>
    
    <!-- Contact Form -->
    <form class="contact-form">
        <input type="text" placeholder="Your Name">
        <input type="email" placeholder="Your Email">
        <textarea placeholder="Your Message"></textarea>
        <button type="submit">Send Message</button>
    </form>
    
    <!-- Google Map -->
    <div class="google-map" id="googleMap"></div>
</section>
```

### Block 5: FOOTER
**File:** All pages (bottom)
```html
<footer class="footer">
    <div class="footer-content">
        <!-- Company info -->
        <h3>Bahlaping Mash</h3>
        <p>Innovative mining & engineering solutions across Southern Africa</p>
        
        <!-- Certifications -->
        <ul>
            <li>✓ BBBEE Level 1</li>
            <li>✓ CIDB Registered (GR 7 GB/CE)</li>
            <li>✓ SANS 1393:2023 Accredited</li>
            <li>✓ VAT Registered</li>
        </ul>
        
        <!-- Links -->
        <nav>
            <a href="index.html">Home</a>
            <a href="about-us.html">About</a>
            <a href="Industries-industry-served.html">Services</a>
            <a href="contacs.html">Contact</a>
        </nav>
        
        <!-- Social -->
        <div class="social-links">
            <a href="#facebook">f</a>
            <a href="#twitter">𝕏</a>
            <a href="#instagram">📷</a>
            <a href="#linkedin">in</a>
        </div>
        
        <!-- Copyright -->
        <p>&copy; 2026 Bahlaping Mash. All Rights Reserved.</p>
    </div>
</footer>
```

---

## 🖼️ IMAGE OPTIMIZATION GUIDE

### Required Images

#### 1. LOGO FILES
**Location:** `assets/images/logo/`
```
├── logo-light.png       (Use on dark backgrounds)
├── logo-dark.png        (Use on light backgrounds)
└── favicon.png          (Browser tab icon, 32x32px)
```

#### 2. HERO/BANNER IMAGES
**Location:** `assets/images/banners/`
```
├── home-hero.jpg        (1920x600px, mining operations)
├── about-banner.jpg     (1920x600px)
└── services-banner.jpg  (1920x600px)

Specs:
- Size: 1920px wide minimum
- Format: JPG (compressed) or WebP
- Optimization: 100-200KB each (compressed)
```

#### 3. SERVICE ICONS
**Location:** `assets/images/icons/` or `assets/images/services/`
```
├── electrical.svg       (Cable Pit)
├── mining.svg           (Chrome Export)
├── construction.svg     (Civil & Construction)
└── [other service icons]

Specs:
- Format: SVG (scalable)
- Size: 64x64px or larger (SVG scales)
- Style: Consistent with brand
```

#### 4. TEAM PHOTOS
**Location:** `assets/images/team/`
```
├── sharon-mashishi.jpg  (Founder - main)
├── team-member-1.jpg
├── team-member-2.jpg
└── team-member-3.jpg

Specs:
- Size: 400x400px minimum (square)
- Format: JPG
- Optimization: 50-100KB each
- Style: Professional headshots
```

#### 5. CLIENT/COMPANY LOGOS
**Location:** `assets/images/clients/`
```
├── client-1.png
├── client-2.png
└── [partner logos]

Specs:
- Format: PNG with transparency
- Size: 200x200px or larger
- Remove background (transparent)
```

### IMAGE OPTIMIZATION BEST PRACTICES

1. **Compression:**
   - Use TinyPNG, ImageOptim, or Squoosh
   - Reduce file size 50-70%
   - Keep quality high

2. **Format Selection:**
   - Photos → JPG (80-85% quality)
   - Icons → SVG or PNG
   - Backgrounds → JPG or WebP
   - Logos → PNG with transparency

3. **Responsive Sizing:**
   - Create 2x versions for Retina displays
   - Use srcset for different screen sizes
   - Lazy load images below fold

4. **Naming Convention:**
   ```
   Good:     service-icon-electrical.svg
   Bad:      icon123.png
   
   Good:     team-sharon-founder.jpg
   Bad:      photo.jpg
   ```

---

## 🔧 COMMON MODIFICATIONS

### Change Navigation Menu
**File:** All HTML files (in navbar section)
```html
<ul class="navbar-nav mx-auto">
    <li class="nav__item">
        <a href="index.html">Home</a>
    </li>
    <li class="nav__item with-dropdown">
        <a href="about-us.html">Company</a>
        <ul class="dropdown-menu">
            <li><a href="about-us.html">About Us</a></li>
            <li><a href="leadership-team.html">Team</a></li>
            <li><a href="why-us.html">Why Us</a></li>
        </ul>
    </li>
    <!-- Add more items as needed -->
</ul>
```

### Change Button Colors
**File:** `assets/scss/layout/_buttons.scss`
```scss
.btn-primary {
    background-color: $color-theme;    // Uses #ff5e14
    color: $color-white;
    border: none;
    padding: 12px 30px;
    
    &:hover {
        background-color: darken($color-theme, 10%);
    }
}
```

### Add New Section
**File:** Any HTML page
```html
<!-- New section template -->
<section id="newsection" class="new-section pt-100 pb-100">
    <div class="container">
        <h2>Section Title</h2>
        <p>Content here</p>
    </div>
</section>
```

### Change Spacing
**File:** Apply classes to any element
```html
<!-- Padding/Margin classes -->
<div class="pt-100 pb-100 mt-50 mb-30">
    <!-- pt = padding-top, pb = padding-bottom -->
    <!-- mt = margin-top, mb = margin-bottom -->
    <!-- Numbers: 10, 20, 30, 40, 50, 60, 70, 80, 90, 100, 110, 120, etc. -->
</div>
```

---

## ✅ LAUNCH CHECKLIST

### WEEK 1: Setup ✅
- [ ] SCSS compilation configured
- [ ] Color variables finalized
- [ ] Asset directories organized
- [ ] Images collected & optimized
- [ ] Contact form backend ready

### WEEK 2: Content 📝
- [ ] index.html populated
- [ ] about-us.html complete
- [ ] Services page complete
- [ ] Team page complete (Sharon featured)
- [ ] Contact page complete

### WEEK 3: Features 🎯
- [ ] Forms tested & working
- [ ] Portfolio/case studies added
- [ ] Blog section setup
- [ ] SEO meta tags added
- [ ] Analytics tracking code installed

### WEEK 4: Testing 🧪
- [ ] Mobile responsiveness verified
- [ ] All links tested (internal & external)
- [ ] Forms tested end-to-end
- [ ] Performance tested (Lighthouse 90+)
- [ ] Security scan passed
- [ ] Cross-browser testing done

### LAUNCH 🚀
- [ ] Domain redirects configured
- [ ] SSL certificate installed
- [ ] Backups created
- [ ] Monitoring enabled
- [ ] Analytics verified
- [ ] Search Console submitted

---

## 💡 QUICK HELP

### Common Issues & Solutions

**Q: Page not showing changes after editing CSS?**
- A: SCSS not recompiled. Click "Watch Sass" or run `sass --watch`

**Q: Images not loading?**
- A: Check file path. Use `assets/images/filename.jpg` from HTML root

**Q: Mobile menu not working?**
- A: Check `main.js` is loading. Open browser console for errors

**Q: Performance slow?**
- A: Check image sizes. Use TinyPNG to compress.

**Q: Layout broken on mobile?**
- A: Add `class="container"` wrapper, use Bootstrap grid classes

---

## 📞 SUPPORT RESOURCES

- **Template Docs:** `/Documentation/index.html`
- **Bootstrap Docs:** https://getbootstrap.com/docs/4.3/
- **SCSS Guide:** https://sass-lang.com/guide
- **Image Optimization:** https://tinypng.com or https://squoosh.app
- **Lighthouse Testing:** Chrome DevTools → Lighthouse

---

## 🎉 YOU'RE READY!

**Next Step:** Start Phase 1 Implementation  
**Timeline:** Week 1 - Setup & Configuration  
**Questions:** Review the `MODERNIZATION_GAMEPLAN_v2.0.md` document

---

*Quick Reference v1.0 | May 27, 2026*
