# Your Substack SEO site — quick start

This is a working Hugo site, already built and tested. It's set up to do
exactly one job: get your essays indexed by Google via short excerpts,
then send readers to Substack to read the rest and subscribe.

## What's in here

- `hugo.toml` — site config. Change `substackURL`, `title`, `tagline`,
  and `description` here first.
- `content/essays/switching-sides.md` — a worked example showing the
  front-matter pattern (title, date, description, substack_url, and the
  `<!--more-->` excerpt cutoff). Copy this file's structure for every
  new essay.
- `layouts/` — the three templates: homepage, essay archive, and single
  essay page. The single essay page (`layouts/essays/single.html`) is
  the one doing the canonical-tag + "Continue reading on Substack" work.
- `static/css/main.css` — the whole design. One file, no build step,
  easy to tweak.

## Design

A "declassified case file" aesthetic — aged paper background, a serif
display face (Fraunces) for headlines, a typewriter face (Special Elite)
for labels/dates/stamps, and a black "redaction bar" as the continue-
reading button that turns stamp-red on hover. Built to fit an
intelligence-history publication specifically, not a generic template.

## Adding a new essay

```
hugo new content essays/your-essay-slug.md
```

This uses `archetypes/essays.md` to scaffold the front matter for you.
Fill in `title`, `date`, `description` (155ish characters, this is your
Google snippet), and `substack_url` (the live URL of the matching
Substack post). Write your excerpt above the `<!--more-->` line —
that's the only part that gets published to your own site and indexed
by search engines. Everything below it is ignored unless you delete
`substack_url`, in which case the full `.Content` renders instead (use
this for the "publish full text once it's an older archive essay"
strategy, if you go that route later).

## Running it locally

```
hugo server
```

Then open http://localhost:1313 — live-reloads as you edit.

## Deploying

**GitHub Pages (free):**
1. Push this folder to a new GitHub repo.
2. Add a GitHub Actions workflow using `peaceiris/actions-hugo` (search
   "Hugo GitHub Pages Actions" for the current YAML — it's a copy-paste
   job, five minutes).
3. Point your custom domain at the repo in Settings → Pages.

**Netlify (also free, slightly less setup):**
1. Push to GitHub.
2. Connect the repo in Netlify, set build command to `hugo`, publish
   directory to `public`.
3. Netlify auto-detects Hugo and handles the rest.

## Before you go live

`hugo.toml` is already set up for the "Mikhail Garth" branding
(`baseURL` is set to `https://mikhailgarth.com/`, `substackURL` to
`https://mikhailgarth.substack.com`). Double-check both once you've
actually bought the domain and renamed the Substack publication, in
case either ends up slightly different from what's assumed here.

- Replace the example essay's `substack_url` with a real post, or
  delete the example file once you have real content.
- Submit the site to Google Search Console once it's live.
