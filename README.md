# SLM-2 Coming Soon

Static HTML/CSS coming soon page for [https://slm-2.com/](https://slm-2.com/).

## Buttons

| Button | Behavior |
|--------|----------|
| **Get Commercial Proposal** | Disabled — coming soon (no link) |
| **Book Chores Service** | Redirects to [https://chores.slm-2.com/](https://chores.slm-2.com/) |

## Local preview

Open `index.html` in a browser, or run:

```bash
npx serve .
```

## Push to GitHub

From this folder, after [GitHub CLI](https://cli.github.com/) login:

```bash
gh auth login
gh repo create slm-2-coming-soon --public --source=. --remote=origin --push
```

If the remote already exists (from a prior setup):

```bash
git push -u origin main
```

Repo URL: `https://github.com/aliaqib13/slm-2-coming-soon`

## Deploy to Vercel

1. Push this repo to GitHub (see above).
2. In [Vercel](https://vercel.com), click **Add New Project** and import the repo.
3. Framework Preset: **Other** (static HTML).
4. Build Command: leave empty.
5. Output Directory: `.` (root).
6. Deploy.

## Connect slm-2.com

In the Vercel project → **Settings** → **Domains**, add:

- `slm-2.com`
- `www.slm-2.com`

At your domain registrar, set DNS (Vercel may show exact values in the Domains UI):

| Type | Name | Value |
|------|------|-------|
| A | `@` | `76.76.21.21` |
| CNAME | `www` | `cname.vercel-dns.com` |

**Important:** Do not remove the existing `chores` subdomain CNAME — [chores.slm-2.com](https://chores.slm-2.com/) stays on its current deployment.

## Enable Commercial Proposal later

Replace the disabled button in `index.html` with a link when ready:

```html
<a href="YOUR_URL_HERE" class="btn btn-primary">Get Commercial Proposal</a>
```

## Stack

- Plain HTML + CSS (no framework)
- Inter font via Google Fonts
- Brand colors: navy `#0F172A`, green `#22C55E`
