# Handoff — NanoBonanza
_Last updated: 2026-03-14_

## Current State
Workshop presentation site for AI image prompting. 17 slides, 6 prompt sections each with section-intro slide + cluster slide. p1 (Studio) and p2 (Reklam) fully populated. Sections prod/stock/reklam/viral have real images but placeholder prompts. Deployed via Vercel (GitHub push = auto-deploy).

## This Session
- **All section-intro slides** converted to CSS Grid masonry: `display: grid; grid-template-columns: 1.65fr 1fr; grid-template-rows: 1fr 1fr; height: calc(100vh - 290px)`
- **Hero layout**: image-01 spans both rows (big left), image-02 + image-03 stack right
- **`object-fit: contain`** — images show in full, no crop (dark bg fills gaps)
- **`overflow: hidden` on `.section-intro`** — fixed overflow bleeding into next slide (root cause: CSS `columns` + `max-height` = extra columns; fixed by switching to CSS `grid`)
- **p1 hover effect**: `images/p1/image-03.png` → crossfades to `images/p1/image-03-02.png` on hover (`.has-hover` class)
- **Font-weight fix**: `.rail-brand h1`, `.bonus-title`, `.collage-title`, `.outro-card h3` → all `font-weight: 100`
- **Image fix**: p1 uses `image-02.png` (not .jpg); reklam fixed broken `image-04.jpg` ref

## Open Issues
- prod/stock/reklam/viral clusters still have placeholder/English prompts
- Slide 3 (`#upplagg1`) has `www.xxx.sd` URL + placeholder QR code
- `NanoBonanza.html` (old version) still in repo — can delete
- Changes not committed to git yet

## Next Steps
1. `git add -p && git commit && git push` → Vercel deploy
2. Delete `NanoBonanza.html`
3. Populate prod cluster with real Swedish prompts (check `images/prod/produkt-prompt.rtf`)
4. Same for stock, reklam, viral — check `sourcefile/` and `images/*/` for RTF/ODT files
5. Fix `#upplagg1` Vercel URL + QR code

## Key Context
- **Always sync**: `cp overview.html index.html` after every edit
- **CSS bug pattern**: `columns:` + `max-height` → extra columns. Always use `display: grid` for fixed-height masonry
- **Masonry CSS**: `.section-intro-imgs.masonry` — hero layout applies to ALL 6 section-intro slides
- **Hover images**: only p1/image-03 has a hover variant (image-03-02.png); pattern reusable for others
- **GitHub**: push to `aiipraktiken-cmd/nanobonanza` → Vercel auto-deploys
