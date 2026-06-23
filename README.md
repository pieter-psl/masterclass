# Masterclass · AI: Proosten op de toekomst

Interactieve webonderdelen voor het New Day tenant event (PSL Consulting).
Statische site, te hosten op GitHub Pages.

## Inhoud

- `index.html` — landingspagina met drie knoppen (AI-check, meedoen, beamer).
- `quiz.html` — persoonlijke AI-check (lokaal, geen account nodig).
- `poll.html` — live poll, Kahoot-stijl. Eén bestand is zowel het beamer-scherm als de stem-pagina.
- `.nojekyll` — laat GitHub Pages de bestanden ongewijzigd serveren.

## Online zetten via GitHub Pages

1. Maak op GitHub een repository met de naam `masterclass`.
2. Upload de bestanden uit deze map naar de repository.
3. Ga in de repository naar **Settings → Pages**.
4. Bij **Source** kies je de branch `main` en map `/ (root)`. Save.
5. Na een minuut staat de site op `https://JOUW-NAAM.github.io/masterclass/`.

## Live poll instellen (eenmalig, ongeveer 10 minuten)

De live poll heeft een gratis realtime-database nodig (Firebase).

1. Ga naar https://console.firebase.google.com en log in met Google.
2. Add project, naam bijvoorbeeld `newday-poll`, Analytics mag uit.
3. Build → Realtime Database → Create Database → locatie `europe-west1` → start in **test mode**.
4. Project settings → onderaan bij Your apps → web-icoon `</>` → registreer de app.
5. Kopieer het `firebaseConfig`-blok en plak het in `poll.html` (duidelijk gemarkeerd bovenin het script).
6. Commit en push de wijziging.

## Gebruik op de avond

- Beamer: open `.../masterclass/poll.html?host`
- Telefoons: scannen de QR op het scherm, of gaan naar de site en typen de zaalcode.
- Jij klikt "Volgende vraag"; de zaal stemt; de balkjes lopen live mee.

De vragen, opties en discussieregels staan bovenin `poll.html` en `quiz.html` in nette lijstjes en zijn zo aan te passen.

---
PSL Consulting · Pieter Slingerland · AI Leadership & Digitale Transformatie
