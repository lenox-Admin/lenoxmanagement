# Deployment Guide
## How to Deploy Your SEO Package to www.Lenoxmanagement.com

---

## ⚠️ BEFORE YOU START

### 1. Backup Your Current Website
```bash
# If you have SSH access:
tar -czf backup-$(date +%Y%m%d).tar.gz /path/to/website/

# Or use your hosting control panel's backup feature
```

### 2. Review All Files
Before uploading, make sure you've:
- [ ] Updated business information (address, phone, email)
- [ ] Updated geographic coordinates
- [ ] Created necessary images
- [ ] Reviewed all HTML content

---

## 📤 DEPLOYMENT STEPS

### Step 1: Update Business Information (Required!)

**Files to edit:**
- `index.html`
- `contact.html`
- `services.html`

**What to update:**
```
Find and replace these placeholders:

Address:
  "123 Main Street" → Your actual street address
  "Your City" → Your city
  "State" → Your state abbreviation
  "12345" → Your ZIP code

Contact:
  "+1-555-123-4567" → Your phone number
  "info@lenoxmanagement.com" → Your email

Geographic coordinates:
  "40.7128" → Your latitude
  "-74.0060" → Your longitude
  (Get from: https://www.latlong.net/)

Hours:
  Adjust business hours in LocalBusiness schema

Social Media:
  Replace placeholder social media URLs with your actual profiles
```

### Step 2: Upload Core Files to Website Root

**Using FTP/SFTP Client (FileZilla, Cyberduck, etc.):**

Upload these files to your website root directory (usually `public_html`, `www`, or `htdocs`):

```
Source Files          →  Destination
─────────────────────────────────────────────────
robots.txt            →  /robots.txt
sitemap.xml           →  /sitemap.xml
.htaccess             →  /.htaccess
index.html            →  /index.html
```

**Using cPanel File Manager:**
1. Log into cPanel
2. Click "File Manager"
3. Navigate to public_html (or your root directory)
4. Click "Upload"
5. Upload the files listed above

### Step 3: Upload Page Templates

Create directories and upload page templates:

```
1. Create /contact/ directory
   Upload: contact.html to /contact/index.html

2. Create /services/ directory
   Upload: services.html to /services/index.html
```

**Important:** Rename files to `index.html` when placing in subdirectories so they load as:
- www.lenoxmanagement.com/contact/
- www.lenoxmanagement.com/services/

### Step 4: Upload Images (After Creating Them)

Create `/images/` directory and upload:
```
/images/logo.png
/images/og-image.jpg
/images/og-contact.jpg
/images/og-services.jpg
/images/office.jpg
/images/residential.webp
/images/commercial.webp
```

Also upload to root:
```
/favicon.ico
/favicon-16x16.png
/favicon-32x32.png
/apple-touch-icon.png
```

### Step 5: Verify File Permissions

Ensure files have correct permissions:
```
Files (.html, .txt, .xml):     644
Directories:                   755
.htaccess:                     644
```

**Using cPanel:**
- Right-click file → Change Permissions
- Files: 644 (Owner: Read+Write, Group: Read, Public: Read)
- Directories: 755 (Owner: Read+Write+Execute, Group: Read+Execute, Public: Read+Execute)

**Using SSH:**
```bash
cd /path/to/website
chmod 644 robots.txt sitemap.xml .htaccess *.html
chmod 755 images/
```

---

## ✅ VERIFICATION STEPS

### 1. Verify Files Are Accessible

Test in your browser:
```
✓ https://www.lenoxmanagement.com/robots.txt
✓ https://www.lenoxmanagement.com/sitemap.xml
✓ https://www.lenoxmanagement.com/
✓ https://www.lenoxmanagement.com/contact/
✓ https://www.lenoxmanagement.com/services/
```

Each should load without errors.

### 2. Verify HTTPS Redirect

Test HTTP to HTTPS redirect:
```
1. Visit: http://www.lenoxmanagement.com
2. Should automatically redirect to: https://www.lenoxmanagement.com
3. Check for padlock icon in browser
```

### 3. Test SSL Certificate

Visit: https://www.ssllabs.com/ssltest/
- Enter: www.lenoxmanagement.com
- Click "Submit"
- Aim for grade A or A+

### 4. Check Mobile Friendliness

Visit: https://search.google.com/test/mobile-friendly
- Enter your URL
- Run test
- Fix any issues found

### 5. Test Page Speed

Visit: https://pagespeed.web.dev/
- Enter your URL
- Run test for both mobile and desktop
- Aim for 80+ on mobile, 90+ on desktop

### 6. Validate Structured Data

Visit: https://search.google.com/test/rich-results
- Enter: https://www.lenoxmanagement.com/
- Click "Test URL"
- Fix any errors
- Repeat for other pages

---

## 🔧 GOOGLE SEARCH CONSOLE SETUP

### 1. Access Search Console
Visit: https://search.google.com/search-console/

### 2. Add Property
- Click "Add Property"
- Choose "URL prefix"
- Enter: https://www.lenoxmanagement.com
- Click "Continue"

### 3. Verify Ownership

**Method 1: HTML File Upload (Recommended)**
1. Download verification file from Search Console
2. Upload to your website root
3. Verify it's accessible at: https://www.lenoxmanagement.com/google[xxxxx].html
4. Click "Verify" in Search Console

**Method 2: HTML Tag**
1. Copy meta tag from Search Console
2. Add to `<head>` section of index.html
3. Re-upload index.html
4. Click "Verify"

### 4. Submit Sitemap
1. In Search Console, go to "Sitemaps" (left menu)
2. Enter: sitemap.xml
3. Click "Submit"
4. Wait for processing (may take hours/days)

### 5. Verify Sitemap
- Check "Sitemaps" section in Search Console
- Status should be "Success"
- Should show number of discovered URLs

---

## 📊 GOOGLE ANALYTICS SETUP

### 1. Create Account
Visit: https://analytics.google.com/
- Sign in with Google account
- Click "Start measuring"
- Enter account name: "Lenox Management"

### 2. Create Property
- Property name: "Lenox Management Website"
- Time zone: Your time zone
- Currency: USD (or your currency)

### 3. Get Tracking Code
- Choose "Web" platform
- Enter: www.lenoxmanagement.com
- Get your Measurement ID (format: G-XXXXXXXXXX)

### 4. Update HTML Files
Edit these files:
- index.html
- contact.html
- services.html

Find this line:
```javascript
gtag('config', 'GA_MEASUREMENT_ID');
```

Replace `GA_MEASUREMENT_ID` with your actual ID:
```javascript
gtag('config', 'G-ABC123XYZ');
```

### 5. Re-upload Files
Upload the updated HTML files to your server.

### 6. Verify Tracking
1. Visit your website
2. In Google Analytics, go to "Reports" → "Realtime"
3. You should see yourself as an active user
4. If not, check console for errors (F12 in browser)

---

## 🔔 MONITORING SETUP

### 1. UptimeRobot (Free Uptime Monitoring)

**Sign Up:**
1. Visit: https://uptimerobot.com/
2. Create free account

**Add Monitor:**
1. Click "Add New Monitor"
2. Monitor Type: HTTP(s)
3. Friendly Name: "Lenox Management"
4. URL: https://www.lenoxmanagement.com
5. Monitoring Interval: 5 minutes
6. Click "Create Monitor"

**Set Up Alerts:**
1. Go to "My Settings" → "Alert Contacts"
2. Add email address
3. Add phone number for SMS (optional)
4. Save

### 2. Search Console Email Notifications

In Google Search Console:
1. Click Settings (gear icon)
2. Click "Users and permissions"
3. Ensure your email is added
4. Email notifications are automatic for:
   - Manual actions
   - Security issues
   - Critical coverage issues

---

## 📱 GOOGLE BUSINESS PROFILE (Local SEO)

### 1. Claim/Create Profile
Visit: https://www.google.com/business/

### 2. Complete Profile
- Business name
- Category: "Property Management Company"
- Address (must match website)
- Phone (must match website)
- Website URL
- Hours of operation
- Add photos (minimum 10)
- Add services
- Add description

### 3. Verify Location
Google will send verification postcard to your address.

### 4. Optimize Profile
- Respond to all reviews
- Post regular updates
- Add Q&A
- Enable messaging
- Add products/services

---

## 🐛 TROUBLESHOOTING

### Issue: HTTPS Not Working

**Cause:** SSL certificate not installed
**Fix:** 
1. Contact hosting provider
2. Request free Let's Encrypt SSL certificate
3. Or purchase SSL certificate
4. Follow host's SSL installation guide

### Issue: .htaccess Not Working

**Cause:** Apache mod_rewrite not enabled
**Fix:**
1. Contact hosting support
2. Ask them to enable mod_rewrite
3. Verify .htaccess is in root directory
4. Check file permissions (644)

### Issue: 404 Errors on Subpages

**Cause:** Files not in correct directories
**Fix:**
1. Ensure /contact/index.html exists
2. Ensure /services/index.html exists
3. Check file names are lowercase
4. Verify no extra file extensions

### Issue: Images Not Loading

**Cause:** Incorrect image paths or missing files
**Fix:**
1. Create /images/ directory
2. Upload all images
3. Verify image file names match HTML
4. Check file permissions (644)
5. Use browser dev tools (F12) to see exact error

### Issue: Google Analytics Not Tracking

**Cause:** Incorrect Measurement ID or blocked by ad blocker
**Fix:**
1. Verify Measurement ID is correct
2. Check browser console for errors (F12)
3. Disable ad blockers
4. Wait 24-48 hours for data to appear
5. Test in incognito/private browsing

### Issue: Search Console Not Indexing

**Cause:** Normal - takes time
**Fix:**
1. Be patient (can take 1-4 weeks)
2. Submit URL for indexing manually:
   - Search Console → URL Inspection
   - Enter URL
   - Click "Request Indexing"
3. Share site on social media
4. Build a few backlinks

---

## 📋 POST-DEPLOYMENT CHECKLIST

### Immediate (Within 24 Hours)
- [ ] All files accessible (robots.txt, sitemap.xml, pages)
- [ ] HTTPS working with padlock icon
- [ ] No mixed content warnings
- [ ] Search Console verified
- [ ] Sitemap submitted
- [ ] Analytics tracking verified
- [ ] Mobile-friendly test passed
- [ ] Page speed acceptable

### Week 1
- [ ] Check Search Console for errors
- [ ] Verify pages being crawled
- [ ] Monitor analytics for traffic
- [ ] Check for any 404 errors
- [ ] Verify structured data no errors

### Week 2-4
- [ ] Site appearing in Google (search: site:www.lenoxmanagement.com)
- [ ] Pages being indexed
- [ ] Analytics showing organic traffic
- [ ] No critical Search Console issues

---

## 🎯 NEXT STEPS AFTER DEPLOYMENT

### Week 1-2: Content & Images
- Create and optimize all images
- Write additional page content
- Create About page
- Create Privacy Policy
- Create Terms of Service

### Week 3-4: Local SEO
- Complete Google Business Profile
- Submit to online directories
- Ensure NAP consistency
- Request initial customer reviews

### Month 2: Content Marketing
- Start blog (if applicable)
- Create valuable content
- Share on social media
- Email marketing setup

### Month 3+: Link Building
- Reach out to partners
- Guest posting
- Industry directories
- Local sponsorships

---

## 📞 SUPPORT RESOURCES

### If You Get Stuck

**Hosting Issues:**
- Contact your hosting provider support
- Have FTP credentials ready
- Explain what you're trying to do

**Google Search Console:**
- Help Center: https://support.google.com/webmasters
- Community Forum: https://support.google.com/webmasters/community

**Google Analytics:**
- Help Center: https://support.google.com/analytics
- Community: https://support.google.com/analytics/community

**SEO Questions:**
- Google SEO Guide: https://developers.google.com/search/docs
- Reference the documentation files in this package

---

## ✅ FINAL VERIFICATION

Before considering deployment complete:

```
✓ Business information updated in all files
✓ All files uploaded to correct locations
✓ HTTPS working correctly
✓ robots.txt accessible
✓ sitemap.xml accessible
✓ All pages loading without errors
✓ Images displaying correctly
✓ Google Search Console verified
✓ Sitemap submitted to Search Console
✓ Google Analytics tracking working
✓ Mobile-friendly test passed
✓ Page speed acceptable (80+ mobile, 90+ desktop)
✓ Structured data valid (no errors)
✓ Uptime monitoring configured
✓ No JavaScript errors in console
```

---

## 🎉 CONGRATULATIONS!

If you've completed all the steps above, your SEO package is successfully deployed!

**What happens next:**
- Google will start crawling your site
- Pages will be indexed (1-4 weeks)
- Rankings will improve over 3-6 months
- Organic traffic will grow steadily

**Remember:**
- Monitor Search Console weekly
- Update content regularly
- Build quality backlinks
- Be patient - SEO takes time!

---

**Need Help?** Review the comprehensive guides in the documentation files.

**Last Updated:** February 4, 2026
