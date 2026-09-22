# moleesh.github.io

Personal portfolio site for **A Moleesh** — Senior Software Engineer & AI Generalist.

Live at: https://moleesh.github.io

## What's here

A single-page, static HTML/CSS/JS site (no build step, no framework) covering:

- Hero intro with a typewriter tagline and animated circuit-board canvas background
- About, experience timeline, AI engineering highlight (KIMMY), and skills
- Featured projects (BabuScales, HireWise, FirstDay, VaultBill)
- **Live GitHub repositories**, fetched client-side from the GitHub REST API (`/users/moleesh/repos`) with search/filter
- Resume ([resume.pdf](resume.pdf)) and contact links (email, phone, GitHub, LinkedIn)

## Stack

Plain HTML5, CSS3 (custom properties, no framework), and vanilla JS. Fonts via Google Fonts (Space Grotesk, JetBrains Mono).

## Deployment

Deployed via GitHub Actions (`.github/workflows/deploy.yml`) using the official Pages actions
(`actions/configure-pages`, `actions/upload-pages-artifact`, `actions/deploy-pages`) — every push to
`master` rebuilds and republishes the site. No Jekyll processing (`.nojekyll` present); files ship as-is.

Repo Settings → Pages → Source must be set to **GitHub Actions** for the workflow to publish.

## Local preview

Any static file server works, e.g.:

```bash
python -m http.server 8080
```

Then open `http://localhost:8080`.

## Updating the resume

Replace [resume.pdf](resume.pdf) with the latest export and commit — the "View Resume" button and
footer link point directly at that file.
