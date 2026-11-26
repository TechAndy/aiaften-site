# AI:Aften Tønsberg

Statisk landingsside for AI:Aften Tønsberg, tenkt for [aiaften.no](https://aiaften.no/).

Siden er ren HTML og CSS. Ingen byggesteg. Den kan ligge på GitHub Pages, Netlify eller Vercel.

## Kjør lokalt

```bash
python3 -m http.server 41731
```

Åpne [http://127.0.0.1:41731](http://127.0.0.1:41731).

## Bytt dato og program

Alt innhold for kvelden ligger i `index.html`. Søk etter `3. desember 2026` og `2026-12-03`, og oppdater:

1. `<title>` og meta-beskrivelsen
2. Datoen i toppen (`.when`). Ukedag, dag og måned skal stå én gang, i den rekkefølgen i koden.
3. Listen under `<!-- PROGRAM -->`
4. Feltet Praktisk
5. JSON-LD i `<head>` (`startDate` er dørene 18.30, `endDate`, `doorTime`, `subEvent`)

Programmet er en vanlig liste. Ett `<li>` er ett punkt, med klokkeslett i `<time>` og teksten i `<p>`.

Påmeldingsknappen peker til arrangementssiden hos Tønsberg og Færder Næringsforening:

https://www.tfnf.no/liste-arrangementer?aiaften-28335

## Logo

- `assets/ai-aften-merke.png` og `assets/ai-aften-cover.png` er originalene
- `assets/ai-aften-merke-web.png`, `assets/ai-aften-cover-960.png`, `assets/ai-aften-cover-1600.png` og `assets/ai-aften-cover-og.png` er web-utgaver
- `og:image` bruker cover-bildet i 1200×675

## Publisering

Roten i repoet er nettstedet. `CNAME` er satt til `aiaften.no` for GitHub Pages. Pek domenet til GitHub Pages, Netlify eller Vercel, og publiser uten byggesteg (publiseringsmappe `/`).
