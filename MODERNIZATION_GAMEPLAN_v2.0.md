# BAHLAPING MASH WEBSITE MODERNIZATION 2.0
## Strategic Gameplan & Execution Blueprint

**Date:** May 27, 2026  
**Current Site:** https://bahlapingmash.com (WordPress)  
**Template Base:** Axima - Factory & Manufacturing HTML Template (Envato)  
**Objective:** Modernize UI/UX while maintaining brand identity and content integrity

---

## 🎯 CURRENT STATE ANALYSIS

### Current Live Site (WordPress)
**Status:** Functional but dated design
- **Platform:** WordPress with custom theme
- **Strengths:**
  - Clear service offerings (Cable Pit, Chrome Export, Civil & Construction)
  - Established company story
  - Contact information accessible
  - Social media integration
  - Professional branding elements

- **Weaknesses:**
  - Slow loading performance (WordPress overhead)
  - Limited mobile responsiveness
  - Outdated visual hierarchy
  - Poor accessibility features
  - WordPress maintenance burden

### Template Analysis (Axima)
- **Type:** Factory & Manufacturing HTML Template
- **Technology:** HTML5, CSS3 (SCSS), jQuery, Bootstrap 4
- **Perfect fit for Bahlaping Mash:**
  - ✅ Industry-appropriate (manufacturing/mining focus)
  - ✅ Modern, professional aesthetic
  - ✅ Orange theme (#ff5e14) aligns perfectly
  - ✅ Multiple layout variations
  - ✅ Performance optimized (static files)
  - ✅ Full customization control

---

## 📊 CONTENT MAPPING: Current → New Template

| Current | New Template | Purpose |
|---|---|---|
| Home | `index.html` | Hero + Services Overview |
| About | `about-us.html` | Company Story (Founded 2016, BBBEE Level 1) |
| Services | `Industries-industry-served.html` | Service Showcase |
| Service Detail | `industries-single-industry.html` | Individual Services |
| Team | `leadership-team.html` | Sharon + Team Members |
| Contact | `contacs.html` | Contact Form + Map |
| Case Studies | `case-studies-grid.html` | Project Portfolio |
| Why Us | `why-us.html` | Value Proposition |

---

## 🎨 BRANDING STRATEGY

### Color Palette (Locked):
- **Primary Orange:** #ff5e14 (Already matches Axima!)
- **Dark Blue:** #0b2653 (Professional headings)
- **Body Text:** #51668a (Readability)
- **Backgrounds:** #ffffff (Clean white)

### Key Brand Elements:
1. **Black Woman-Owned:** Prominent (Sharon Mashishi, Founded 2016)
2. **Certifications:** BBBEE Level 1, CIDB GR 7, SANS 1393:2023, VAT Registered
3. **Geographic Focus:** Mapela, Limpopo, Southern Africa
4. **Core Services:** 
   - Cable Pit Reticulation (Electrical)
   - Export/Import Chrome (Mining)
   - Civil & Construction (Projects)

---

## 🏗️ SITE ARCHITECTURE

### Main Navigation:
```
HOME
├─ COMPANY
│  ├─ About Us
│  ├─ Leadership Team
│  └─ Why Choose Us
├─ SERVICES
│  ├─ Cable Pit Reticulation
│  ├─ Export/Import Chrome
│  └─ Civil & Construction
├─ PORTFOLIO
├─ NEWS
├─ REQUEST QUOTE
└─ CONTACT
```

---

## 🔧 IMPLEMENTATION PHASES

### PHASE 1: Foundation (Week 1)
**Files to Configure:**
- `assets/scss/global/_vars.scss` - Finalize colors
- `assets/scss/style.scss` - Import structure
- Create `/assets/images/` directories
- Set up SCSS compilation

**Deliverables:**
- [ ] Template structure verified
- [ ] Color variables confirmed
- [ ] Asset directories organized
- [ ] Development environment ready

### PHASE 2: Content Integration (Week 2)
**Pages to Create:**
1. **index.html** - Hero section with mining operations image
2. **about-us.html** - Company story, 2016 founding, Sharon's vision
3. **Industries-industry-served.html** - 3 service cards with icons
4. **leadership-team.html** - Sharon Mashishi profile + team
5. **contacs.html** - Contact form, map, credentials

**Content Points:**
- Address: House 060175, Ga-chaba village, Mapela 0610
- Phone: +27 60 877 5153
- Email: Sharon@bahlapingmash.com
- Hours: Mon-Fri 8:00-17:00

### PHASE 3: Features & Optimization (Week 3)
- [ ] Contact form functionality
- [ ] Portfolio/case studies
- [ ] Blog/news section
- [ ] Request quote form
- [ ] Image optimization (WebP, lazy loading)
- [ ] SEO optimization
- [ ] Accessibility (WCAG 2.1 AA)

### PHASE 4: Testing & Deployment (Week 4)
- [ ] Performance audit (Lighthouse 90+)
- [ ] Mobile responsiveness
- [ ] Cross-browser testing
- [ ] Accessibility audit
- [ ] Security scan
- [ ] Domain migration setup

---

## 🎯 KEY CUSTOMIZATIONS

### 1. HOME HERO
```
Background: Mining operations image
Headline: "Innovative Mining & Engineering Solutions"
Subtext: "BBBEE Level 1 | Trusted Across Southern Africa"
CTA: "Explore Services" + "Download Profile"
```

### 2. SERVICES SECTION (3 Cards)
**Cable Pit Reticulation**
- 4-shift continuous service on 6.6KV electrical networks
- Shovels, drills, pumps support

**Export/Import Chrome**
- Chrome ore mining & export
- Zimbabwe & South Africa operations
- Spiral wash plants, concentrates

**Civil & Construction**
- Turnkey projects
- Residential, commercial, infrastructure
- Roads, dams, bridges

### 3. CERTIFICATIONS (Footer/About)
- Reg: 2016/519101/07
- CSD Registered
- CIDB Registered (GR 7 GB/CE)
- BBBEE Level One
- VAT Registered
- SANS 1393:2023 Accredited

### 4. SOCIAL LINKS
- Facebook: p/Bahlaping-Mash-Trading-Mining-and-Project-61550189019944/
- Twitter: @bahlaping_mash
- Instagram: @bahlaping_mash
- LinkedIn: company/bahlaping-mash-trading-mining-and-projects/

---

## 📱 RESPONSIVE DESIGN

**Breakpoints (Bootstrap):**
- Desktop: 1200px+ (full experience)
- Tablet: 768px - 1199px (optimized)
- Mobile: <768px (touch-optimized, stacked)

---

## 🚀 PERFORMANCE TARGETS

- Page Load Time: < 3 seconds
- Lighthouse Score: 90+
- First Contentful Paint: < 1.5s
- Mobile Friendly: 100%

---

## 🔍 SEO OPTIMIZATION

**Meta Tags:**
- Title: "Bahlaping Mash - Mining & Engineering Solutions | BBBEE Level 1"
- Description: "Innovative mining, cable pit reticulation, chrome export, and civil construction services across Southern Africa."
- Keywords: Mining, engineering, construction, chrome export, South Africa, BBBEE

**Technical SEO:**
- Semantic HTML5
- Schema.org markup
- Open Graph tags
- XML sitemap
- robots.txt

---

## ✅ LAUNCH CHECKLIST

**Pre-Launch:**
- [ ] All pages created & populated
- [ ] Images optimized & compressed
- [ ] All links tested
- [ ] Forms functional
- [ ] Mobile responsive
- [ ] Performance optimized
- [ ] SEO audit passed
- [ ] Accessibility verified
- [ ] Security scan passed

**Post-Launch:**
- [ ] Domain redirects configured
- [ ] Analytics tracking verified
- [ ] Search Console setup
- [ ] Monitoring active
- [ ] Backups established

---

## 💡 FUTURE ENHANCEMENTS (v2.1+)

1. **Headless CMS** - Easy content updates for Sharon
2. **Client Portal** - Project tracking & document sharing
3. **Blog/Thought Leadership** - Industry insights
4. **Multi-language** - Afrikaans, Setswana support
5. **Advanced Analytics** - Heatmapping, user journeys
6. **E-commerce** - Service package ordering

---

## 📞 PROJECT CONTACTS

**Client:**
- Sharon Mashishi (Founder)
- Email: Sharon@bahlapingmash.com
- Phone: +27 60 877 5153

---

## ✨ EXECUTION READINESS: **GO**

**Prerequisites Met:**
- ✅ Template selected and appropriate
- ✅ Content analyzed and mapped
- ✅ Brand colors confirmed
- ✅ Company information compiled
- ✅ Design direction clear
- ✅ Current site analyzed (WordPress)
- ✅ Content structure confirmed
- ✅ Navigation finalized

**Ready to Begin Phase 1 Implementation**

---

## 🎬 EXECUTION KICKOFF - MAY 27, 2026

### Current Site Analysis Complete ✅
**Live Site:** https://bahlapingmash.com (WordPress)
- 3 main service offerings documented
- Sharon Mashishi founder story confirmed
- 9+ years in business established
- BBBEE Level 1, multiple certifications visible
- Contact info verified: +27 60 877 5153 | Sharon@bahlapingmash.com
- Address confirmed: House 060175, Ga-chaba village, Mapela 0610
- Operating hours: Mon-Fri 8:00-17:00

### Content Extracted ✅
**From WordPress:**
- Company mission & vision statements
- 3 core services fully documented
- Certifications (5 items)
- Social media links (4 platforms)
- Team information (Sharon featured)
- Gallery/portfolio items available

### Template Status ✅
**Axima Template (HTML5):**
- Index.html - Ready with Bahlaping content
- About-us.html - Ready with company story
- Industries-industry-served.html - 3 services configured
- Leadership-team.html - Ready for Sharon feature
- Contact page - Ready with Mapela details
- Footer - All pages branded with Bahlaping colors

### Brand Alignment ✅
**Color Palette (Locked):**
- Primary Orange: #ff5e14 (Already matches template!)
- Dark Blue: #0b2653 (Professional)
- Body Text: #51668a (Readable)
- Background: #ffffff (Clean)

### Phase 1 Tasks (This Week) 🚀
1. **SCSS Variables** - Finalize color/font variables
2. **Asset Organization** - Prepare image directories
3. **Image Collection** - Gather company/team photos (⏳ Needed from Sharon)
4. **Logo Setup** - Place Bahlaping logo files
5. **Development Environment** - Set up SCSS compilation

### Phase 2 Tasks (Next Week) 📝
1. **Page Content Integration** - Populate all 5 core pages
2. **Form Setup** - Contact form backend
3. **Link Verification** - Test all navigation
4. **Mobile Responsiveness** - Verify Bootstrap breakpoints

### Critical Assets Needed from Client ⏳
1. Company operations/hero image (1200x800px minimum)
2. Sharon Mashishi professional photo (400x400px)
3. 2-4 team member photos + bios (optional for v1)
4. Service-related icons/graphics (if custom)
5. Portfolio project images (4-6 items)

### GO/NO-GO Decision Points
- [ ] Phase 1 complete → Proceed to Phase 2
- [ ] All pages populated → Proceed to Phase 3
- [ ] Testing passed → Proceed to Phase 4
- [ ] Client approval → Proceed to launch

---

*Document Version 1.1 | Last Updated: May 27, 2026 | Status: EXECUTION KICKOFF*
