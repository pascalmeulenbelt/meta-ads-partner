# Unison · Toegang tot je Meta ads

Statische one-page site (het stappenplan waarmee een klant Unison toegang geeft tot z'n Meta ads). Alles zit in `index.html`: HTML, CSS en het logo staan inline. Het enige externe is het lettertype Syne, dat via Google Fonts laadt.

## Live zetten op Vercel

Je hebt geen build-stap nodig. Kies één van de manieren hieronder.

### Manier 1 — Vercel CLI (snelst, zonder Git)

1. Installeer de CLI (eenmalig): `npm i -g vercel`
2. Ga in de terminal naar deze map: `cd unison-site`
3. Preview-deploy: `vercel`
4. Naar productie: `vercel --prod`

De eerste keer vraagt Vercel om in te loggen en of je een nieuw project wilt aanmaken. Bevestig de standaardopties (geen framework, output = deze map).

### Manier 2 — Via GitHub

1. Zet deze map in een GitHub-repository (push `index.html` en `vercel.json`).
2. Ga naar https://vercel.com/new en importeer de repo.
3. Framework Preset: **Other** (geen build). Klik **Deploy**.

Elke push naar de repo zet automatisch een nieuwe versie live.

## Aanpassen

Alle tekst en opmaak staat in `index.html`. Zoek op de tekst die je wilt wijzigen en pas 'm aan; er is geen compileerstap.

## Eigen domein

In het Vercel-dashboard onder **Settings → Domains** koppel je bijvoorbeeld `meta-toegang.unison.nl` aan het project.

## Let op

- Het lettertype Syne komt van Google Fonts. Zonder internet valt de site terug op een systeem-sans; de opmaak blijft verder heel.
- Wil je de fonts zelf hosten (geen externe afhankelijkheid), zet dan de Syne `.woff2/.ttf`-bestanden in een `/fonts`-map en vervang de Google Fonts `<link>` in `index.html` door lokale `@font-face`-regels.
