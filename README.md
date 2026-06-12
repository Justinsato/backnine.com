# Backnine Trades — backninetrades.com

Client-facing marketing site for Backnine Trades, a third-party R&M operating company serving SF Bay Area multifamily, plus the internal brand package.

## Contents

| File | Purpose |
|------|---------|
| `index.html` | Client-facing marketing homepage: services, team, process, compliance, client portal (work order + proposal forms), FAQ |
| `package.html` | Internal brand package index (formerly the homepage) |
| `flyer.html` | One-page sales flyer for prospective 3rd-party PMs |
| `naming.html` | Naming decision record — shortlist, domains, risk assessment |
| `logos.html` | Logo lockup options (selected mark + alternates) |

The homepage was rebuilt 2026-06-12 against the competitive survey in `../docs/Competitive_Survey_SF_Handyman_CM_2026-06-12.md`. Portal forms route via mailto to info@backninetrades.com until a backend exists. Do not add license numbers, insurance limits, phone numbers, testimonials, or photos until they are real.

## Local preview

Open `index.html` in any browser. No build step required — pure static HTML/CSS/SVG.

```bash
open index.html
```

## Deploy to Vercel

This is a zero-config static site. No `package.json`, no framework — Vercel will serve it directly.

### One-time setup

1. **Push to GitHub** (or GitLab/Bitbucket):
   ```bash
   git init
   git add .
   git commit -m "Initial Backnine brand package"
   gh repo create backnine-site --public --source=. --push
   ```

2. **Connect to Vercel**:
   - Go to https://vercel.com/new
   - Import the `backnine-site` repo
   - Framework preset: **Other** (static)
   - Output directory: leave blank (root)
   - Click **Deploy**

3. **Custom domain** (optional):
   - In Vercel project settings → Domains, add `backninetrades.com`
   - Update DNS at your registrar to point to Vercel

### Subsequent updates

```bash
git add .
git commit -m "Update flyer copy"
git push
```

Vercel auto-deploys on every push to `main`.

## Print to PDF

The brand-package documents are letter-size and print clean. From any open file: `Cmd+P` → **Save as PDF**.
