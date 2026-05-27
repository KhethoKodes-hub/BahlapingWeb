# BAHLAPING MASH WEBSITE 2.0 - DEPLOYMENT & HOSTING GUIDE
**For:** Site Launch & Post-Launch Operations  
**Date:** May 27, 2026  
**Status:** Pre-Launch Planning

---

## 🚀 DEPLOYMENT STRATEGY

### Current Setup
- **Current Site:** https://bahlapingmash.com (WordPress)
- **New Site:** https://bahlapingmash.com (HTML5 Axima template)
- **Timeline:** June 24, 2026 (4 weeks)
- **Approach:** Full migration with rollback capability

### Migration Strategy
1. **Week 1-3:** Develop on staging environment
2. **Week 4:** Final testing on production-like environment
3. **June 24:** Deploy to production during low-traffic window
4. **June 24-25:** Monitor for issues
5. **June 25+:** Redirect old WordPress (301 permanent)

---

## 📋 HOSTING OPTIONS COMPARISON

### Option 1: Shared Hosting (Recommended for Budget)
**Examples:** Bluehost, HostGator, GoDaddy

**Pros:**
- ✅ Cheap ($3-15/month)
- ✅ Easy setup (one-click)
- ✅ Email hosting included
- ✅ SSL certificate included
- ✅ Automatic backups
- ✅ Support included

**Cons:**
- ❌ Slower performance
- ❌ Shared server resources
- ❌ Limited customization

**Best For:** Small business, startup budget

**Cost:** $120-180/year

---

### Option 2: VPS (Virtual Private Server)
**Examples:** Linode, DigitalOcean, Vultr

**Pros:**
- ✅ Better performance
- ✅ Full root access
- ✅ Scalable resources
- ✅ Better security
- ✅ Cheaper than dedicated

**Cons:**
- ❌ More technical setup
- ❌ Need server management
- ❌ Security responsibility yours

**Best For:** Performance-critical, technical team

**Cost:** $60-120/year (basic tier)

---

### Option 3: Static Site Hosting (Fastest)
**Examples:** Netlify, Vercel, GitHub Pages + CloudFlare

**Pros:**
- ✅ Fastest performance (CDN)
- ✅ Cheapest (free tier available)
- ✅ Automatic deployments
- ✅ Version control integration
- ✅ Zero server maintenance

**Cons:**
- ❌ No backend (need separate API for forms)
- ❌ Learning curve
- ❌ Custom domain setup needed

**Best For:** Static HTML5 sites with external form handlers

**Cost:** Free-$20/month

---

## 🌐 RECOMMENDED SETUP FOR BAHLAPING MASH

### Best Value: Shared Hosting + CDN
```
┌─────────────────────────────────┐
│   bahlapingmash.com             │
│   (Domain registrar: GoDaddy)   │
└──────────────┬──────────────────┘
               │
       ┌───────┴──────────┐
       │                  │
    ┌──▼──┐          ┌────▼─────┐
    │ CDN │          │   Host    │
    │ CF  │          │ Bluehost  │
    └─────┘          └──────────┘
     (Free)        ($120/year)
     (CloudFlare)
```

### What You Get
- ✅ Fast performance (CloudFlare CDN)
- ✅ DDoS protection (CloudFlare)
- ✅ Email hosting (Bluehost)
- ✅ SSL certificate (Free with CloudFlare)
- ✅ Automatic backups (Bluehost)
- ✅ Total cost: ~$120/year

### Setup Steps
1. Register domain (if not already)
2. Purchase shared hosting
3. Upload HTML files via FTP
4. Set up email forwarding
5. Connect CloudFlare CDN
6. Enable SSL certificate

---

## 📁 FILE STRUCTURE FOR DEPLOYMENT

### What Gets Uploaded
```
public_html/                 (Root folder on hosting)
├── index.html              (Home page)
├── about-us.html
├── Industries-industry-served.html
├── leadership-team.html
├── contacs.html
├── case-studies-grid.html
├── case-studies-single.html
├── news.html
├── news-single-post.html
├── why-us.html
├── request-quote.html
├── .htaccess               (URL rewriting, if needed)
├── robots.txt              (SEO)
├── sitemap.xml             (SEO)
├── assets/
│   ├── css/
│   │   ├── libraries.css
│   │   └── style.css
│   ├── js/
│   │   ├── jquery-3.3.1.min.js
│   │   ├── plugins.js
│   │   └── main.js
│   ├── images/
│   │   ├── logo/
│   │   ├── about/
│   │   ├── banners/
│   │   ├── services/
│   │   ├── portfolio/
│   │   ├── testimonials/
│   │   ├── backgrounds/
│   │   ├── icons/
│   │   ├── clients/
│   │   └── [other folders]
│   ├── fonts/
│   │   ├── fontawesome-webfont.eot
│   │   ├── fontawesome-webfont.svg
│   │   ├── fontawesome-webfont.ttf
│   │   ├── fontawesome-webfont.woff
│   │   └── fontawesome-webfont.woff2
│   └── scss/               (Keep for reference, not uploaded)
└── [optional: /api/]       (If using external form handler)
```

### What Does NOT Get Uploaded
- ❌ `/Documentation/` folder
- ❌ All `.md` files (planning docs)
- ❌ `.scss` source files (only compiled CSS)
- ❌ Node.js files (package.json, node_modules)
- ❌ Git files (.git, .gitignore)
- ❌ IDE files (.vscode, .idea)

---

## 🔐 SECURITY CHECKLIST

### Pre-Deployment Security

#### 1. HTTPS/SSL Certificate
- [ ] Purchase or request SSL certificate
- [ ] Install on web server
- [ ] Test: https://bahlapingmash.com works
- [ ] All pages accessible via HTTPS
- [ ] Redirect HTTP to HTTPS

**Command for HTTPS redirect (.htaccess):**
```apache
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
```

#### 2. Security Headers
- [ ] Add security headers via .htaccess:
```apache
# Security Headers
<IfModule mod_headers.c>
  Header set Strict-Transport-Security "max-age=31536000; includeSubDomains"
  Header set X-Content-Type-Options "nosniff"
  Header set X-Frame-Options "SAMEORIGIN"
  Header set X-XSS-Protection "1; mode=block"
  Header set Referrer-Policy "strict-origin-when-cross-origin"
</IfModule>
```

#### 3. Directory Protection
- [ ] Disable directory listing (.htaccess):
```apache
Options -Indexes
```

#### 4. File Permissions
- [ ] Set file permissions: 644 (for HTML, CSS, JS)
- [ ] Set directory permissions: 755
- [ ] Sensitive files: 600

#### 5. Backups
- [ ] Daily backups enabled
- [ ] Test backup restoration
- [ ] Store offsite (AWS, Google Drive)
- [ ] Retention: 30 days minimum

#### 6. Monitoring
- [ ] Set up 404 error monitoring
- [ ] Monitor uptime (Uptime Robot)
- [ ] Monitor performance (Pingdom)
- [ ] Set up alerts for issues

---

## 📧 EMAIL CONFIGURATION

### If Using Hosting Provider Email

**Setup (Bluehost example):**
1. [ ] Create email accounts in cPanel
2. [ ] Create: `info@bahlapingmash.com`
3. [ ] Create: `contact@bahlapingmash.com`
4. [ ] Create: `support@bahlapingmash.com`
5. [ ] Configure webmail (Roundcube)

**Test:**
```
Send test email to: info@bahlapingmash.com
Check inbox via webmail
Verify delivery
```

### If Using External Email (Recommended)
**Example: Google Workspace**

**Setup:**
1. [ ] Purchase Google Workspace ($6/user/month)
2. [ ] Add domains in Google admin
3. [ ] Verify domain ownership (TXT record)
4. [ ] Update MX records:
   ```
   aspmx.l.google.com (priority 10)
   alt1.aspmx.l.google.com (priority 20)
   alt2.aspmx.l.google.com (priority 30)
   alt3.aspmx.l.google.com (priority 40)
   alt4.aspmx.l.google.com (priority 50)
   ```
5. [ ] Create user: sharon@bahlapingmash.com
6. [ ] Set up forwarding: contact@bahlapingmash.com → sharon@...

**Test:**
```
Send test email to: contact@bahlapingmash.com
Verify it arrives in Sharon's inbox
Test reply functionality
```

---

## 📬 CONTACT FORM BACKEND SETUP

### Option 1: Formspree (Easiest)

**Setup:**
1. Go to: https://formspree.io
2. Create account (free)
3. Add new form
4. Get form ID (example: abc123)
5. Update form action in `contacs.html`:

```html
<form action="https://formspree.io/f/abc123" method="POST">
  <input type="email" name="email" required>
  <textarea name="message" required></textarea>
  <button type="submit">Send</button>
</form>
```

**Cost:** Free (up to 50/month)

---

### Option 2: Getform

**Setup:**
1. Go to: https://getform.io
2. Create account
3. Add new form
4. Configure actions (email notification)
5. Get endpoint URL
6. Update form action in `contacs.html`:

```html
<form action="https://getform.io/f/abc123" method="POST">
  <!-- form fields -->
</form>
```

**Cost:** Free tier available

---

### Option 3: Self-Hosted PHP Handler

**Create file: `/api/contact.php`**

```php
<?php
// Prevent direct access
if ($_SERVER['REQUEST_METHOD'] != 'POST') {
    http_response_code(405);
    die('Method not allowed');
}

// Get form data
$name = sanitize($_POST['name'] ?? '');
$email = sanitize($_POST['email'] ?? '');
$phone = sanitize($_POST['phone'] ?? '');
$subject = sanitize($_POST['subject'] ?? '');
$message = sanitize($_POST['message'] ?? '');

// Validate
if (!$name || !$email || !$message) {
    http_response_code(400);
    die('Missing required fields');
}

// Prepare email
$to = 'Sharon@bahlapingmash.com';
$headers = "From: $email\r\n";
$headers .= "Reply-To: $email\r\n";
$body = "Name: $name\nPhone: $phone\nSubject: $subject\n\nMessage:\n$message";

// Send email
if (mail($to, "New Contact Form: $subject", $body, $headers)) {
    http_response_code(200);
    echo json_encode(['status' => 'success', 'message' => 'Email sent']);
} else {
    http_response_code(500);
    echo json_encode(['status' => 'error', 'message' => 'Failed to send']);
}

function sanitize($input) {
    return htmlspecialchars(strip_tags(trim($input)));
}
?>
```

**Update form in `contacs.html`:**
```html
<form action="/api/contact.php" method="POST">
  <!-- form fields -->
</form>
```

**Cost:** Free (included with hosting)

---

## 🔗 DNS CONFIGURATION

### Domain Registrar Setup (GoDaddy Example)

**Step 1: Update Nameservers**
1. Log in to GoDaddy
2. Find Domain Manager
3. Update nameservers to hosting provider:
   - `ns1.bluehost.com`
   - `ns2.bluehost.com`
   - (Or your host's nameservers)
4. Wait 24-48 hours for propagation

**Step 2: Verify DNS Records**
```bash
# Test DNS propagation
nslookup bahlapingmash.com
dig bahlapingmash.com

# Should show hosting provider's IP
```

**Step 3: CloudFlare Setup (Optional but Recommended)**
1. Create CloudFlare account (free)
2. Add site: bahlapingmash.com
3. Update nameservers to CloudFlare:
   - `ns1.cloudflare.com`
   - `ns2.cloudflare.com`
4. In CloudFlare, create A record:
   - Name: `bahlapingmash.com`
   - Type: `A`
   - Content: `[Your hosting IP]`
   - Proxied: Yes (orange cloud)

**Cost:** Free CloudFlare account

---

## 🗺️ SEO SETUP

### robots.txt
**Create file: `/robots.txt`**

```
User-agent: *
Allow: /
Disallow: /api/
Disallow: /admin/
Sitemap: https://bahlapingmash.com/sitemap.xml
```

### sitemap.xml
**Create file: `/sitemap.xml`**

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://bahlapingmash.com/</loc>
    <lastmod>2026-05-27</lastmod>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://bahlapingmash.com/about-us.html</loc>
    <lastmod>2026-05-27</lastmod>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://bahlapingmash.com/Industries-industry-served.html</loc>
    <lastmod>2026-05-27</lastmod>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://bahlapingmash.com/contacs.html</loc>
    <lastmod>2026-05-27</lastmod>
    <priority>0.7</priority>
  </url>
  <!-- Add all other pages -->
</urlset>
```

### Google Search Console
1. [ ] Go to: https://search.google.com/search-console
2. [ ] Verify domain ownership
3. [ ] Submit sitemap
4. [ ] Monitor indexing
5. [ ] Check for errors

### Google Analytics
1. [ ] Go to: https://analytics.google.com
2. [ ] Create property for bahlapingmash.com
3. [ ] Get tracking ID
4. [ ] Add to all pages (in `<head>`):

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

---

## 📊 PERFORMANCE OPTIMIZATION

### Image Optimization Before Upload

```bash
# Using ImageMagick
convert image.jpg -quality 80 -strip image-optimized.jpg

# Using ffmpeg for WebP conversion
ffmpeg -i image.jpg -quality 80 image.webp
```

### Minify CSS & JavaScript

```bash
# Install minifier
npm install -g csso-cli uglify-js

# Minify CSS
csso style.css -o style.min.css

# Minify JS
uglifyjs main.js -o main.min.js

# Use minified versions in production
```

### Enable Gzip Compression (.htaccess)

```apache
<IfModule mod_deflate.c>
  AddOutputFilterByType DEFLATE text/plain
  AddOutputFilterByType DEFLATE text/html
  AddOutputFilterByType DEFLATE text/xml
  AddOutputFilterByType DEFLATE text/css
  AddOutputFilterByType DEFLATE text/javascript
  AddOutputFilterByType DEFLATE application/xml
  AddOutputFilterByType DEFLATE application/xhtml+xml
  AddOutputFilterByType DEFLATE application/rss+xml
  AddOutputFilterByType DEFLATE application/javascript
  AddOutputFilterByType DEFLATE application/x-javascript
</IfModule>
```

### Browser Caching (.htaccess)

```apache
<IfModule mod_expires.c>
  ExpiresActive On
  
  # Images
  ExpiresByType image/jpeg "access plus 1 year"
  ExpiresByType image/gif "access plus 1 year"
  ExpiresByType image/png "access plus 1 year"
  ExpiresByType image/webp "access plus 1 year"
  
  # CSS & JavaScript
  ExpiresByType text/css "access plus 1 month"
  ExpiresByType application/javascript "access plus 1 month"
  
  # Fonts
  ExpiresByType font/ttf "access plus 1 year"
  ExpiresByType font/otf "access plus 1 year"
  ExpiresByType font/woff "access plus 1 year"
  ExpiresByType font/woff2 "access plus 1 year"
  
  # Default
  ExpiresDefault "access plus 2 days"
</IfModule>
```

---

## 🔄 MIGRATION FROM WORDPRESS

### Step 1: Content Backup
```bash
# Export WordPress content
# Use: Tools → Export (in WordPress admin)
# Select: All Content
# Download: .xml file
```

### Step 2: Prepare New Site
- [ ] All HTML pages ready
- [ ] All content migrated
- [ ] All images uploaded
- [ ] Forms configured
- [ ] Analytics set up

### Step 3: Staging Test
- [ ] Deploy to staging URL (staging.bahlapingmash.com)
- [ ] Full testing on staging
- [ ] Staging sign-off from client

### Step 4: Production Deployment
- [ ] Create full backup of current WordPress
- [ ] Upload all HTML files
- [ ] Test all pages on production
- [ ] Verify all links work

### Step 5: Traffic Redirection
- [ ] Set up 301 redirects from WordPress pages to new pages
- [ ] Example: `/about/` → `/about-us.html`
- [ ] Test redirects work
- [ ] Verify Google doesn't see duplicate content

**Redirect Examples (.htaccess):**
```apache
# Redirect old WordPress URLs to new HTML pages
RewriteRule ^about/$ /about-us.html [R=301,L]
RewriteRule ^services/$ /Industries-industry-served.html [R=301,L]
RewriteRule ^contact/$ /contacs.html [R=301,L]
RewriteRule ^team/$ /leadership-team.html [R=301,L]
RewriteRule ^portfolio/$ /case-studies-grid.html [R=301,L]

# Catch all: if file doesn't exist, send to index
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ /index.html [L]
```

### Step 6: Decommission WordPress
- [ ] Verify traffic moved to new site
- [ ] Wait 30 days (for SEO)
- [ ] Delete WordPress installation
- [ ] Keep backup for reference

---

## 📈 POST-LAUNCH MONITORING

### Day 1 (Launch Day)
- [ ] Monitor every 15 minutes
- [ ] Check homepage loads
- [ ] Test contact form
- [ ] Verify SSL certificate works
- [ ] Check mobile responsiveness
- [ ] Monitor error logs

### Week 1
- [ ] Daily uptime checks
- [ ] Monitor performance metrics
- [ ] Check for 404 errors
- [ ] Verify analytics tracking
- [ ] Monitor email delivery
- [ ] Check conversion data

### Month 1
- [ ] Weekly performance reviews
- [ ] Monitor user feedback
- [ ] Check search engine indexing
- [ ] Review analytics trends
- [ ] Update content if needed
- [ ] Plan Phase 2 improvements

### Ongoing
- [ ] Monthly security updates
- [ ] Quarterly backups test
- [ ] Semi-annual performance audit
- [ ] Annual SEO review

---

## 🚨 ROLLBACK PLAN

If something goes wrong:

### Hour 1: Identify Issue
- [ ] Check error logs
- [ ] Test on different browsers
- [ ] Test on mobile
- [ ] Verify DNS propagation
- [ ] Check CloudFlare status

### Hour 2-3: Attempt Fix
- [ ] Fix obvious issues (broken links, images)
- [ ] Recompile CSS if needed
- [ ] Clear browser cache
- [ ] Clear CloudFlare cache

### Hour 4: Rollback to Previous Version
```bash
# If using version control
git checkout previous_commit
git push to production

# If manual upload
# Restore from backup
# Upload previous version
```

### Communication
- [ ] Notify Sharon immediately
- [ ] Post status update (if public-facing)
- [ ] Keep stakeholders informed
- [ ] Document issue & fix

---

## 📋 LAUNCH CHECKLIST

### 48 Hours Before Launch
- [ ] Final code review
- [ ] Full testing passed
- [ ] All images optimized
- [ ] Performance targets met
- [ ] Backups created
- [ ] Rollback plan ready
- [ ] Team on standby

### 24 Hours Before Launch
- [ ] Final client approval
- [ ] DNS changes queued
- [ ] Email configured
- [ ] Analytics tracking verified
- [ ] Monitoring alerts set
- [ ] War room scheduled

### Launch Day Morning
- [ ] Team assembled (video call)
- [ ] War room open
- [ ] All monitoring active
- [ ] Deployment ready
- [ ] Client standing by

### Go Time!
- [ ] Deploy to production (10:00 AM)
- [ ] Verify all pages load (10:05 AM)
- [ ] Test contact form (10:10 AM)
- [ ] Check mobile (10:15 AM)
- [ ] Announce on social (10:30 AM)
- [ ] Monitor for 2 hours
- [ ] Team debrief (12:00 PM)
- [ ] Celebration! 🎉 (1:00 PM)

---

*Deployment & Hosting Guide v1.0 | May 27, 2026*
