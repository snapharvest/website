# Snap for Harvest - V3 Website

This folder contains the complete V3 version of the Snap for Harvest website with the "Editorial-Industrial" design aesthetic.

## What's Included

- ✅ **index.html** - Homepage with dark hero, marquee strip, features, and CTA
- ✅ **pricing.html** - Pricing page (free forever)
- ✅ **privacy.html** - Privacy policy
- ✅ **terms.html** - Terms of service
- ✅ **css/style.css** - Complete V3 stylesheet (Bricolage Grotesque + DM Sans)
- ✅ **images/** - All logos and assets
- ✅ **js/** - Empty folder (JavaScript is inline in HTML)

## Design Features

- **Dark hero section** with asymmetric layout
- **Scrolling marquee strip** showing compatible sites with logos
- **Horizontal feature rows** with large background numbers
- **Mobile hamburger menu** with smooth animations
- **Scroll reveal animations** for progressive disclosure
- **Consistent V3 navigation** across all pages
- **Editorial-Industrial aesthetic** with Bricolage Grotesque font

## How to View

### Local Development
```bash
# From the snap-website folder
python3 -m http.server 8080

# Then visit:
http://localhost:8080/v3/
```

### Deploy to Netlify
This is the production-ready folder. Upload this entire folder, or set your Netlify publish directory to `v3`.

## Folder Structure
```
v3/
├── index.html
├── pricing.html
├── privacy.html
├── terms.html
├── css/
│   └── style.css
├── images/
│   ├── logo.png
│   ├── google-calendar-icon.png
│   ├── notion-icon.png
│   ├── jira.png
│   ├── hubspot.png
│   ├── Googledoc.png
│   ├── Googlemeet.png
│   ├── spiceworks-icon.png
│   ├── freshservice.png
│   ├── atlassian.png
│   └── ... (screenshots and other assets)
└── js/
    └── (empty - JS is inline)
```

## V1 vs V3

- **V1** lives at the root (`index.html`) - lighter, card-based design
- **V3** lives in this folder - darker, editorial, more distinctive

Both are fully functional and can be deployed independently.
