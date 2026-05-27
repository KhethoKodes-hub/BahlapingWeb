# BAHLAPING MASH 2.0 | EXECUTION STATUS & PRIORITY CHECKLIST
**Status Date:** May 27, 2026  
**Project Phase:** Phase 1 - Foundation & Setup  
**Timeline:** 4 Weeks to Launch

---

## 📊 PROJECT OVERVIEW

### ✅ COMPLETED
- [x] Strategic planning (4 documentation files)
- [x] Template selection & analysis (Axima verified)
- [x] Current site audit (https://bahlapingmash.com analyzed)
- [x] Content mapping (All pages documented)
- [x] Brand strategy (Colors confirmed)
- [x] Information architecture (Navigation finalized)

### 🚀 IN PROGRESS
- [ ] Phase 1: Foundation Setup (This week)
- [ ] Asset preparation
- [ ] Development environment configuration

### ⏳ PENDING
- [ ] Phase 2: Content Integration (Week 2)
- [ ] Phase 3: Features & Optimization (Week 3)
- [ ] Phase 4: Testing & Launch (Week 4)

---

## 📋 PRIORITY CHECKLIST: PHASE 1 (Week 1)

### 1️⃣ SCSS/CSS VARIABLES
- [ ] Open: `axima/assets/scss/global/_vars.scss`
- [ ] Verify color variables:
  - [ ] Primary Orange: `#ff5e14`
  - [ ] Dark Blue: `#0b2653`
  - [ ] Body Text: `#51668a`
  - [ ] White: `#ffffff`
- [ ] Verify font variables:
  - [ ] Primary font (verify weight/family)
  - [ ] Secondary font (headers)
- [ ] Test SCSS compilation
- [ ] Verify output in CSS

### 2️⃣ ASSET DIRECTORY STRUCTURE
**Create folders for:**
```
axima/assets/images/
├── about/
│   ├── company-operations.jpg
│   ├── sharon-headshot.jpg
│   └── team-photo.jpg
├── banners/
│   └── hero-mining.jpg
├── logos/
│   ├── logo-light.png
│   └── logo-dark.png
├── services/
│   ├── cable-pit.jpg
│   ├── chrome-export.jpg
│   └── civil-construction.jpg
├── portfolio/
│   ├── project-1.jpg
│   ├── project-2.jpg
│   ├── project-3.jpg
│   └── project-4.jpg
└── testimonials/
    └── thumbs/
        ├── client-1.jpg
        ├── client-2.jpg
        └── client-3.jpg
```

### 3️⃣ LOGO PREPARATION
**Required files:**
- [ ] `logo-light.png` (300x100px) - Header light version
- [ ] `logo-dark.png` (300x100px) - Header dark version
- [ ] `logo-footer.png` (250x80px) - Footer version
- [ ] `favicon.ico` (32x32px)
- [ ] Place in: `axima/assets/images/logo/`

**Current placeholder in template:**
- `assets/images/logo/logo-light.png` ← REPLACE
- `assets/images/logo/logo-dark.png` ← REPLACE
- `assets/images/logo/logo-footer.png` ← REPLACE

### 4️⃣ IMAGE REQUIREMENTS FROM CLIENT (⏳ PENDING)

#### A. Hero/Operations Images
- [ ] Mining operations wide shot (1200x600px min, JPG)
- [ ] Cable pit reticulation work photo (1200x600px, JPG)
- [ ] Construction project image (1200x600px, JPG)

#### B. Team Photos
- [ ] Sharon Mashishi professional headshot (400x400px min, JPG)
- [ ] Founder signature image (200x100px PNG/JPG)

#### C. Service Icons
- [ ] Cable pit icon (200x200px, PNG transparent)
- [ ] Chrome export icon (200x200px, PNG transparent)
- [ ] Civil & construction icon (200x200px, PNG transparent)

#### D. Portfolio/Gallery
- [ ] Project 1 image (800x600px, JPG)
- [ ] Project 2 image (800x600px, JPG)
- [ ] Project 3 image (800x600px, JPG)
- [ ] Project 4-6 images (optional for v1)

#### E. Company Assets
- [ ] About page company photo (1000x600px, JPG)
- [ ] Client/partner logos (PNG, 200x100px each)

### 5️⃣ DEVELOPMENT ENVIRONMENT
- [ ] Verify Node.js installed
- [ ] Verify npm installed
- [ ] Install SCSS compiler if needed: `npm install -g sass`
- [ ] Test SCSS compilation on existing styles
- [ ] Set up watch mode for development

**Command to compile SCSS:**
```bash
cd axima/assets/scss
sass --watch . ../css
```

### 6️⃣ FILE STRUCTURE VERIFICATION
**Verify all key files exist:**
- [ ] `axima/index.html` (Already populated with Bahlaping content)
- [ ] `axima/about-us.html` (Ready)
- [ ] `axima/Industries-industry-served.html` (Ready)
- [ ] `axima/leadership-team.html` (Ready)
- [ ] `axima/contacs.html` (Ready)
- [ ] `axima/assets/css/style.css` (Main stylesheet)
- [ ] `axima/assets/scss/style.scss` (SCSS source)
- [ ] `axima/assets/js/main.js` (jQuery logic)

### 7️⃣ CONTENT VERIFICATION
**Verify embedded content in HTML files:**

**index.html:**
- [ ] Hero title: "Turning Your Vision Into Tangible Results!"
- [ ] Hero subtitle: "9+ Years of Excellence..."
- [ ] 3 service cards present
- [ ] Company credentials in footer
- [ ] Contact info correct: +27 60 877 5153

**about-us.html:**
- [ ] "Founded 2016" present
- [ ] "BBBEE Level 1" prominent
- [ ] Sharon Mashishi name present
- [ ] Mission & vision statements
- [ ] 5 certifications listed

**Industries-industry-served.html:**
- [ ] 3 service sections:
  - Cable Pit Reticulation
  - Export/Import Chrome
  - Civil & Construction
- [ ] Service descriptions accurate

**leadership-team.html:**
- [ ] Sharon Mashishi featured
- [ ] Contact info: sharon.mashishi@bahlapingmash.com
- [ ] Phone: +27 60 877 5153

**contacs.html:**
- [ ] Address: House 060175, Ga-chaba village, Mapela 0610
- [ ] Phone: +27 60 877 5153
- [ ] Email: Sharon@bahlapingmash.com
- [ ] Hours: Mon-Fri 8:00-17:00
- [ ] Contact form present

### 8️⃣ FOOTER CONTENT CHECK (All Pages)
- [ ] Company description: "Innovative mining & engineering solutions..."
- [ ] Certifications block:
  - ✓ BBBEE Level 1
  - ✓ CIDB Registered
  - ✓ SANS 1393:2023 Accredited
  - ✓ VAT Registered
- [ ] Social media links:
  - Facebook
  - Twitter
  - Instagram
  - LinkedIn
- [ ] Quick navigation links
- [ ] Copyright year updated to 2025

---

## 📋 PRIORITY CHECKLIST: PHASE 2 (Week 2)

### IMAGE INTEGRATION
- [ ] Add hero image to index.html slider
- [ ] Add company operations image to about-us.html
- [ ] Add service images to Industries-industry-served.html
- [ ] Add Sharon's photo to leadership-team.html
- [ ] Optimize all images (WebP format + fallbacks)
- [ ] Test lazy loading on mobile

### FORM SETUP
- [ ] Verify contact form HTML in contacs.html
- [ ] Set up form backend (PHP/Node/Alternative)
- [ ] Test form submission
- [ ] Set up email notifications to: Sharon@bahlapingmash.com
- [ ] Add success/error messages

### NAVIGATION TESTING
- [ ] Test all internal links
- [ ] Verify dropdown menus work
- [ ] Test mobile navigation toggle
- [ ] Verify breadcrumbs (if applicable)
- [ ] Check 404 error page

### MOBILE RESPONSIVENESS
- [ ] Test on iPhone 12 Pro
- [ ] Test on iPhone 14 Pro Max
- [ ] Test on iPad
- [ ] Test on Android (Chrome)
- [ ] Verify Bootstrap breakpoints work
- [ ] Check touch-friendly button sizes

---

## 📋 PRIORITY CHECKLIST: PHASE 3 (Week 3)

### FEATURES & ENHANCEMENTS
- [ ] Portfolio/Case Studies section
- [ ] Blog/News section setup
- [ ] Request Quote form
- [ ] Testimonials/Social proof section
- [ ] Search functionality (if needed)
- [ ] Comment system (if blog enabled)

### PERFORMANCE OPTIMIZATION
- [ ] Image optimization (compression + WebP)
- [ ] CSS minification & critical CSS
- [ ] JavaScript minification
- [ ] Lazy loading implementation
- [ ] Font optimization (subset fonts)
- [ ] Remove unused CSS/JS

### SEO OPTIMIZATION
- [ ] Meta tags on all pages
- [ ] Schema.org structured data
- [ ] Open Graph tags
- [ ] XML sitemap generation
- [ ] robots.txt setup
- [ ] Canonical tags

### ACCESSIBILITY (WCAG 2.1 AA)
- [ ] Color contrast verification
- [ ] Alt text on all images
- [ ] ARIA labels on interactive elements
- [ ] Keyboard navigation testing
- [ ] Screen reader testing (NVDA/JAWS)
- [ ] Form label associations

---

## 📋 PRIORITY CHECKLIST: PHASE 4 (Week 4)

### TESTING
- [ ] Lighthouse audit (Target: 90+)
- [ ] Cross-browser testing (Chrome, Firefox, Safari, Edge)
- [ ] Mobile responsiveness audit
- [ ] Accessibility audit (WCAG AA)
- [ ] Performance audit (<3s load time)
- [ ] Security scan (OWASP)

### DEPLOYMENT PREPARATION
- [ ] Domain setup (bahlapingmash.com)
- [ ] SSL certificate (Let's Encrypt)
- [ ] Hosting configuration
- [ ] Database setup (if needed)
- [ ] Email configuration
- [ ] DNS configuration

### ANALYTICS & MONITORING
- [ ] Google Analytics setup
- [ ] Google Search Console verification
- [ ] Hotjar/Heatmap setup (optional)
- [ ] Error tracking (Sentry/similar)
- [ ] Uptime monitoring
- [ ] Performance monitoring

### LAUNCH PREPARATION
- [ ] Final content review with Sharon
- [ ] Client sign-off on all pages
- [ ] Backup strategy finalized
- [ ] Rollback plan documented
- [ ] Launch timeline confirmed
- [ ] Support documentation prepared

### LAUNCH & POST-LAUNCH
- [ ] Deploy to production
- [ ] Test all functionality on live site
- [ ] Redirect WordPress site (301s)
- [ ] Monitor for errors (first 24 hours)
- [ ] Verify email delivery
- [ ] Confirm analytics tracking
- [ ] Social media announcement

---

## 👥 TEAM ASSIGNMENTS

| Task | Owner | Status |
|------|-------|--------|
| SCSS/CSS Setup | Frontend Dev | ⏳ Pending |
| Asset Organization | Frontend Dev | ⏳ Pending |
| Image Integration | Frontend Dev | ⏳ Pending |
| Content Review | Project Lead | ⏳ Pending |
| Form Backend | Backend Dev | ⏳ Pending |
| Testing/QA | QA Lead | ⏳ Pending |
| Client Communication | Project Lead | ⏳ Pending |

---

## 📞 CLIENT CONTACT POINTS

**Sharon Mashishi (Founder)**
- Email: Sharon@bahlapingmash.com
- Phone: +27 60 877 5153

**Outstanding Items from Client:**
1. Company/operations photos (CRITICAL)
2. Sharon's professional photo (CRITICAL)
3. Service icons (if custom design wanted)
4. Portfolio project details (4-6 projects)
5. Client testimonials (2-3 quotes)
6. Team member information (optional)

---

## 🎯 SUCCESS METRICS

### Launch Ready When:
- ✅ All 5 core pages functional
- ✅ Lighthouse score 90+
- ✅ Mobile responsive on all devices
- ✅ Forms working properly
- ✅ All images optimized
- ✅ Client approval obtained
- ✅ Performance <3s page load

### Quality Standards:
- ✅ Zero broken links
- ✅ WCAG AA accessibility
- ✅ Cross-browser compatible
- ✅ Mobile-first responsive
- ✅ Zero console errors
- ✅ SEO optimized

---

## 📊 PROGRESS TRACKING

### Week 1 (Phase 1) - Foundation
- Start Date: May 27, 2026
- Target Completion: June 3, 2026
- Status: 🟡 In Progress

### Week 2 (Phase 2) - Content
- Start Date: June 3, 2026
- Target Completion: June 10, 2026
- Status: ⏳ Pending

### Week 3 (Phase 3) - Features
- Start Date: June 10, 2026
- Target Completion: June 17, 2026
- Status: ⏳ Pending

### Week 4 (Phase 4) - Launch
- Start Date: June 17, 2026
- Target Completion: June 24, 2026
- Status: ⏳ Pending

---

## 🚀 NEXT IMMEDIATE ACTIONS (TODAY)

### Frontend Developer:
1. [ ] Review this checklist
2. [ ] Verify SCSS compilation setup
3. [ ] Start organizing asset directories
4. [ ] Confirm all HTML files have content
5. [ ] Schedule daily standup with team

### Project Lead:
1. [ ] Send asset requirements to Sharon
2. [ ] Set up project tracking (Jira/Asana)
3. [ ] Schedule weekly check-ins with client
4. [ ] Assign QA resources
5. [ ] Confirm launch timeline

### Client (Sharon):
1. [ ] Send company/operations photos
2. [ ] Send professional headshot
3. [ ] Confirm all content is accurate
4. [ ] Provide feedback on template layouts
5. [ ] Assign contact person for questions

---

*Execution Status v1.0 | Last Updated: May 27, 2026 | Next Update: June 3, 2026*
