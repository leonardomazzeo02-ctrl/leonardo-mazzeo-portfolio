# Leonardo Mazzeo — Portfolio

Sito portfolio in **Astro** con **GSAP** (animazioni), **Lenis** (smooth scroll) e stile coerente col CV (blu #3577BE, font Archivo, impianto editoriale).

## Avvio in locale
Serve Node 18+.
```bash
cd site
npm install
npm run dev      # http://localhost:4321
```
Build di produzione: `npm run build` (output in `dist/`).

## Struttura
```
src/
  data/works.js        → contenuti dei case study (unica fonte, modifica qui)
  layouts/Base.astro   → head, nav, footer, cookie banner, GSAP + Lenis
  pages/index.astro    → home: hero tipografico + griglia editoriale animata
  pages/work/[slug].astro → template case study (Overview/Ruolo/Sfida/Processo/Soluzione)
  pages/about.astro    → bio + form contatti
  pages/404.astro      → 404 comica con mascotte animata
  styles/global.css    → design system (token, tipografia, componenti)
public/
  mascot.webp          → la tua illustrazione (marchio / mascotte / favicon)
  works/*              → immagini dei progetti
```

## Deploy gratis (Netlify)
1. Crea un repo GitHub e carica questa cartella `site/`.
2. Su netlify.com → "Add new site" → "Import from GitHub" → scegli il repo.
   Build già configurata in `netlify.toml` (build `npm run build`, publish `dist`).
3. Il **form** in /about funziona in automatico (Netlify Forms) una volta online.
4. Dominio: parti con `nome.netlify.app`, poi eventuale dominio tuo.

## Da fare / da fornire
- Cookie: ora c'è un banner placeholder con la mascotte. In produzione incolla lo **snippet Iubenda** al posto dello script cookie in `Base.astro`.
- Immagini mancanti: Micidial e libro La Ferla (i lavori mostrano un placeholder colorato finché non le aggiungi in `public/works/`).
- QR del portfolio, se lo vuoi anche sul CV.
