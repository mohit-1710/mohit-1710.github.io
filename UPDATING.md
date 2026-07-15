# How to update this site

Everything lives in `index.html`. No build step — edit, commit, push to `main`, and
GitHub Pages redeploys in ~1 minute. The News and Publications sections have copy-paste
templates in the HTML comments above them; for Experience, Education, and Projects,
copy an existing `.entry` block.

## Add a news item (do this whenever something ships)

1. Open `index.html`, find `<section id="news">`.
2. Copy an existing `<li class="news-item">` block.
3. Paste it at the **top** of the `<ul class="news-list">` (newest first), edit the date + text.
4. Date format: **"Mon YYYY"** (3-letter month, e.g. `Sep 2026`). "Early/Late YYYY" is
   fine when the month is fuzzy. Longer date strings wrap awkwardly in the date column.
5. Keep it to one sentence. Link the artifact if it's public.

## Add a publication (the whole point of this site)

1. Find `<section id="publications">`. The comment above it has the full template.
2. Paste a `<li class="pub-item">` at the top of the `<ul class="pub-list">`, newest first.
3. Fill in: venue + year, title (linked to arXiv), authors (your name in `<strong>`),
   one-sentence description, and the arXiv / code / project links.
4. **Delete the `.pub-empty` placeholder `<li>`** once the first real paper is in.
5. Add a matching news item ("Paper accepted at X").

## When a paper exists, also do these once

- Make a Google Scholar profile, then uncomment the Scholar link in the header nav.
- Export a CV to `cv.pdf` in the repo root, then uncomment the CV link.

## Other maintenance

- **Photo:** replace `images/profile.jpg` (square, ≥400×400). Currently the GitHub avatar —
  swap in a real photo when you have one you like.
- **Role changes** (new job, graduation): update the header tagline, the About paragraph,
  and the Experience/Education sections together so they don't drift.
- **Every edit:** bump the "Last updated" date in the footer. It's the honesty signal
  academic pages live on — a stale date reads as an abandoned page.

## Standing rules for this page (from `/me/myself`)

- Research/AI framing only. **No web3 projects on this page** — that work lives on GitHub.
- Never open with stats. Story and stakes first (see `VOICE.md` in `/me/myself`).
- Honest status framing: no "in progress" claimed as shipped.
- BITS Pilani is the lead education credential.
