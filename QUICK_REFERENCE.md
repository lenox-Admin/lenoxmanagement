# SEO Quick Reference Guide

## 🚨 Critical Tasks (Do First)

### 1. Update Business Information
**Files to edit:** `index.html`, `contact.html`, `STRUCTURED_DATA_TEMPLATES.md`

Replace these placeholders:
```
Address: "123 Main Street, Your City, State 12345"
Phone: "+1-555-123-4567"
Email: "info@lenoxmanagement.com"
Latitude: "40.7128"
Longitude: "-74.0060"
```

**How to get coordinates:**
Visit https://www.latlong.net/ and enter your address.

---

### 2. Upload Core Files
Upload these to your website root:
- ✅ robots.txt
- ✅ sitemap.xml
- ✅ .htaccess
- ✅ index.html
- ✅ contact.html (create /contact/ directory)

---

### 3. Verify HTTPS
1. Visit: https://www.lenoxmanagement.com
2. Look for padlock icon
3. Test: https://www.ssllabs.com/ssltest/
4. Fix any "mixed content" warnings

---

### 4. Google Search Console
1. Go to: https://search.google.com/search-console/
2. Add property: www.lenoxmanagement.com
3. Verify ownership (HTML file upload)
4. Submit sitemap: https://www.lenoxmanagement.com/sitemap.xml
5. Monitor Coverage and Performance tabs

---

### 5. Google Analytics
1. Create account: https://analytics.google.com/
2. Create property for your site
3. Get tracking ID (G-XXXXXXXXXX)
4. Replace `GA_MEASUREMENT_ID` in HTML files
5. Verify tracking works

---

## 📝 Page-by-Page SEO Checklist

For every page on your site:

### Title Tag
- [ ] 50-60 characters
- [ ] Includes primary keyword
- [ ] Includes brand name
- [ ] Unique for each page

**Example:**
```html
<title>Property Management Services | Lenox Management</title>
```

---

### Meta Description
- [ ] 150-160 characters
- [ ] Includes primary keyword
- [ ] Has call-to-action
- [ ] Unique and compelling

**Example:**
```html
<meta name="description" content="Professional property management services in [City]. Tenant screening, rent collection, maintenance. Call us today!">
```

---

### Canonical Tag
- [ ] Present on every page
- [ ] Points to correct URL
- [ ] Uses absolute URL (includes https://)

**Example:**
```html
<link rel="canonical" href="https://www.lenoxmanagement.com/page/">
```

---

### Heading Tags
- [ ] One H1 per page (main topic)
- [ ] H2-H6 in logical order
- [ ] Keywords included naturally

**Example:**
```html
<h1>Property Management Services</h1>
  <h2>Residential Properties</h2>
    <h3>Apartments</h3>
    <h3>Single-Family Homes</h3>
  <h2>Commercial Properties</h2>
```

---

### Images
- [ ] Compressed (< 100KB most images)
- [ ] Descriptive alt text
- [ ] Width/height attributes set
- [ ] Lazy loading enabled
- [ ] WebP format when possible

**Example:**
```html
<img src="office.webp" 
     alt="Lenox Management modern office building" 
     width="800" 
     height="600" 
     loading="lazy">
```

---

### Structured Data
- [ ] LocalBusiness (homepage)
- [ ] Breadcrumb (all pages except homepage)
- [ ] Appropriate schema for page type
- [ ] Validated with Rich Results Test

**Validation:** https://search.google.com/test/rich-results

---

## 🔍 Common Issues & Fixes

### Issue: Site not appearing in Google
**Fix:**
1. Check robots.txt isn't blocking
2. Verify sitemap submitted to Search Console
3. Check for noindex tags
4. Wait 2-4 weeks for initial indexing

---

### Issue: Slow page speed
**Fix:**
1. Compress images
2. Enable caching (.htaccess already configured)
3. Use CDN for static assets
4. Minimize CSS/JS files
5. Enable lazy loading

**Test:** https://pagespeed.web.dev/

---

### Issue: Mixed content warnings
**Fix:**
1. Ensure all URLs use HTTPS
2. Check: images, CSS, JS, fonts
3. Update any hard-coded http:// links

**Find mixed content:**
```javascript
// Run in browser console
document.querySelectorAll('img, script, link').forEach(el => {
  let src = el.src || el.href;
  if (src && src.startsWith('http:')) console.log(src);
});
```

---

### Issue: Duplicate content
**Fix:**
1. Add canonical tags to all pages
2. Use 301 redirects for old URLs
3. Avoid thin/duplicate pages
4. Use parameter handling in Search Console

---

### Issue: Poor mobile experience
**Fix:**
1. Ensure viewport meta tag present
2. Use responsive images
3. Test on real devices
4. Avoid intrusive interstitials

**Test:** https://search.google.com/test/mobile-friendly

---

## 📊 Key Metrics to Track

### Weekly
- **Organic Traffic:** Google Analytics > Acquisition > All Traffic > Channels
- **Search Queries:** Search Console > Performance
- **Indexed Pages:** Search Console > Coverage
- **Page Speed:** PageSpeed Insights

### Monthly
- **Keyword Rankings:** Manual checks or rank tracker
- **Backlinks:** Search Console > Links
- **Core Web Vitals:** Search Console > Core Web Vitals
- **Conversions:** Google Analytics > Conversions

---

## 🎯 Priority Keywords (Update These!)

Replace with your actual keywords:
1. property management [city]
2. property management services
3. residential property management
4. commercial property management
5. [city] property manager

**Where to use keywords:**
- Title tags
- Meta descriptions
- H1/H2 headings
- First paragraph of content
- Image alt text
- URL slugs

---

## ✅ Weekly Maintenance (15 min)

### Monday Morning Routine
1. [ ] Check site is online: https://www.lenoxmanagement.com
2. [ ] Open Google Search Console
3. [ ] Review Coverage for errors (fix if any)
4. [ ] Check Performance tab for traffic changes
5. [ ] Look for manual actions/security issues
6. [ ] Open Google Analytics
7. [ ] Compare traffic to last week
8. [ ] Note any unusual patterns

---

## 🚀 Content Publishing Checklist

Before publishing new content:

### SEO Basics
- [ ] Unique, optimized title tag
- [ ] Compelling meta description
- [ ] One H1 with primary keyword
- [ ] Proper heading structure (H2, H3, etc.)
- [ ] Canonical tag
- [ ] 300+ words of quality content
- [ ] Internal links to related pages
- [ ] External links to authority sources

### Technical
- [ ] All images optimized and compressed
- [ ] Alt text on all images
- [ ] Mobile-friendly layout
- [ ] Fast load time (< 3 seconds)
- [ ] HTTPS enabled

### Structured Data
- [ ] Breadcrumb schema
- [ ] Article/BlogPosting schema (for blog posts)
- [ ] FAQ schema (if applicable)

### After Publishing
- [ ] Submit URL to Search Console for indexing
- [ ] Update sitemap.xml
- [ ] Share on social media
- [ ] Monitor in Analytics

---

## 🔧 Emergency Fixes

### Site Down
```bash
# Quick check
curl -I https://www.lenoxmanagement.com

# If down:
1. Contact hosting provider immediately
2. Check server status
3. Post status update on social media
4. Monitor Search Console for crawl errors
```

### Traffic Drop > 50%
1. Check Google Analytics to confirm
2. Look for Search Console manual actions
3. Check for recent algorithm updates
4. Verify robots.txt hasn't blocked crawlers
5. Check for noindex tags accidentally added
6. Review recent site changes

### Hacked Site
1. Contact hosting provider immediately
2. Change all passwords
3. Scan for malware
4. Check Search Console for security issues
5. Clean infected files
6. Submit reconsideration request

---

## 📞 Quick Links

### Essential Tools
- Search Console: https://search.google.com/search-console/
- Analytics: https://analytics.google.com/
- PageSpeed: https://pagespeed.web.dev/
- Mobile Test: https://search.google.com/test/mobile-friendly
- Rich Results: https://search.google.com/test/rich-results
- SSL Test: https://www.ssllabs.com/ssltest/

### Help Resources
- Google SEO Guide: https://developers.google.com/search/docs
- Search Console Help: https://support.google.com/webmasters
- Schema.org: https://schema.org/

---

## 💡 Pro Tips

1. **Be Patient:** SEO takes 3-6 months to show results
2. **Content is King:** Quality content > keyword stuffing
3. **Mobile First:** Optimize for mobile devices
4. **User Experience:** Fast, easy-to-use sites rank better
5. **Local SEO:** Claim and optimize Google Business Profile
6. **Backlinks:** Quality > quantity
7. **Regular Updates:** Fresh content signals active site
8. **Monitor Competitors:** Learn from their strategies

---

**Print this guide and keep it handy!**

Last Updated: February 4, 2026
