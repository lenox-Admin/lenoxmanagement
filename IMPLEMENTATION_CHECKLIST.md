# SEO Implementation Checklist
## Print this and check off items as you complete them

---

## 🚨 CRITICAL - Do These First

### Business Information Updates
- [ ] Edit `index.html` - Update business address
- [ ] Edit `index.html` - Update phone number
- [ ] Edit `index.html` - Update email address
- [ ] Edit `index.html` - Update business hours
- [ ] Get coordinates from https://www.latlong.net/
- [ ] Edit `index.html` - Update latitude/longitude
- [ ] Edit `contact.html` - Update all contact info
- [ ] Edit `services.html` - Update service area/state
- [ ] Update social media URLs in schema

### File Uploads
- [ ] Upload `robots.txt` to website root
- [ ] Upload `sitemap.xml` to website root
- [ ] Upload `.htaccess` to website root
- [ ] Upload `index.html` as homepage
- [ ] Create `/contact/` directory
- [ ] Upload `contact.html` to `/contact/` directory
- [ ] Create `/services/` directory
- [ ] Upload `services.html` to `/services/` directory

### HTTPS Setup
- [ ] Verify SSL certificate is installed
- [ ] Test site loads with https://
- [ ] Check for padlock icon in browser
- [ ] Test at https://www.ssllabs.com/ssltest/
- [ ] Fix any mixed content warnings
- [ ] Verify .htaccess redirects HTTP to HTTPS

### Search Console Setup
- [ ] Go to https://search.google.com/search-console/
- [ ] Add property: www.lenoxmanagement.com
- [ ] Download verification HTML file
- [ ] Upload verification file to website root
- [ ] Click "Verify" in Search Console
- [ ] Submit sitemap URL: https://www.lenoxmanagement.com/sitemap.xml
- [ ] Verify sitemap was accepted (no errors)

### Google Analytics Setup
- [ ] Create account at https://analytics.google.com/
- [ ] Create property for www.lenoxmanagement.com
- [ ] Get tracking ID (G-XXXXXXXXXX)
- [ ] Replace `GA_MEASUREMENT_ID` in `index.html`
- [ ] Replace `GA_MEASUREMENT_ID` in `contact.html`
- [ ] Replace `GA_MEASUREMENT_ID` in `services.html`
- [ ] Test tracking is working (visit site, check Real-Time in Analytics)

---

## 📝 IMPORTANT - Complete Soon

### Image Creation
- [ ] Create logo.png (200x60px, < 20KB)
- [ ] Create favicon.ico (16x16px and 32x32px)
- [ ] Create apple-touch-icon.png (180x180px)
- [ ] Create og-image.jpg for homepage (1200x630px)
- [ ] Create og-contact.jpg for contact page (1200x630px)
- [ ] Create og-services.jpg for services page (1200x630px)
- [ ] Create twitter card images (1200x675px)
- [ ] Compress all images (< 100KB each)
- [ ] Upload images to `/images/` directory

### Image Optimization
- [ ] Install image optimization plugin or tool
- [ ] Convert existing images to WebP format
- [ ] Add alt text to all images
- [ ] Verify lazy loading is working
- [ ] Check images on mobile devices

### Additional Pages
- [ ] Create About page with proper meta tags
- [ ] Create Properties/Portfolio page
- [ ] Create Blog page (if applicable)
- [ ] Create Privacy Policy page
- [ ] Create Terms of Service page
- [ ] Add canonical tags to all pages
- [ ] Add breadcrumb schema to all subpages

### Structured Data
- [ ] Validate all structured data: https://search.google.com/test/rich-results
- [ ] Fix any errors found in validation
- [ ] Add FAQ schema to relevant pages
- [ ] Add Review schema if you have testimonials
- [ ] Test rich results appearance

### Mobile Optimization
- [ ] Test mobile-friendly: https://search.google.com/test/mobile-friendly
- [ ] Fix any mobile usability issues
- [ ] Test on actual mobile devices (iOS & Android)
- [ ] Verify tap targets are appropriately sized
- [ ] Check responsive images work correctly

---

## 🔍 TESTING & VALIDATION

### Technical SEO Tests
- [ ] Test robots.txt: https://www.lenoxmanagement.com/robots.txt
- [ ] Test sitemap.xml: https://www.lenoxmanagement.com/sitemap.xml
- [ ] SSL test: https://www.ssllabs.com/ssltest/ (aim for A or A+)
- [ ] Security headers: https://securityheaders.com/ (aim for A or higher)
- [ ] Mobile-friendly: https://search.google.com/test/mobile-friendly
- [ ] PageSpeed desktop: https://pagespeed.web.dev/ (aim for 90+)
- [ ] PageSpeed mobile: https://pagespeed.web.dev/ (aim for 80+)

### Meta Tags Tests
- [ ] Preview homepage meta tags: https://metatags.io/
- [ ] Preview contact meta tags: https://metatags.io/
- [ ] Preview services meta tags: https://metatags.io/
- [ ] Test Facebook share: https://developers.facebook.com/tools/debug/
- [ ] Test Twitter share: https://cards-dev.twitter.com/validator
- [ ] LinkedIn share test: https://www.linkedin.com/post-inspector/

### Structured Data Tests
- [ ] Rich Results Test homepage: https://search.google.com/test/rich-results
- [ ] Rich Results Test contact page
- [ ] Rich Results Test services page
- [ ] Schema validator: https://validator.schema.org/
- [ ] Fix any errors or warnings

### Performance Tests
- [ ] GTmetrix: https://gtmetrix.com/ (aim for A/B grades)
- [ ] WebPageTest: https://www.webpagetest.org/
- [ ] Chrome DevTools Lighthouse audit
- [ ] Check Core Web Vitals in Search Console (after 28 days)

---

## 🌐 THIRD-PARTY INTEGRATIONS

### Search Engine Submissions
- [ ] Submit to Google Search Console ✓ (done above)
- [ ] Submit to Bing Webmaster Tools: https://www.bing.com/webmasters/
- [ ] Verify Bing ownership
- [ ] Submit sitemap to Bing

### Google Business Profile (Local SEO)
- [ ] Claim/create Google Business Profile
- [ ] Verify business location
- [ ] Add complete business information
- [ ] Add business hours
- [ ] Add business photos (min 10)
- [ ] Add services
- [ ] Set up Q&A section
- [ ] Enable messaging
- [ ] Request reviews from customers

### Social Media Setup
- [ ] Create/update Facebook business page
- [ ] Create/update LinkedIn company page
- [ ] Create/update Twitter business account
- [ ] Ensure all profiles link to website
- [ ] Add business information to all profiles
- [ ] Match NAP (Name, Address, Phone) across all platforms

### Directory Listings
- [ ] List on Yelp (if applicable)
- [ ] List on Better Business Bureau
- [ ] List on industry-specific directories
- [ ] Ensure NAP consistency across all directories

---

## 📊 MONITORING SETUP

### Uptime Monitoring
- [ ] Create UptimeRobot account: https://uptimerobot.com/
- [ ] Add monitor for www.lenoxmanagement.com
- [ ] Set check interval (5-15 minutes)
- [ ] Configure email alerts
- [ ] Configure SMS alerts (optional)
- [ ] Test alerts are working

### Search Console Alerts
- [ ] Enable email notifications in Search Console
- [ ] Configure alerts for coverage issues
- [ ] Configure alerts for manual actions
- [ ] Configure alerts for security issues
- [ ] Configure alerts for Core Web Vitals

### Analytics Alerts
- [ ] Set up custom alert for traffic drop > 25%
- [ ] Set up alert for conversion rate changes
- [ ] Set up alert for bounce rate spike
- [ ] Set up alert for error page (404) increase

### Regular Monitoring Schedule
- [ ] Add daily check to calendar (5 min)
- [ ] Add weekly review to calendar (30 min)
- [ ] Add monthly audit to calendar (2-3 hours)
- [ ] Add quarterly review to calendar (1 day)

---

## 📈 ONGOING OPTIMIZATION

### Content
- [ ] Create content calendar
- [ ] Plan blog posts (if applicable)
- [ ] Update properties/portfolio regularly
- [ ] Add customer testimonials
- [ ] Create case studies
- [ ] Update outdated content quarterly

### Keywords
- [ ] Research primary keywords
- [ ] Research long-tail keywords
- [ ] Create keyword map for each page
- [ ] Track keyword rankings
- [ ] Update content based on keyword performance

### Link Building
- [ ] Create backlink strategy
- [ ] Reach out to industry partners
- [ ] Submit to relevant directories
- [ ] Guest posting opportunities
- [ ] Monitor competitor backlinks
- [ ] Disavow spam links if found

### Technical Maintenance
- [ ] Update sitemap when adding pages
- [ ] Check for broken links monthly
- [ ] Monitor 404 errors in Search Console
- [ ] Update structured data as needed
- [ ] Optimize new images before upload
- [ ] Monitor page speed monthly

---

## 🎯 ADVANCED OPTIMIZATION (Optional)

### Advanced Technical
- [ ] Implement CDN (Cloudflare recommended)
- [ ] Set up AMP for mobile (if beneficial)
- [ ] Implement progressive web app features
- [ ] Add service worker for offline capability
- [ ] Optimize critical rendering path
- [ ] Implement HTTP/2 push

### Advanced Tracking
- [ ] Set up conversion tracking
- [ ] Configure e-commerce tracking (if applicable)
- [ ] Set up event tracking
- [ ] Implement heat mapping (Hotjar, Crazy Egg)
- [ ] Set up session recording
- [ ] Configure custom dimensions in Analytics

### Advanced Schema
- [ ] Add Video schema (if you have videos)
- [ ] Add Event schema (if you host events)
- [ ] Add Review schema
- [ ] Add Product schema (if applicable)
- [ ] Add HowTo schema
- [ ] Add Aggregate Rating schema

---

## ✅ FINAL VERIFICATION

### Pre-Launch Checklist
- [ ] All business information is accurate
- [ ] All placeholder content replaced
- [ ] All images optimized and uploaded
- [ ] All pages have unique title tags
- [ ] All pages have unique meta descriptions
- [ ] All pages have canonical tags
- [ ] All images have alt text
- [ ] HTTPS is working correctly
- [ ] No mixed content warnings
- [ ] Sitemap submitted to Search Console
- [ ] Analytics tracking verified
- [ ] Mobile-friendly test passed
- [ ] Page speed acceptable (80+ mobile, 90+ desktop)
- [ ] No JavaScript errors in console
- [ ] Forms are working (if applicable)
- [ ] 404 page is set up
- [ ] Privacy policy in place
- [ ] Cookie consent (if needed for GDPR)

### Post-Launch 24-Hour Check
- [ ] Site is indexed (search: site:www.lenoxmanagement.com)
- [ ] Analytics showing traffic
- [ ] Search Console showing impressions
- [ ] No critical errors in Search Console
- [ ] Uptime monitor hasn't triggered
- [ ] Forms receiving submissions (test)
- [ ] Social sharing working correctly

### Post-Launch Week 1
- [ ] Search Console coverage report reviewed
- [ ] Initial keyword positions noted
- [ ] Baseline Analytics metrics recorded
- [ ] Any issues from Search Console addressed
- [ ] All pages indexed
- [ ] Sitemaps processed successfully

### Post-Launch Month 1
- [ ] First monthly report created
- [ ] Keyword rankings tracked
- [ ] Traffic trends analyzed
- [ ] Any technical issues resolved
- [ ] Content plan for month 2 created
- [ ] First batch of content published

---

## 📞 EMERGENCY CONTACTS

In case of issues:

**Hosting Provider:** ___________________________
**Phone:** ___________________________
**Email:** ___________________________

**Web Developer:** ___________________________
**Phone:** ___________________________
**Email:** ___________________________

**SSL Certificate Provider:** ___________________________
**Renewal Date:** ___________________________

**Domain Registrar:** ___________________________
**Login:** ___________________________

---

## 📅 DATES COMPLETED

- Setup Started: _______________
- Files Uploaded: _______________
- HTTPS Verified: _______________
- Search Console Verified: _______________
- Analytics Set Up: _______________
- Site Launched: _______________
- First Indexed: _______________

---

**Print this checklist and track your progress!**

Last Updated: February 4, 2026
