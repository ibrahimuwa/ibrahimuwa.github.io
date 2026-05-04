# Academic Website — Dr. Muhammad Ibrahim

This repository hosts a Jekyll-based academic website at **`https://IbrahimUWA.github.io`** (when deployed).

## What's inside

```
website/
├── _config.yml              # Jekyll configuration
├── _layouts/default.html    # Site layout (header, footer, nav)
├── assets/css/style.css     # Styling
├── assets/img/              # Place your profile photo here as profile.jpg
├── index.md                 # About / home page
├── research.md              # Research themes and funding
├── publications.md          # Publications, datasets
├── teaching.md              # Teaching philosophy + UWA unit alignment
├── projects.md              # Active projects, grants, datasets, awards
├── cv.md                    # Online CV
├── Gemfile                  # Ruby dependencies (only needed for local preview)
└── README.md                # This file
```

## One-time deployment to GitHub Pages

> **Result:** your site will be live at `https://IbrahimUWA.github.io` (no custom domain needed).

### Step 1 — Add a profile photo

Drop a square photo (~600×600 px) named `profile.jpg` into `assets/img/`. The site will automatically pick it up. If no photo is added the page still renders cleanly without it.

### Step 2 — Create the GitHub repository

The repository **must be named exactly** `IbrahimUWA.github.io` (matches your GitHub username). Create it on github.com **as Public** and leave it empty (no README, no `.gitignore`).

### Step 3 — Push from this folder

Open Git Bash / PowerShell in this `website/` folder and run:

```bash
git init
git branch -M main
git add .
git commit -m "Initial academic site"
git remote add origin https://github.com/IbrahimUWA/IbrahimUWA.github.io.git
git push -u origin main
```

### Step 4 — Enable GitHub Pages

1. Go to `https://github.com/IbrahimUWA/IbrahimUWA.github.io` → **Settings** → **Pages**.
2. Under **Source**, select **Deploy from a branch**.
3. Branch: `main`, folder: `/ (root)`. Save.
4. Wait ~1–2 minutes. The site will appear at `https://IbrahimUWA.github.io`.

That's it — every future `git push` updates the site automatically.

## Updating content

All content is in **plain Markdown**. To add a new publication, open `publications.md` and copy an existing `<li>` entry. To update news on the home page, edit the **News** section of `index.md`. The navigation in the header is defined in `_layouts/default.html`.

## (Optional) Preview locally

You only need this if you want to see the site before pushing. Requires **Ruby 3.x**.

```bash
gem install bundler jekyll
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Custom domain (optional)

If you later buy a domain (e.g. `muhammadibrahim.au`), add a file `CNAME` containing the domain at the repo root and update DNS to point at GitHub Pages — full guide in GitHub's [Pages docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
