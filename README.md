# Order Flow Public Website

Minimal static public website for Meta Business and WhatsApp Business verification.

## Included files

- `index.html`
- `privacy.html`
- `contact.html`
- `styles.css`
- `.nojekyll`
- `CNAME.example` (optional template)
- `nginx.conf` (optional, for VPS)
- `Dockerfile` (optional, for VPS)

## 1. Publish on GitHub Pages

1. Create a **public** GitHub repository.
2. Upload these files to repository root:
   - `index.html`
   - `privacy.html`
   - `contact.html`
   - `styles.css`
   - `.nojekyll`
3. Commit and push to `main` branch.
4. In GitHub: `Settings` → `Pages`.
5. Set:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main`
   - **Folder**: `/ (root)`
6. Wait until the site is published at:
   - `https://<username>.github.io/<repo>/`

## 2. Use a custom domain (recommended for Meta verification)

1. In repository `Settings` → `Pages` → `Custom domain`, enter your domain (recommended `www.yourdomain.com`).
2. Save and wait for DNS check.
3. GitHub will manage `CNAME` automatically in most cases.

Alternative: manual `CNAME` file

1. Copy `CNAME.example` to `CNAME`.
2. Put your domain in `CNAME` (single line), for example:
   ```text
   www.yourdomain.com
   ```
3. Commit and push.

## 3. DNS setup

### Recommended (`www`)

Create DNS record:

- Type: `CNAME`
- Host: `www`
- Value: `<username>.github.io`

### Optional apex (`yourdomain.com`)

If you also need apex domain, use your DNS provider instructions for GitHub Pages (`A` records or `ALIAS/ANAME`) and keep `www` configured too.

## 4. HTTPS

1. In `Settings` → `Pages`, wait until certificate is issued.
2. Enable **Enforce HTTPS**.
3. Verify:
   - `https://www.yourdomain.com`
   - Pages open without certificate warnings.

## 5. Pre-submit checklist (Meta / WhatsApp)

- Public access without login
- Working links: Home, Privacy Policy, Contact
- No 404 on main pages
- No lorem ipsum or empty template text
- HTTPS enabled
- Contact details visible

## Notes

- `nginx.conf` and `Dockerfile` are kept as optional files if you later migrate from GitHub Pages to VPS.
- Before Meta submission, replace placeholder contact values with real business contacts.
