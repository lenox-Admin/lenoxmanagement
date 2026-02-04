# Image Optimization Guide

## Quick Reference

### Recommended Image Sizes

| Use Case | Recommended Size | Format | Max File Size |
|----------|-----------------|--------|---------------|
| Hero images | 1920x1080px | WebP/JPG | 200KB |
| Feature images | 1200x800px | WebP/JPG | 150KB |
| Thumbnails | 400x300px | WebP/JPG | 50KB |
| Logo | 200x60px | SVG/PNG | 20KB |
| Open Graph | 1200x630px | JPG | 300KB |
| Twitter Card | 1200x675px | JPG | 300KB |
| Favicon | 32x32px, 16x16px | PNG/ICO | 10KB |
| Apple Touch Icon | 180x180px | PNG | 30KB |

### Compression Guidelines

**Target compression levels:**
- JPG: 80-85% quality
- WebP: 75-80% quality
- PNG: Use tools like TinyPNG or pngquant

### Image Lazy Loading Implementation

**HTML method (native):**
```html
<img src="image.jpg" alt="Description" loading="lazy" width="800" height="600">
```

**JavaScript fallback:**
```html
<img data-src="image.jpg" alt="Description" class="lazyload" width="800" height="600">
<noscript>
  <img src="image.jpg" alt="Description" width="800" height="600">
</noscript>
```

### Responsive Images with srcset

```html
<picture>
  <source 
    srcset="image-400.webp 400w,
            image-800.webp 800w,
            image-1200.webp 1200w"
    sizes="(max-width: 600px) 400px,
           (max-width: 1000px) 800px,
           1200px"
    type="image/webp">
  <img 
    srcset="image-400.jpg 400w,
            image-800.jpg 800w,
            image-1200.jpg 1200w"
    sizes="(max-width: 600px) 400px,
           (max-width: 1000px) 800px,
           1200px"
    src="image-800.jpg"
    alt="Property photo"
    width="1200"
    height="800"
    loading="lazy">
</picture>
```

### Alt Text Best Practices

**Good examples:**
- ✅ "Modern three-bedroom apartment with city skyline view"
- ✅ "Lenox Management team reviewing property documents"
- ✅ "Residential property garden with outdoor seating area"

**Bad examples:**
- ❌ "image1"
- ❌ "IMG_20260204"
- ❌ "picture of building"

### Tools for Image Optimization

**Online:**
- Squoosh.app - https://squoosh.app/
- TinyPNG - https://tinypng.com/
- Compressor.io - https://compressor.io/

**Command Line:**
```bash
# Convert to WebP
cwebp -q 80 input.jpg -o output.webp

# Optimize JPG
jpegoptim --max=85 --strip-all image.jpg

# Optimize PNG
pngquant --quality=65-80 image.png
```

**WordPress Plugins:**
- Smush
- ShortPixel
- Imagify
- EWWW Image Optimizer

### Automated Workflow

1. **Before upload:**
   - Resize to appropriate dimensions
   - Compress images
   - Convert to WebP (keep original as fallback)
   - Add descriptive filename (e.g., `lenox-office-building.jpg`)

2. **During upload:**
   - Use descriptive alt text
   - Specify width and height attributes
   - Add lazy loading attribute

3. **After upload:**
   - Verify images load properly
   - Check mobile display
   - Test page load speed

### Performance Checklist

- [ ] All images compressed (< 100KB for most)
- [ ] WebP format with JPG fallback
- [ ] Lazy loading enabled for below-fold images
- [ ] Width and height attributes set
- [ ] Alt text for all images
- [ ] Responsive srcset for large images
- [ ] CDN delivery (optional but recommended)
