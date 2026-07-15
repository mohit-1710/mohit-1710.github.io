# How to update this site

Everything lives in `index.html`. No build step — edit, commit, push to `main`, and
GitHub Pages redeploys in ~1 minute. News and Publications have copy-paste templates
in the HTML comments around them; for Experience, Education, and Projects, copy an
existing `.card.item` block.

## Add a news item (do this whenever something ships)

1. Open `index.html`, find `<section class="shell section" id="news">`.
2. Copy an existing `<li>` block.
3. Paste it at the **top** of `<ul class="news-list">` (newest first), edit the date + text.
4. Date format: **"Mon YYYY"** (3-letter month, e.g. `Sep 2026`). "Early/Late YYYY" or
   plain "YYYY" is fine when the month is fuzzy.
5. Keep it to one sentence. Link the artifact if it's public.

## Post the first paper / preprint / technical note (the big one)

The Publications section is **fully commented out** until something real exists —
deliberate: no publication claims on the page before there's something to show.
The day the first one is posted:

1. Find the `PUBLICATIONS (hidden until the first one exists)` comment block in
   `index.html` and uncomment the whole `<section id="publications">`.
2. Fill the `pub-item` template: venue + year chip, title (linked), authors (your name
   in `<strong>`), one-sentence description, and the arXiv / code links.
3. Add a matching news item.
4. Create a Google Scholar profile, then uncomment the Scholar link in the Contact
   panel (template is already there, icon included). Same for `cv.pdf` when it exists.
5. Consider adding "Papers" to the sticky nav: `<a href="#publications">Papers</a>`.

## Other maintenance

- **Photo:** there is deliberately **no photo anywhere right now** (the GitHub avatar is
  an anime character — wrong tone for this page). Three things are wired together when a
  real headshot arrives; do all of them in one commit:
  1. Save it as `images/profile.jpg` (square, ≥400×400).
  2. In `index.html`, uncomment the `.profile-panel` block in the board section and
     remove the `span-full` class from `.identity-panel`.
  3. Restore the link-preview image in `<head>`:
     `<meta property="og:image" content="https://mohit-1710.github.io/images/profile.jpg">`
- **Role changes** (new job, graduation): update the identity-panel lead lines, the
  About paragraphs, and the Experience/Education cards together so they don't drift.
- **Every edit:** bump the "Last updated" date in the footer. A stale date reads as an
  abandoned page.

## Standing rules for this page (from Mohit, see also `/me/myself`)

- Safety/AI framing only. **No web3 projects on this page** — that work lives on GitHub.
- **Don't use the word "research" or claim papers/notes on the page until the first one
  is actually posted** (rule set 2026-07-16). The Publications section stays commented
  out until then.
- The safety workstream is described **without naming** any task, project, model, or
  partner — "frontier models", "safety guardrails", "checks and enforcement" is the
  approved vocabulary.
- Never open with stats. Story and stakes first (see `VOICE.md` in `/me/myself`).
- Honest status framing: no "in progress" claimed as shipped.
- BITS Pilani is the lead education credential.
