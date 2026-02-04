# Structured Data (JSON-LD) Templates

This document contains JSON-LD structured data templates for common page types on the Lenox Management website.

## LocalBusiness Schema (Homepage)

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "@id": "https://www.lenoxmanagement.com/#organization",
  "name": "Lenox Management",
  "url": "https://www.lenoxmanagement.com",
  "logo": "https://www.lenoxmanagement.com/images/logo.png",
  "image": "https://www.lenoxmanagement.com/images/office.jpg",
  "description": "Professional property management services for residential and commercial properties",
  "priceRange": "$$",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Main Street",
    "addressLocality": "Your City",
    "addressRegion": "State",
    "postalCode": "12345",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "40.7128",
    "longitude": "-74.0060"
  },
  "telephone": "+1-555-123-4567",
  "email": "info@lenoxmanagement.com",
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "09:00",
      "closes": "17:00"
    }
  ],
  "sameAs": [
    "https://www.facebook.com/lenoxmanagement",
    "https://www.linkedin.com/company/lenoxmanagement",
    "https://twitter.com/lenoxmanagement"
  ]
}
```

## Organization Schema

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Lenox Management",
  "url": "https://www.lenoxmanagement.com",
  "logo": "https://www.lenoxmanagement.com/images/logo.png",
  "contactPoint": {
    "@type": "ContactPoint",
    "telephone": "+1-555-123-4567",
    "contactType": "customer service",
    "email": "info@lenoxmanagement.com",
    "areaServed": "US",
    "availableLanguage": ["English"]
  },
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Main Street",
    "addressLocality": "Your City",
    "addressRegion": "State",
    "postalCode": "12345",
    "addressCountry": "US"
  }
}
```

## Breadcrumb Schema (Example: Services Page)

```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://www.lenoxmanagement.com/"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Services",
      "item": "https://www.lenoxmanagement.com/services/"
    }
  ]
}
```

## Service Schema (For Service Pages)

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "serviceType": "Property Management",
  "provider": {
    "@type": "LocalBusiness",
    "name": "Lenox Management",
    "url": "https://www.lenoxmanagement.com"
  },
  "areaServed": {
    "@type": "State",
    "name": "Your State"
  },
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Property Management Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Residential Property Management"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Commercial Property Management"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Tenant Screening"
        }
      }
    ]
  }
}
```

## FAQ Schema

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What property management services does Lenox Management offer?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Lenox Management offers comprehensive property management services including tenant screening, rent collection, maintenance coordination, property inspections, financial reporting, and 24/7 emergency support."
      }
    },
    {
      "@type": "Question",
      "name": "How do I contact Lenox Management?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "You can contact us by phone at +1-555-123-4567, email at info@lenoxmanagement.com, or visit our office at 123 Main Street during business hours Monday through Friday, 9 AM to 5 PM."
      }
    },
    {
      "@type": "Question",
      "name": "What areas does Lenox Management serve?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Lenox Management provides property management services throughout [Your City/Region/State]. Contact us to verify if we service your specific area."
      }
    }
  ]
}
```

## RealEstateListing Schema (For Property Pages)

```json
{
  "@context": "https://schema.org",
  "@type": "RealEstateListing",
  "name": "3-Bedroom Apartment - 456 Oak Street",
  "url": "https://www.lenoxmanagement.com/properties/456-oak-street",
  "description": "Beautiful 3-bedroom, 2-bathroom apartment with modern amenities",
  "datePosted": "2026-02-04",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "456 Oak Street",
    "addressLocality": "Your City",
    "addressRegion": "State",
    "postalCode": "12345",
    "addressCountry": "US"
  },
  "offers": {
    "@type": "Offer",
    "price": "2000",
    "priceCurrency": "USD",
    "availability": "https://schema.org/InStock",
    "priceSpecification": {
      "@type": "UnitPriceSpecification",
      "price": "2000",
      "priceCurrency": "USD",
      "unitText": "per month"
    }
  },
  "numberOfRooms": 3,
  "numberOfBathroomsTotal": 2,
  "floorSize": {
    "@type": "QuantitativeValue",
    "value": "1200",
    "unitCode": "SQF"
  }
}
```

## Blog Post / Article Schema

```json
{
  "@context": "https://schema.org",
  "@type": "BlogPosting",
  "headline": "5 Tips for First-Time Renters",
  "image": "https://www.lenoxmanagement.com/images/blog/first-time-renters.jpg",
  "author": {
    "@type": "Organization",
    "name": "Lenox Management"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Lenox Management",
    "logo": {
      "@type": "ImageObject",
      "url": "https://www.lenoxmanagement.com/images/logo.png"
    }
  },
  "datePublished": "2026-02-04",
  "dateModified": "2026-02-04",
  "description": "Essential tips for first-time renters to make the rental process smooth and successful."
}
```

## WebSite Schema (For Site Search)

```json
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "name": "Lenox Management",
  "url": "https://www.lenoxmanagement.com",
  "potentialAction": {
    "@type": "SearchAction",
    "target": "https://www.lenoxmanagement.com/search?q={search_term_string}",
    "query-input": "required name=search_term_string"
  }
}
```

## ContactPage Schema

```json
{
  "@context": "https://schema.org",
  "@type": "ContactPage",
  "name": "Contact Lenox Management",
  "description": "Contact information for Lenox Management",
  "mainEntity": {
    "@type": "LocalBusiness",
    "name": "Lenox Management",
    "telephone": "+1-555-123-4567",
    "email": "info@lenoxmanagement.com",
    "address": {
      "@type": "PostalAddress",
      "streetAddress": "123 Main Street",
      "addressLocality": "Your City",
      "addressRegion": "State",
      "postalCode": "12345",
      "addressCountry": "US"
    }
  }
}
```

## AboutPage Schema

```json
{
  "@context": "https://schema.org",
  "@type": "AboutPage",
  "name": "About Lenox Management",
  "description": "Learn about Lenox Management's history, mission, and team",
  "mainEntity": {
    "@type": "Organization",
    "name": "Lenox Management",
    "foundingDate": "2010",
    "description": "Professional property management company serving residential and commercial clients"
  }
}
```

## Review / Rating Schema (If you have testimonials)

```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Lenox Management",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "127",
    "bestRating": "5",
    "worstRating": "1"
  },
  "review": [
    {
      "@type": "Review",
      "author": {
        "@type": "Person",
        "name": "John Smith"
      },
      "datePublished": "2026-01-15",
      "reviewBody": "Excellent property management service. Very professional and responsive.",
      "reviewRating": {
        "@type": "Rating",
        "ratingValue": "5",
        "bestRating": "5"
      }
    }
  ]
}
```

## Video Schema (If you have property tour videos)

```json
{
  "@context": "https://schema.org",
  "@type": "VideoObject",
  "name": "Virtual Tour: 3-Bedroom Apartment on Oak Street",
  "description": "Take a virtual tour of this beautiful 3-bedroom apartment",
  "thumbnailUrl": "https://www.lenoxmanagement.com/images/video-thumb.jpg",
  "uploadDate": "2026-02-04",
  "duration": "PT3M45S",
  "contentUrl": "https://www.lenoxmanagement.com/videos/oak-street-tour.mp4",
  "embedUrl": "https://www.lenoxmanagement.com/embed/oak-street-tour"
}
```

## How to Implement

### 1. Add to HTML `<head>` section

```html
<script type="application/ld+json">
{
  // Paste your JSON-LD schema here
}
</script>
```

### 2. Multiple Schemas on One Page

You can include multiple schemas on a single page:

```html
<!-- LocalBusiness Schema -->
<script type="application/ld+json">
{ ... }
</script>

<!-- Breadcrumb Schema -->
<script type="application/ld+json">
{ ... }
</script>

<!-- FAQ Schema -->
<script type="application/ld+json">
{ ... }
</script>
```

### 3. Validation

Always validate your structured data:
- Rich Results Test: https://search.google.com/test/rich-results
- Schema Markup Validator: https://validator.schema.org/

### 4. Customization Checklist

For each schema, update:
- [ ] Business name
- [ ] Address
- [ ] Phone number
- [ ] Email
- [ ] Operating hours
- [ ] Geographic coordinates
- [ ] Social media links
- [ ] Actual content/descriptions
- [ ] Dates
- [ ] URLs

## Common Mistakes to Avoid

❌ Using fake or incorrect information
❌ Marking up content not visible to users
❌ Adding structured data for content that doesn't exist on the page
❌ Using the wrong schema type
❌ Forgetting to update placeholder values
❌ Not validating the markup

✅ Keep structured data accurate and up-to-date
✅ Match schema to actual page content
✅ Use multiple schemas when appropriate
✅ Validate before deploying
✅ Monitor Search Console for structured data errors

## Resources

- Schema.org Documentation: https://schema.org/
- Google Structured Data Guide: https://developers.google.com/search/docs/advanced/structured-data/intro-structured-data
- Rich Results Test: https://search.google.com/test/rich-results
- Schema Markup Generator: https://technicalseo.com/tools/schema-markup-generator/
