# imananvari.tech

Personal site for Iman Anvari. Plain static HTML/CSS, no build step.

## Files

- `index.html` — the page (intro, projects, about, contact)
- `styles.css` — styling, with automatic dark mode
- `CNAME` — custom domain for GitHub Pages

## Preview locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy with GitHub Pages

1. Create a new public repo on GitHub (e.g. `imananvari.tech`).
2. Push this folder:
   ```bash
   git add -A
   git commit -m "Initial site"
   git remote add origin git@github.com:<your-username>/imananvari.tech.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Build and deployment**, set source to *Deploy from a branch*, branch `main`, folder `/ (root)`.
4. Under **Custom domain**, enter `imananvari.tech` and save. Enable **Enforce HTTPS** once the certificate is ready.
5. At your domain registrar, add DNS records:
   - `A` records for `@` pointing to GitHub Pages IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www` pointing to `<your-username>.github.io`

DNS changes can take a few minutes to a few hours to propagate.

## Adding a project

Copy one `<article class="card">` block in `index.html` and fill in the title, description, and link. Later, each project can get its own folder (e.g. `/projects/diagram-museum/`) with its own `index.html`.
