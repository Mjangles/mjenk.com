# Launching mjenk.com on GitHub Pages

Plain HTML, CSS and images. No build step. This folder is the whole site.

## 1. Put it on GitHub
The site lives in a GitHub repository. Every push to the `main` branch republishes the site.

## 2. Turn on GitHub Pages
In the repository: **Settings → Pages → Build and deployment**
- Source: **Deploy from a branch**
- Branch: **main**, folder **/ (root)** → Save

After a minute or two the site is live at `https://<username>.github.io/<repo>/`.

## 3. Connect mjenk.com
The `CNAME` file already tells GitHub the site's domain is `www.mjenk.com`.

Add these DNS records where the domain is registered (likely Squarespace: **Domains → mjenk.com → DNS settings**), replacing the old Squarespace website records:

| Type  | Host | Value |
|-------|------|-------|
| CNAME | www  | `<username>.github.io` |
| A     | @    | 185.199.108.153 |
| A     | @    | 185.199.109.153 |
| A     | @    | 185.199.110.153 |
| A     | @    | 185.199.111.153 |

Then in **Settings → Pages**, wait for the DNS check to pass and tick **Enforce HTTPS**.

## 4. Retire Squarespace
Once mjenk.com shows the new site, cancel the Squarespace **website** plan. Keep the **domain** registration if it's held there.

## What's in this folder
- `index.html`, `about.html`, `work/` – the pages
- `styles.css` – all styling
- `images/` – photos and the social preview card (`og-image.jpg`)
- `loyalty-crm/`, `customer-insight/`, `the-chain/`, `formative/` and the other short folders – redirect old Squarespace links to the new pages
- `404.html` – shown for any missing page
- `CNAME` – the custom domain for GitHub Pages
- `sitemap.xml`, `robots.txt` – for search engines
