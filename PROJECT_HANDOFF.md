# Handoff — NanoBonanza
_Last updated: 2026-03-11_

## Current State
Workshop presentation site for "Nano Bonanza" — an AI image prompt workout with 6 sections (Porträtt studio/miljö, Produkt, Stockbilder, Redaktionellt, Viralt). Built as a single HTML file (`index.html` = copy of `overview.html`), deployed to Vercel via GitHub repo `aiipraktiken-cmd/nanobonanza`. Slide nav with prev/next buttons, collapsible rail, copy-to-clipboard prompts.

## This Session
- Set up project: git init, `.gitignore`, initial commit, pushed to `github.com/aiipraktiken-cmd/nanobonanza`
- `index.html` = `overview.html` (always keep in sync via `cp overview.html index.html`)
- Removed Slide 5 (`#prompt-ovr`) — the prompt overview grid
- Added 6 section intro slides (`#p1-intro`, `#p2-intro`, `#prod-intro`, `#stock-intro`, `#red-intro`, `#viral-intro`) before each cluster — full-viewport, centered title + 2 portrait image placeholders
- Updated rail nav (17 entries), `#oversikt` grid links, JS `SLIDES` array
- Hero: enlarged "Nano Bonanza" title (`clamp(4.4rem, 9vw, 6.8rem)`), added animated banana background (19 emoji + 4 Lottie instances)
- Lottie animations: 2 URLs used, loaded via `@dotlottie/player-component` CDN script in `<head>`
- Centered `#upplagg1` and `#upplagg2` slides
- All heading titles changed to `font-weight: 100` (Outfit Thin)

## Open Issues
- Section intro slides have placeholder image divs — real images not yet added
- URL on slide 3 (`#upplagg2`) is still `www.xxx.sd` — needs real Vercel URL
- QR code on slide 3 is a placeholder — needs real QR image
- `NanoBonanza.html` (old version) still in repo — can be deleted

## Next Steps
1. Add real images to all 6 section intro slides (`#p1-intro` through `#viral-intro`)
2. Update URL + QR code on slide 3 with the live Vercel URL
3. Push latest changes to GitHub to trigger Vercel redeploy
4. Delete `NanoBonanza.html` if no longer needed

## Key Context
- **Always sync**: after editing `overview.html` run `cp overview.html index.html`
- **Slide system**: JS `SLIDES` array in `overview.html` must match all `data-s` sections in order
- **Lottie**: `<script type="module" src="https://unpkg.com/@dotlottie/player-component@latest/...">` in `<head>`
- **Banana opacity**: `.hero-bananas span { opacity: .07 }` — user wants this kept
- **GitHub auth**: local git is authenticated as `mariadebahia`, repo is under `aiipraktiken-cmd` — need to `gh auth login` as `aiipraktiken-cmd` before pushing
