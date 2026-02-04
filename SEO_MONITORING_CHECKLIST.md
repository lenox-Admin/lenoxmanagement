# SEO Monitoring & Maintenance Checklist

## Daily Tasks (5 minutes)

### Site Health Check
- [ ] Verify site is online: https://www.lenoxmanagement.com
- [ ] Check for critical alerts in Google Search Console
- [ ] Review overnight traffic spikes/drops in Google Analytics

### Quick Monitoring
```bash
# Simple uptime check
curl -I https://www.lenoxmanagement.com | grep "200 OK"

# Check robots.txt is accessible
curl https://www.lenoxmanagement.com/robots.txt

# Check sitemap is accessible
curl https://www.lenoxmanagement.com/sitemap.xml
```

---

## Weekly Tasks (30 minutes)

### Search Console Review
- [ ] Open Google Search Console
- [ ] Check Coverage report for indexing errors
- [ ] Review Performance tab for traffic trends
- [ ] Check for new manual actions or security issues
- [ ] Review Core Web Vitals report

### Analytics Review
- [ ] Check Google Analytics weekly traffic
- [ ] Identify top-performing pages
- [ ] Review traffic sources (organic, direct, referral, social)
- [ ] Check bounce rate and average session duration
- [ ] Note any unusual traffic patterns

### Content Updates
- [ ] Publish new blog post (if applicable)
- [ ] Update recent properties listings
- [ ] Respond to reviews/comments

### Technical Checks
- [ ] Check site load speed: https://pagespeed.web.dev/
- [ ] Verify HTTPS certificate hasn't expired
- [ ] Check for broken links on homepage and key pages

---

## Monthly Tasks (2-3 hours)

### Comprehensive Search Console Review
- [ ] Deep dive into Coverage report
- [ ] Check Mobile Usability issues
- [ ] Review search queries and click-through rates
- [ ] Analyze average position changes
- [ ] Check for crawl errors
- [ ] Review indexed pages count

### Analytics Deep Dive
- [ ] Generate monthly traffic report
- [ ] Analyze top landing pages
- [ ] Review goal completions/conversions
- [ ] Identify traffic source performance
- [ ] User demographics and behavior analysis
- [ ] Compare month-over-month growth

### Keyword Performance
- [ ] Check keyword rankings (use free tools or manual searches)
- [ ] Identify ranking improvements/declines
- [ ] Research new keyword opportunities
- [ ] Update meta tags for underperforming pages

### Content Audit
- [ ] Review and update outdated content
- [ ] Check for thin content pages
- [ ] Identify content gaps
- [ ] Update statistics and data
- [ ] Refresh meta descriptions for top pages

### Technical SEO
- [ ] Run full site crawl (Screaming Frog or similar)
- [ ] Check for broken links: https://www.deadlinkchecker.com/
- [ ] Verify all images have alt text
- [ ] Check for duplicate content
- [ ] Review canonical tags
- [ ] Check structured data validity: https://search.google.com/test/rich-results

### Backlink Analysis
- [ ] Check new backlinks (Google Search Console > Links)
- [ ] Identify spam/toxic links
- [ ] Disavow harmful links if necessary
- [ ] Look for backlink opportunities
- [ ] Monitor competitor backlinks

### Sitemap Maintenance
- [ ] Update sitemap.xml if new pages added
- [ ] Verify sitemap submission in Search Console
- [ ] Check sitemap is error-free

### Performance Optimization
- [ ] Run Lighthouse audit
- [ ] Check Core Web Vitals:
  - Largest Contentful Paint (LCP): < 2.5s
  - First Input Delay (FID): < 100ms
  - Cumulative Layout Shift (CLS): < 0.1
- [ ] Optimize images if needed
- [ ] Review page load times

### Security Check
- [ ] Scan for security vulnerabilities
- [ ] Check SSL certificate expiration
- [ ] Review security headers: https://securityheaders.com/
- [ ] Update WordPress/plugins (if applicable)
- [ ] Backup website

---

## Quarterly Tasks (1 day)

### Comprehensive SEO Audit
- [ ] Full technical SEO audit
- [ ] Complete content audit
- [ ] Competitive analysis
- [ ] Site structure review
- [ ] Mobile usability testing
- [ ] Accessibility audit

### Content Strategy Review
- [ ] Analyze content performance
- [ ] Plan new content topics
- [ ] Update content calendar
- [ ] Identify evergreen content to refresh
- [ ] Review user engagement metrics

### Structured Data Review
- [ ] Validate all structured data
- [ ] Update LocalBusiness information
- [ ] Add new schema types if applicable
- [ ] Test rich results appearance

### Link Building
- [ ] Reach out for new backlink opportunities
- [ ] Guest posting outreach
- [ ] Local directory submissions
- [ ] Partner link exchanges
- [ ] Monitor brand mentions

### Competitive Analysis
- [ ] Identify top 5 competitors
- [ ] Analyze competitor keywords
- [ ] Review competitor backlinks
- [ ] Study competitor content strategy
- [ ] Benchmark your performance

### Local SEO (if applicable)
- [ ] Update Google Business Profile
- [ ] Manage and respond to reviews
- [ ] Update NAP (Name, Address, Phone) across directories
- [ ] Local citations audit
- [ ] Local keyword optimization

### Reporting
- [ ] Create quarterly SEO report
- [ ] Traffic trends analysis
- [ ] ROI calculation
- [ ] Set goals for next quarter
- [ ] Present findings to stakeholders

---

## Annual Tasks (2-3 days)

### Year-End Review
- [ ] Comprehensive annual SEO report
- [ ] Year-over-year growth analysis
- [ ] Review all KPIs and metrics
- [ ] Calculate ROI of SEO efforts

### Complete Content Refresh
- [ ] Review all website pages
- [ ] Update copyright year
- [ ] Refresh all outdated content
- [ ] Remove or consolidate thin content
- [ ] Update all meta tags

### Technical Overhaul
- [ ] Full site architecture review
- [ ] URL structure optimization
- [ ] Internal linking audit and optimization
- [ ] Redirect audit (clean up old 301s)
- [ ] Page speed comprehensive optimization

### Strategic Planning
- [ ] Set SEO goals for next year
- [ ] Identify growth opportunities
- [ ] Plan content strategy
- [ ] Budget allocation for SEO
- [ ] Tool and resource evaluation

### Certifications & Renewals
- [ ] Renew SSL certificate (if not auto-renewing)
- [ ] Review and update privacy policy
- [ ] Update terms of service
- [ ] Renew paid SEO tools subscriptions

---

## Alerts to Set Up

### Google Search Console Alerts
Set up email notifications for:
- New security issues
- Manual actions
- Coverage issues
- Core Web Vitals issues

### Uptime Monitoring
Set up alerts with UptimeRobot or similar:
- Site down notifications
- Response time alerts
- SSL certificate expiration warnings

### Analytics Alerts
Google Analytics custom alerts:
- Traffic drops > 25% day-over-day
- Conversion rate drops
- Unusual spike in bounce rate
- Error pages (404) increase

---

## Key Performance Indicators (KPIs)

Track these metrics monthly:

### Traffic Metrics
- Organic traffic (sessions)
- New vs. returning visitors
- Pages per session
- Average session duration
- Bounce rate

### Ranking Metrics
- Number of keywords ranking in top 10
- Number of keywords ranking in top 3
- Average position for target keywords

### Conversion Metrics
- Contact form submissions
- Phone calls from website
- Property inquiries
- Newsletter signups

### Technical Metrics
- Pages indexed
- Crawl errors
- Page load speed (LCP)
- Mobile usability errors
- Core Web Vitals passing URLs

### Authority Metrics
- Total backlinks
- Referring domains
- Domain Authority (Moz)
- Domain Rating (Ahrefs)

---

## Tools & Resources

### Free Monitoring Tools
- **Google Search Console:** https://search.google.com/search-console/
- **Google Analytics:** https://analytics.google.com/
- **UptimeRobot:** https://uptimerobot.com/
- **PageSpeed Insights:** https://pagespeed.web.dev/
- **Mobile-Friendly Test:** https://search.google.com/test/mobile-friendly

### Chrome Extensions
- **Lighthouse:** Built into Chrome DevTools
- **SEO Meta in 1 Click:** Quick meta tag review
- **Link Redirect Trace:** Check redirect chains
- **Check My Links:** Find broken links on page

### Crawling Tools
- **Screaming Frog:** https://www.screamingfrog.co.uk/ (Free up to 500 URLs)
- **Sitebulb:** https://sitebulb.com/ (Paid, free trial)

---

## Emergency Procedures

### Site Down
1. Check if it's a hosting issue
2. Contact hosting provider
3. Post status update on social media
4. Monitor Search Console for crawl errors
5. Document downtime duration

### Traffic Drop
1. Check Google Analytics for verification
2. Review Search Console for manual actions
3. Check for algorithm updates
4. Verify technical issues (robots.txt, noindex tags)
5. Compare with industry trends
6. Document and investigate cause

### Security Breach
1. Immediately contact hosting provider
2. Change all passwords
3. Scan for malware
4. Check Search Console for security issues
5. Submit reconsideration request if hacked
6. Restore from clean backup

### Lost Rankings
1. Verify with multiple rank tracking tools
2. Check for manual actions in Search Console
3. Review recent Google algorithm updates
4. Check for technical issues
5. Analyze competitor changes
6. Review recent content changes

---

## Monthly Reporting Template

### Executive Summary
- Overall traffic: [number] sessions ([+/-]% vs. last month)
- Organic traffic: [number] sessions ([+/-]% vs. last month)
- Top performing page: [page name]
- Key wins this month: [list]
- Areas for improvement: [list]

### Traffic Breakdown
- Organic: [number] ([+/-]%)
- Direct: [number] ([+/-]%)
- Referral: [number] ([+/-]%)
- Social: [number] ([+/-]%)

### Keyword Performance
- Keywords in top 3: [number]
- Keywords in top 10: [number]
- Biggest ranking gains: [list]
- Biggest ranking losses: [list]

### Technical Health
- Indexed pages: [number]
- Crawl errors: [number]
- Core Web Vitals: [Pass/Fail]
- Page speed: [score]

### Backlinks
- Total backlinks: [number] ([+/-])
- Referring domains: [number] ([+/-])
- New quality backlinks: [list]

### Actions for Next Month
1. [Action item 1]
2. [Action item 2]
3. [Action item 3]

---

**Last Updated:** February 4, 2026
