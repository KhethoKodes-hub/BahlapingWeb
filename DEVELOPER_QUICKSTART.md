# BAHLAPING MASH 2.0 | QUICK START DEVELOPER GUIDE
**For:** Frontend & Backend Developers  
**Date:** May 27, 2026  
**Project:** Website Modernization v2.0

---

## 🚀 5-MINUTE PROJECT OVERVIEW

**What:** Modernize Bahlaping Mash website from WordPress to modern HTML5  
**Why:** Better performance, lower maintenance, fresher design  
**How:** Use Axima template (already customized with company content)  
**When:** 4-week project starting today  
**Where:** `/axima/` folder structure

---

## 📁 YOUR WORKING DIRECTORY

```
/Users/khethomngomezulu/Desktop/MaySItes/BahlapingMash/BahlapingWeb/
├── axima/                          ← YOUR MAIN FOLDER
│   ├── index.html                  ✅ READY (Bahlaping content)
│   ├── about-us.html               ✅ READY
│   ├── Industries-industry-served.html  ✅ READY
│   ├── leadership-team.html        ✅ READY
│   ├── contacs.html                ✅ READY
│   ├── case-studies-grid.html      (Portfolio)
│   ├── case-studies-single.html    (Detail)
│   ├── news.html                   (Blog)
│   ├── news-single-post.html       (Article)
│   ├── why-us.html                 (Value prop)
│   ├── request-quote.html          (Forms)
│   └── assets/
│       ├── css/
│       │   ├── libraries.css       (Bootstrap + plugins)
│       │   └── style.css           ✅ COMPILED from SCSS
│       ├── scss/
│       │   ├── style.scss          (Main source)
│       │   └── global/
│       │       └── _vars.scss      ← CONFIGURE HERE
│       ├── images/
│       │   ├── logo/               ← ADD Bahlaping logos
│       │   ├── about/              ← ADD company photos
│       │   ├── banners/            ← ADD hero images
│       │   ├── services/           ← ADD service icons
│       │   ├── portfolio/          ← ADD projects
│       │   └── testimonials/       ← ADD client photos
│       ├── js/
│       │   ├── jquery-3.3.1.min.js
│       │   ├── main.js             (Custom logic)
│       │   └── plugins.js          (jQuery plugins)
│       └── fonts/
│           └── (FontAwesome icons already included)
└── Documentation/                  (Template docs)
```

---

## ⚡ QUICK COMMANDS

### Start Development
```bash
# Navigate to project
cd /Users/khethomngomezulu/Desktop/MaySItes/BahlapingMash/BahlapingWeb

# Watch SCSS for changes
cd axima/assets/scss
sass --watch . ../css

# In another terminal, run a local server
cd /Users/khethomngomezulu/Desktop/MaySItes/BahlapingMash/BahlapingWeb/axima
python3 -m http.server 8000

# Open browser
open http://localhost:8000
```

### Test on Mobile
```bash
# Get your local IP
ifconfig | grep "inet " | grep -v 127.0.0.1

# Then visit: http://YOUR_IP:8000 on your phone
```

---

## 🎨 COLORS (Already Configured)

**Primary Orange:** `#ff5e14`  
**Dark Blue:** `#0b2653`  
**Body Text:** `#51668a`  
**White:** `#ffffff`

**Location:** `axima/assets/scss/global/_vars.scss`

```scss
// Verify these exist:
$primary-color: #ff5e14;      // Orange buttons
$dark-color: #0b2653;          // Headings
$text-color: #51668a;          // Body text
$white-color: #ffffff;         // Backgrounds
```

---

## 📋 TODAY'S TASKS (Phase 1 - Week 1)

### 1. Verify Template Setup ✅
```bash
cd axima
# Check if all HTML files exist
ls -la *.html

# Expected output:
# ✅ index.html
# ✅ about-us.html
# ✅ Industries-industry-served.html
# ✅ leadership-team.html
# ✅ contacs.html
# ✅ why-us.html
# (+ more optional files)
```

### 2. Test SCSS Compilation
```bash
cd axima/assets/scss
sass --watch . ../css

# You should see:
# Sass is watching for changes. Press Ctrl-C to stop.
```

### 3. Open in Browser
- Navigate to: `http://localhost:8000/axima/`
- Should see: Modern factory/mining template with **Bahlaping Mash content**
- Check: Orange theme (#ff5e14) is applied
- Verify: Company info in header & footer

### 4. Create Asset Directories
```bash
cd axima/assets/images

# Create folders needed for images:
mkdir -p about banners services portfolio testimonials/thumbs

# Verify structure:
ls -la
```

### 5. Check Current Content
**In index.html, verify you see:**
- ✅ "9+ Years of Excellence in Mining, Engineering & Construction"
- ✅ "Turning Your Vision Into Tangible Results!"
- ✅ 3 service cards (Cable Pit, Chrome Export, Civil & Construction)
- ✅ "+27 60 877 5153" in hero section
- ✅ "Sharon Mashishi — Director" in services section

---

## 📸 IMAGES NEEDED FROM CLIENT

**Wait for these from Sharon (email template):**

### Critical (Needed for MVP)
1. **Hero Image** (1200x600px) - Mining operations
2. **Sharon Headshot** (400x400px) - Professional photo
3. **Bahlaping Logo Files:**
   - Logo light (for dark backgrounds)
   - Logo dark (for light backgrounds)
   - Logo footer version

### Important (For Phase 2)
4. **Service Images** (600x600px each):
   - Cable pit reticulation work
   - Chrome mining/export
   - Civil construction project

5. **Company Photos** (1000x600px):
   - Operations/facility
   - Team at work

6. **Portfolio Images** (800x600px each):
   - Project 1, 2, 3, 4

---

## 🔧 KEY FILES TO MODIFY

### For Every Page Change:
**File:** `axima/assets/scss/global/_vars.scss`
```scss
// Colors (already set, don't change)
$primary-color: #ff5e14;
$dark-color: #0b2653;

// Fonts (verify these are loading)
$font-family-sans-serif: 'Open Sans', sans-serif;
$headings-font-family: 'Poppins', sans-serif;
```

### Content Changes:
**Files to edit directly (HTML):**
- `index.html` - Home page (hero, services preview, about preview)
- `about-us.html` - Company story, mission/vision, credentials
- `Industries-industry-served.html` - 3 main services
- `leadership-team.html` - Sharon + team profiles
- `contacs.html` - Contact form, map, info

### Image Placement:
**CSS Background Images:**
- Hero slider: `axima/assets/images/sliders/1.jpg`
- About section: `axima/assets/images/about/2.jpg`
- Banners: `axima/assets/images/banners/[1-4].jpg`

**HTML Image Tags:**
- Logo: `<img src="assets/images/logo/logo-light.png">`
- Team: `<img src="assets/images/[...]/sharon-photo.jpg">`

---

## 📝 CONTENT ALREADY IN PLACE

### Home Page (index.html) ✅
- Hero title: "Turning Your Vision Into Tangible Results!"
- Subtitle: "9+ Years of Excellence in Mining, Engineering & Construction."
- Description: BBBEE Level 1 black woman-owned company
- 3 services: Cable Pit, Chrome Export, Civil & Construction
- Contact chip: "+27 60 877 5153 | Sharon Mashishi — Director"
- Footer: All company info, certifications, social links

### About Page (about-us.html) ✅
- Company story: Founded 2016, BBBEE Level 1
- Sharon Mashishi prominent feature
- Mission/Vision statements
- 5 certifications listed
- "9+ Years" experience counter
- Contact info: sharon.mashishi@bahlapingmash.com

### Services Page (Industries-industry-served.html) ✅
- 3 service cards with descriptions
- Cable Pit Reticulation (4-shift electrical service)
- Export/Import Chrome (Southern Africa operations)
- Civil & Construction (turnkey projects)
- Contact: Sharon's phone number
- CTA buttons throughout

### Team Page (leadership-team.html) ✅
- Ready for Sharon's photo + bio
- Team member placeholders
- Contact section with details

### Contact Page (contacs.html) ✅
- Address: House 060175, Ga-chaba village, Mapela 0610
- Phone: +27 60 877 5153
- Email: Sharon@bahlapingmash.com
- Hours: Mon-Fri 8:00-17:00
- Contact form with service dropdown
- Google Map placeholder

---

## 🎯 IMMEDIATE NEXT STEPS

### For Frontend Dev (You - Right Now)
1. [ ] Open terminal
2. [ ] Navigate to: `cd /Users/khethomngomezulu/Desktop/MaySItes/BahlapingMash/BahlapingWeb/axima`
3. [ ] Start SCSS watch: `sass --watch assets/scss:assets/css`
4. [ ] Start server: `python3 -m http.server 8000` (in another terminal)
5. [ ] Open: `http://localhost:8000`
6. [ ] Make a small CSS change to verify SCSS compilation works
7. [ ] Screenshot the home page
8. [ ] Report back: "Template verified and working"

### For Backend Dev
1. [ ] Review contact form in `contacs.html`
2. [ ] Set up form endpoint (PHP/Node/Lambda)
3. [ ] Test form submission locally
4. [ ] Set up email notifications to Sharon
5. [ ] Report: "Form backend ready"

### For Project Lead
1. [ ] Send this document to team
2. [ ] Send asset requirements to Sharon
3. [ ] Schedule daily standup tomorrow at [TIME]
4. [ ] Create project tracking board
5. [ ] Set up progress tracking

---

## 🐛 COMMON ISSUES & FIXES

### Issue: SCSS not compiling
```bash
# Check if sass is installed
sass --version

# If not, install:
npm install -g sass

# Then try again:
sass --watch axima/assets/scss:axima/assets/css
```

### Issue: Browser not refreshing changes
```bash
# Hard refresh (clear cache)
Cmd+Shift+R (Mac)
Ctrl+Shift+F5 (Windows)

# Or manually reload CSS in browser DevTools
```

### Issue: Images not loading
```
Check: Are images in correct folder?
✅ axima/assets/images/[category]/[filename]

Check: Is path correct in HTML?
✅ src="assets/images/..." (relative path)
❌ src="/assets/images/..." (absolute path won't work locally)
```

### Issue: Template looks broken
- [ ] Check browser console (F12 → Console tab)
- [ ] Look for 404 errors
- [ ] Verify all CSS files loaded
- [ ] Verify all JS files loaded
- [ ] Clear browser cache and reload

---

## 📞 SUPPORT & COMMUNICATION

### Team Questions?
- Post in project Slack/Discord channel
- Tag relevant team member
- Include screenshot/error message

### Client (Sharon) Communication?
- Use templates in `/PROJECT_TEMPLATES/` folder
- Keep communication professional and clear
- Always confirm receipt of assets
- Send weekly status updates

### Emergency Issues?
1. Check this guide first
2. Search GitHub issues for similar problems
3. Escalate to Project Lead
4. Consider rolling back last changes

---

## 📊 PROGRESS CHECKLIST

### Week 1 (Foundation)
- [ ] SCSS compilation verified
- [ ] Asset directories created
- [ ] All HTML files loading correctly
- [ ] Browser displays Bahlaping content
- [ ] Template logo/colors verified
- [ ] Development environment ready

### Week 2 (Content)
- [ ] Images received from client
- [ ] Images integrated into pages
- [ ] Contact form backend working
- [ ] All links tested and working
- [ ] Mobile responsive verified
- [ ] Content proof-read

### Week 3 (Features)
- [ ] Portfolio section complete
- [ ] Blog section ready
- [ ] All forms functional
- [ ] Accessibility audit passed
- [ ] SEO optimized
- [ ] Performance optimized

### Week 4 (Launch)
- [ ] Final testing complete
- [ ] Client sign-off obtained
- [ ] Domain/hosting ready
- [ ] Analytics configured
- [ ] Deployed to production
- [ ] Post-launch monitoring active

---

## 🎬 YOU'RE READY TO START!

**Project Status:** 🟢 GO  
**Next Standup:** Tomorrow  
**First Milestone:** SCSS + Asset setup (by June 3)  

**Questions?** Check the 4 planning documents in the workspace:
1. `MODERNIZATION_GAMEPLAN_v2.0.md` - Full strategy
2. `PAGE_BY_PAGE_CONTENT_MAPPING.md` - Detailed content
3. `BEFORE_AND_AFTER_ANALYSIS.md` - Current vs New
4. `QUICK_REFERENCE.md` - Developer shortcuts

**Let's build something amazing for Bahlaping Mash! 🚀**

---

*Quick Start Guide v1.0 | May 27, 2026*
