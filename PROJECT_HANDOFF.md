# Handoff — NanoBonanza
_Last updated: 2026-03-16_

## Current State
Workshop presentation site for AI image prompting. 6 prompt sections. All section-intro grids have custom per-section CSS (scoped by `#id`). `overview.html` is the source of truth — `index.html` is kept in sync via `cp overview.html index.html`. Changes from this session are NOT yet committed.

## This Session
- **red-intro Reklam grid fixed** (`overview.html` + `index.html`): replaced fixed-height CSS grid + `object-fit:cover` with flex layout, natural `height:auto` on all images, 46% left / 54% right split (mathematically correct for natural aspect ratios to align heights)
- **HTML structure changed**: wrapped image-02 + image-03 in `<div class="red-stack">` for flex stacking; image-03 (landscape) now on top, image-02 (square) on bottom — matches reference
- **`NanoBonanza.html` deleted** (was dead file, confirmed by user)
- **Wasted work**: all edits this session initially went to wrong file (`NanoBonanza.html`) — discovered late

## Open Issues
- **Changes NOT committed** — `git add overview.html index.html && git commit -m "fix: reklam grid natural aspect ratios" && git push`
- prod/stock/viral clusters still have placeholder/English prompts
- Slide 3 (`#upplagg1`) has `www.xxx.sd` URL + placeholder QR code

## Next Steps
1. `git commit && git push` to deploy Reklam grid fix
2. Populate Reklam cluster with real Swedish prompts (`sourcefile/` has source files)
3. Fix `#upplagg1` Vercel URL + QR code
4. Same treatment for stock/viral section-intro grids if needed

## Key Context
- **Source of truth**: `overview.html` — always edit this, then `cp overview.html index.html`
- **CSS scoping**: each section-intro has `#[id] .section-intro-imgs.masonry` override — never edit base `.masonry`
- **red-intro HTML**: now uses `.red-stack` wrapper div inside `.section-intro-imgs.masonry` — unique structure vs other sections
- **GitHub**: push to `aiipraktiken-cmd/nanobonanza` → Vercel auto-deploys
