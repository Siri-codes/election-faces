# election-faces

Project page for *Facial-Impression Judgments of Multimodal Large Language Models Predict Election Outcomes* (SocialAgent @ NeurIPS 2026).

Live site: https://siricodes.github.io/election-faces/

## Files
- `index.html` — the landing page
- `paper.pdf` — the paper
- `poster.pdf` — the poster **(add this file before publishing — see below)**
- `assets/teaser.png` — Figure 1 teaser

## Add your poster
Drop your poster in this folder named exactly `poster.pdf`. The "Poster (PDF)" button links to it.
If you'd rather use a different name, edit the `href` in `index.html`.

## Publish to GitHub Pages (one time)
From inside this folder:

```bash
git init -b main
git add .
git commit -m "Project page: paper + poster"
gh repo create siricodes/election-faces --public --source=. --push
# then enable Pages on the main branch root:
gh api -X POST repos/siricodes/election-faces/pages -f source='{"branch":"main","path":"/"}'
```

No `gh` CLI? Create an empty public repo named `election-faces` on github.com, then:

```bash
git init -b main && git add . && git commit -m "Project page: paper + poster"
git remote add origin https://github.com/siricodes/election-faces.git
git push -u origin main
```
Then on github.com: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `/ (root)` → Save.**

The site appears at https://siricodes.github.io/election-faces/ within a minute or two.

## Updating later
Replace `paper.pdf` (or `poster.pdf`), then:
```bash
git add . && git commit -m "Update" && git push
```
