# PETZIO • GitHub Pages Site

This folder is ready to upload to a **GitHub Pages** repository.

## Quick Deploy (Project Pages)
1. Create a new repo (e.g. `petzio-site`) on GitHub.
2. Upload all files in this folder to the repo root.
3. In **Settings → Pages**, set **Source: Deploy from branch**, **Branch: main / root**.
4. Add a file named `CNAME` with this single line: `petzio.ae` (already included).
5. Add DNS in Tasjeel (see below).

## Repo Option (User/Org Pages)
Alternatively, name the repo `<your-username>.github.io` and push the files. Skip Pages settings (auto-enabled). CNAME still needed for the custom domain.

## DNS Setup at Tasjeel (for apex `petzio.ae` + `www`)
Add these **A records** for the apex (host `@`):
- 185.199.108.153
- 185.199.109.153
- 185.199.110.153
- 185.199.111.153

Add a **CNAME** for `www`:
- Host: `www` → Value: `<your-username>.github.io`

(Advanced) You can alternatively point `www` to this repo's GitHub Pages subdomain if shown in the Pages settings.

## HTTPS
After DNS propagates, enable **"Enforce HTTPS"** in GitHub Pages (Settings → Pages).

## Edit Content
- Main page: `index.html`
- Styles: `styles.css`
- Update phone, address, prices, images under `/assets/img`

## Notes
- `/.nojekyll` prevents Jekyll processing.
- `404.html` is served automatically for unknown routes.
- `robots.txt` and `sitemap.xml` help search engines.
