# Netlify deploy bundle (`netlify-deploy/`)

This folder is what many Netlify sites use as the **publish directory**. It is **not** auto-synced with `../v3/` — you must copy updates over when help pages, images, or CSS change.

### Before each deploy (from repo root `snap-website/`)

```bash
# Help docs, templates, and new pages (e.g. google-admin.html)
cp -R v3/help/* netlify-deploy/help/

# Images (screenshots, icons — required for help pages to load)
cp -R v3/images/* netlify-deploy/images/

# Sitemap (includes /help/ URLs)
cp sitemap.xml netlify-deploy/sitemap.xml
```

Then upload **this folder** (or push to git if Netlify builds from it).

**Why:** Edits are usually made in `v3/`. If you only upload an old `netlify-deploy/` zip, you will miss **Google Admin Setup**, **Custom Sites** CSV sections, new images, etc.

---

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
Upload the entire `v3` folder as the root of your Netlify site.

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
