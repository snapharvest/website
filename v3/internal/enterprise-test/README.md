# Enterprise extension hosting (testing only)

This folder is for **temporary** hosting of a packaged Chrome extension (`.crx`) so you can use **Google Admin → Add by extension ID → From a custom URL**.

- **Not linked** from the public website or help docs.
- **Discouraged for search engines** via `robots.txt` and `X-Robots-Tag` (see repo `_headers`).
- **Remove** this file and the `.crx` from the server when testing is done.

## URLs (depends how you deploy)

**Important:** Browsing the **folder** URL (`…/enterprise-test/`) only works after you deploy an `index.html` in this folder (otherwise Netlify shows 404). The URL you paste into **Google Admin** must be the **full path to the `.crx` file**, not the folder.

If **Netlify publish directory = `v3`** (site root is this folder):

- Example: `https://snapharvest.xyz/internal/enterprise-test/snap-for-harvest-test.crx`

If **publish directory = `netlify-deploy`** (or whole `snap-website`):

- Example: `https://snapharvest.xyz/internal/enterprise-test/snap-for-harvest-test.crx`

If **publish directory = repo root** (whole `snap-website` without using netlify-deploy):

- Example: `https://snapharvest.xyz/v3/internal/enterprise-test/snap-for-harvest-test.crx`

Use whichever matches your live site after deploy.

## Steps

1. **Stable extension ID**  
   Keep a fixed `key` in `manifest.json` so the ID does not change between builds.

2. **Package the extension**  
   In Chrome: `chrome://extensions` → Developer mode → **Pack extension** → note the `.crx` path.

3. **Upload**  
   Upload the `.crx` into **this folder** on your host (same path as above).  
   Do **not** commit `.crx` to git (see `.gitignore`).

4. **Google Admin**  
   Extension ID + **From a custom URL** + the full HTTPS URL to the `.crx`.

5. **When done**  
   Delete the `.crx` from hosting, remove the Admin app-by-ID entry if needed, and optionally remove this folder.

## Content-Type

Your host should serve `.crx` over **HTTPS**. If Admin or Chrome complains, set MIME type to `application/x-chrome-extension` for `.crx` (Netlify: add a `_headers` rule in publish dir if needed).
