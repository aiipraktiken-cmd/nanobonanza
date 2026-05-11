# Handoff — NanoBonanza
_Last updated: 2026-03-19_

## Current State
AI image prompt workout presentation för Unconf 2026. 6 prompt-sektioner + intro/tips/bonus/outro. Single file: `index.html`. Deployed till Vercel via CLI (`nanobonanza.vercel.app`). Presenter-läget är inaktiverat — alla slides är upplåsta direkt för besökare. Senaste commit: `eca41ca` (pushad till GitHub).

## This Session
- **Bit.ly-länkar borttagna**: hero-sektionen (länk + etikett) + upplägg-sliden (url-text)
- **Presenter-mode inaktiverat**: `PRESENTER_MODE = false`, alla slides upplåsta, audience-polling borttagen
- **Visitor counter tillagd**: top-right, ljusgrå, räknar via Upstash `nb_views`
- **Referensbild borttagen** från Stockbilder-sektionen (tom placeholder)
- **Outro QR-layout fixad**: etiketter nu under respektive QR-kod, centrerat
- **Outro-text**: "Materialet kommer på epost" → "Fyll i och få xtra promptar"

## Open Issues
- **Collage-bakgrund saknas lokalt**: `images/collage/` finns inte i repot — svart bakgrund lokalt, men kan finnas på Vercel
- `images/bonus/image-03.png` saknas (LinkedIn-ram-kortet)

## Next Steps
1. Verifiera att collaget syns på `nanobonanza.vercel.app` — om inte, ladda upp `images/collage/`-mappen
2. Lägg till `images/bonus/image-03.png`
3. Deploya med `vercel --prod` om ytterligare ändringar görs

## Key Context
- **Source of truth**: `index.html` only — ingen build-step
- **Deploy**: `cd DEV/projects/NanoBonanza && vercel --prod`
- **Presenter-mode borttaget**: `?presenter=nanobonanza` fungerar inte längre
- **Upstash**: `nb_views` = besökarcounter (aktiv), `nb_unlock` används inte längre
- **PDF-länk**: `nanobonanza.vercel.app/NANOBONANZA-Unconf26-prompter.pdf`
