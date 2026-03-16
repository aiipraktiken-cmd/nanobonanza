# Handoff — NanoBonanza
_Last updated: 2026-03-16_

## Current State
AI image prompt workout presentation for Unconf 2026. 6 prompt sections + intro/upplägg/sektioner/tips/outro. Single file: `index.html`. Deployed to Vercel via GitHub (`aiipraktiken-cmd/nanobonanza`). Multiple unpushed changes from this session.

## This Session
- **Hero**: mixed-font title (11 Google Fonts), `--banana: #FFD234` accent, radial glow, pill kicker, staggered entry animations, padlet-shake on "Starta passet" → `goTo(1)`
- **Slide 2 (Upplägg)**: QR `images/qr_banan.png`, URL `https://bit.ly/NanoBonanza`, `→` checklist markers in yellow
- **Slide 3 (Sektioner)**: new 2×3 grid overview, Outfit thin (`font-weight:100 !important`), centered, "+Bonus" badge on Stockbilder cell
- **Slide 4 (Tips)**: 2-column layout (`display:block; columns:2`), 4 items/col, 3 real tips, banana emoji markers, yellow `<strong>` titles
- **Order**: Intro → Upplägg → **Sektioner** → **Tips** → prompts → Bonus → Outro
- **SLIDES array** updated to 18 slides; **UNLOCK_MAP**: `[2,3,5,7,9,11,13,15,16,17]`
- **Collage**: image-08 taller, 🫶🏻 emoji below title, `flex-direction:column` on outro
- **Images**: all `.jpeg` → `.png` (prod, stock); new collage/kommunikation/reklam/bonus images added
- **Last push**: commit `502aadb` — current session changes NOT yet pushed

## Open Issues
- Tips slide has 3 placeholder "Xxxx" items (items 6–8) — needs real content
- `font-weight: 100` on cgo-cells may still render as heavier weight in some browsers (added `!important`)
- **Unpushed changes** — run `git commit && git push`

## Next Steps
1. `git commit && git push` to deploy all session changes
2. Fill 3 remaining Tips placeholders with real content
3. Verify Sektioner grid renders thin in browser
4. Add any remaining collage images to `images/collage/`

## Key Context
- **Source of truth**: `index.html` only — one file, no build step
- **SLIDES array** (line ~2025): 18 slides — `['intro','upplagg1','sektioner','oversikt','p1-intro','p1',...]`
- **UNLOCK_MAP** (line ~2021): `[2,3,5,7,9,11,13,15,16,17]` — audience locked to slide 2 on load
- **CSS scoping**: section-intros use `#[id]`-scoped overrides, never touch base `.masonry`
- **GitHub**: push to `aiipraktiken-cmd/nanobonanza` → Vercel auto-deploys
