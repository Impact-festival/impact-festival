# Astro-implementering · 7. september 2026

## Leveret

Forsiden genskaber originalens hvide baggrund, sorte indrammede navigation,
røde logotype, Figtree/Climate Crisis, luftige hero og praktiske footer.
Fire nummererede indgange ligger efter hero og før program/billedindhold.
Trifolium-siden forklarer stedet, virksomhederne, faciliteterne og festivalens
forbindelse til arbejdsfællesskabet. Samme layout, typografi og komponenter anvendes.
MMD-kodestilen er anvendt med semantisk HTML, almindelig CSS og Astro-komponenter;
ingen klientframeworks eller ekstra JavaScript er nødvendige for navigationen.

## Filer

- Ændret: `src/pages/index.astro`, `astro.config.mjs` (dev-toolbar slået fra).
- Oprettet: `src/pages/trifolium.astro`, `src/layouts/Layout.astro`.
- Oprettet komponenter: `Header.astro`, `Footer.astro`, `ContentSection.astro`,
  `EntryPoints.astro` i `src/components/`.
- Oprettet: `src/styles/global.css`, `src/data/festival-content.ts`.
- Oprettet: `public/images/impact-logo.png`, `public/images/impact-2026.png`.
- Oprettet: denne leverancenote. Eksisterende Astro, lockfil og Netlify-opsætning bevaret.

## Indgange

| Indgang | Destination |
| --- | --- |
| Talks & Workshops | `#talks-workshops`, med links til officielle talks/workshops |
| Musik | https://www.trifolium-impactfestival.com/music-2026 |
| Location | `#location`, adresse, kontakt og kortlink |
| Hvad er Trifolium? | `/trifolium/` |

## Kilder og afgrænsninger

Gennemgået 7. september 2026:

- https://www.trifolium-impactfestival.com/ — identitet, logoer, menuer, seks billedopslag, dato og footer.
- https://www.trifolium-impactfestival.com/talks-2026
- https://www.trifolium-impactfestival.com/workshops-2026
- https://www.trifolium-impactfestival.com/music-2026
- https://trifo.dk/ — arbejdsfællesskab, faciliteter, kontakt og administrationsåbningstid.
- https://trifo.dk/pages/trifo-virksomheder — de tre navngivne virksomhedseksempler.
- https://trifo.dk/pages/kontorerogvaerkstedsfaelleskab — værkstedstyper.
- https://trifo.dk/pages/impact — festivalen som del af Trifoliums aktiviteter.

Festivalens adresse er 42; Trifoliums egen kontaktadresse er 42K. Begge er bevaret
med tydelig kontekst. Ingen transporttider, medlemsantal eller festivalåbningstider
er opfundet. Virksomhedsoversigten kan ændre sig; der linkes til den aktuelle kilde.

Billedområdet er et fast udvalg af seks officielle opslag, ikke hele originalens
16-opslagsfeed eller en live Instagram-integration. Det tomme lazy-load-område fra
originalens første render er ikke kopieret. Billederne hentes fra originalens CDN;
Google Fonts leverer skrifterne. Deres tilgængelighed afhænger af tredjepart.
Logoerne ligger lokalt. Rettigheder til offentlig genbrug af festivalmateriale er
ikke selvstændigt dokumenteret; afklar dette før offentlig lancering.
Der er ingen nye fotos/videoer af Trifolium eller opdigtede billedpladsholdere.

## Kontrol

- `ASTRO_TELEMETRY_DISABLED=1 npm run build`: bestået, to statiske sider.
- `git diff --check`: bestået.
- Begge sider visuelt inspiceret i Chrome ved 390, 768 og 1440 px.
- Intet konstateret vandret overflow; mobilindgange fordeles i to kolonner.
- Trifolium-indgang, tilbage-link og Location-anker afprøvet.
- About-menu åbnet med Enter; link til Trifolium fra menu afprøvet.
- Browserens opsamlede error-log var tom.
- Ingen separat lint/typecheck er konfigureret i package.json; build er ikke en
  erstatning for en fuld Astro-typecheck eller en komplet accessibility-audit.
- Ingen commit, push eller Netlify-publicering foretaget i denne implementering.

Lokalt: `ASTRO_TELEMETRY_DISABLED=1 npm run dev`, åbn http://localhost:4321/.
