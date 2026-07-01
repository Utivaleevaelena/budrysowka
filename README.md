# Budrysówka — wdrożenie na Vercel

Statyczna strona (HTML + JS, bez build-stepu). Gotowa do wgrania na Vercel.

## Struktura
- `index.html` — strona (punkt wejścia)
- `support.js`, `image-slot.js` — runtime komponentów
- `assets/` — zdjęcia (hero, separator)
- `vercel.json` — konfiguracja (cache, nagłówki bezpieczeństwa)
- `robots.txt`, `sitemap.xml` — SEO

## Wdrożenie

### Wariant A — przez panel Vercel
1. Wejdź na https://vercel.com/new
2. Zaimportuj repozytorium lub przeciągnij folder projektu.
3. Framework Preset: **Other** (bez build command, output = katalog główny).
4. Deploy.

### Wariant B — przez CLI
```bash
npm i -g vercel
vercel        # podgląd
vercel --prod # produkcja
```

## Po wdrożeniu
- Podmień domenę `budrysowka.pl` w `sitemap.xml`, `robots.txt` oraz w meta `canonical`/`og:url` w `index.html` na docelową.
- Formularz rezerwacji i zgody cookies działają front-endowo (demo). Podłącz backend/mailer oraz Google Analytics, gdy będą gotowe.
