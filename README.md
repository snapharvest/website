# Snap for Harvest Website

Official website for the Snap for Harvest Chrome extension. Editorial-Industrial design with comprehensive help documentation.

## Structure

```
snap-website/
└── v3/                    # Production website (deploy this folder)
    ├── index.html
    ├── pricing.html
    ├── privacy.html
    ├── terms.html
    ├── _headers           # Netlify security headers
    ├── _redirects         # URL redirects
    ├── robots.txt         # Search engine rules
    ├── sitemap.xml        # SEO sitemap
    ├── css/
    │   └── style.css
    ├── images/            # Logos, screenshots, icons
    ├── help/              # Complete help documentation
    │   ├── index.html
    │   ├── getting-started.html
    │   ├── google-calendar.html
    │   ├── notion.html
    │   ├── custom-sites.html
    │   ├── google-admin.html
    │   ├── faq.html
    │   ├── troubleshooting.html
    │   ├── admin-policy-template.json
    │   └── site-import-template.csv
    └── internal/          # Private testing paths (non-indexed)
        └── enterprise-test/
```

## Design Features

- **Dark hero section** with asymmetric layout
- **Scrolling marquee strip** showing compatible sites with logos
- **Horizontal feature rows** with large background numbers
- **Mobile hamburger menu** with smooth animations
- **Scroll reveal animations** for progressive disclosure
- **Editorial-Industrial aesthetic** with Bricolage Grotesque font
- **Complete help center** with admin guides and templates

## Local Development

```bash
# From the snap-website folder
cd v3
python3 -m http.server 8080

# Then visit:
http://localhost:8080/
```

## Deployment to Netlify

### Option 1: Upload via Netlify UI (Recommended)
1. Drag and drop the **v3/** folder to Netlify
2. Site will be live immediately

### Option 2: Deploy from GitHub
1. Connect your GitHub repo to Netlify
2. Set **Publish directory** to: `v3`
3. No build command needed (static HTML)

## Key Features

- ✅ **SEO optimized** with sitemap and meta tags
- ✅ **Security headers** configured for production
- ✅ **Private enterprise test path** for internal .crx hosting
- ✅ **Help documentation** integrated with extension
- ✅ **CSV/JSON templates** for user and admin import
- ✅ **Mobile responsive** across all pages
- ✅ **Fast loading** with no dependencies

## Links

- **Live site:** https://snapharvest.xyz
- **Chrome extension:** https://chromewebstore.google.com/detail/snap-for-harvest/cpdkkbooojkbmadoihipnceeembflfic
- **Help center:** https://snapharvest.xyz/help/
