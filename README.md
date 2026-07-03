# Srujan Devulapalli — Portfolio

A static, dependency-free portfolio (HTML/CSS/JS): a dark, professional single-page
layout with a bold hero (name, role pills, resume/contact CTAs, social icons),
followed by About, Skills, Experience, Projects, Certifications, and Contact sections.

## Files
- `index.html` — all content/markup
- `styles.css` — design system (colors, type, layout)
- `script.js` — mobile nav toggle, scroll reveal
- `vercel.json` — minimal Vercel config (clean URLs)

## Before you deploy — replace these placeholders
1. **Resume PDF** — the nav and hero "Download Resume" buttons link to `resume.pdf`.
   Add your actual resume PDF to this folder and name it `resume.pdf` (or update the
   `href` in `index.html` to point elsewhere).
2. Search `index.html` for `href="#"` — there are project GitHub links and LinkedIn/
   GitHub/LeetCode/HackerRank links in the **Contact** section to update with your
   real URLs.

Email and phone are already wired to `mailto:` / `tel:` links from your resume.

## Deploy to Vercel

### Option A — Vercel CLI (fastest)
```bash
npm i -g vercel
cd portfolio
vercel
```
Follow the prompts (link/create project, accept defaults). Vercel auto-detects
this as a static site — no build step needed.

### Option B — GitHub + Vercel dashboard
```bash
cd portfolio
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin <your-empty-github-repo-url>
git push -u origin main
```
Then on [vercel.com](https://vercel.com):
1. **Add New → Project**
2. Import the GitHub repo
3. Framework Preset: **Other** (static)
4. Leave Build Command / Output Directory blank
5. **Deploy**

Every future `git push` to `main` auto-redeploys.

## Local preview
Just open `index.html` in a browser, or run a local server:
```bash
npx serve .
```

## Customizing
- Colors/fonts: edit the `:root` token block at the top of `styles.css`
- Typed terminal command: edit the `command` variable in `script.js`
- Add a project: copy a `.project-card` block in `index.html` and update its
  eyebrow, title, description, metrics, and tags
