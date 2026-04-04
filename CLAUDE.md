# Aurora Branding Co. — Website

## Projekt leírás
Az Aurora Branding Co. publikus marketing weboldala. Statikus HTML oldal, Vercel-re deployolva.
Beauty szakembereknek szóló mentoring brand — blog-központú edukációs platform.

## Tech stack
- Statikus HTML
- Tailwind CSS (CDN)
- Google Fonts (Pinyon Script, EB Garamond, DM Sans)
- Iconify (ikonok)
- CSS animációk (inline <style> tagben)
- Vercel hosting

## Fájlstruktúra
aurora-branding-website/
├── index.html                          ← Homepage
├── blog/
│   ├── index.html                      ← Blog listing
│   └── salon-policies-for-beauty.../
│       └── index.html                  ← Cikk sablon
├── aurora-circle/
│   └── index.html                      ← Newsletter signup
├── images/
├── vercel.json
├── package.json
└── CLAUDE.md

## Brand színek (PONTOS értékek, mindig ezeket használd)
| Szín | Kód | Használat |
|------|-----|-----------|
| Light pink | #EED6DC | Háttér, nagy felületek |
| Medium pink | #E5A5B5 | Gombok, aktív elemek, hover |
| Dark pink | #D38BA1 | CTA, kiemelések, gradiens sötét vége |
| Body text | #4A4A4A | Törzsszöveg (szürke, NEM fekete) |
| Secondary text | #9C9C9C | Alcímek, placeholder |
| Nude háttér | #FAF7F6 | Oldalháttér, kártyák |
| Fehér | #FFFFFF | Kontrasztelemek |
| Gold accent | #C9956B | Csillag dekorációk |
| Gradiens | #D38BA1 → #EED6DC | Bal→jobb vagy lent→fel |

## Tipográfia
- **Logo:** Pinyon Script (elegant script) — "Aurora"
- **Dekoratív:** Pinyon Script cursive — alcímek, form headingek
- **Címek:** EB Garamond serif (letter-spacing: 0.025em) — H1, H2 headingek
- **Body:** DM Sans light/regular — törzsszöveg (font-size: 1.1rem a body-n)
- **Labels:** DM Sans uppercase, wide letter-spacing

## Design rendszer szabályok
- **Animated gradient blobs:** 2-3 nagy lágy blob (#D38BA1 → #EED6DC → #FAF7F6), CSS @keyframes morphing, 20-30s infinite, opacity 0.2-0.4, blur(80-120px). Mindig jelen vannak, NEM scroll-triggered.
- **Sparkle stars ✦:** 10-14 db négyágú csillag SVG, szétszórva, 8-30px méret, #E5A5B5 és #C9956B, staggered pulse animáció.
- **Glassmorphism:** Kártyák: rgba(255,255,255,0.8-0.88), backdrop-blur(10-16px), subtle #EED6DC border.
- **Grain texture:** Finom noise overlay 2-3% opacity.
- **NINCS scroll-triggered animáció.** Minden CSS-only, page load-tól fut.

## Navigáció (minden oldalon azonos)
Centered script logo "Aurora" + "BRANDING CO." — alatta: HOME | BLOG | AURORA CIRCLE (elválasztva vékony vertical line-nal). Frosted glass hatás. NEM sticky.

## Deploy
- **Hosting:** Vercel (külön projekt az Aurora Booking-tól)
- **Domain:** aurorabrandingco.com (DNS átállítás szükséges WordPress-ről)
- **Repo:** GitHub: aurora-branding-website

## Notion dokumentáció
- Projekt HQ: https://www.notion.so/3377c026e356816f8c42f8604591f174
- Arculat/Színvilág: https://www.notion.so/3307c026e356813abebcfa9ad9ab8287

## Fontos szabályok
1. Új oldal létrehozásakor MINDIG nézd meg a többi HTML fájlt referenciaként
2. A színkódokat PONTOSAN használd — ne közelíts, ne kerekíts
3. Az animációk CSS-only — semmi JavaScript scroll observer
4. A szöveg nyelve a content-ben ANGOL (ez angol nyelvű blog)
5. A struktúra és meta elemek (nav, footer) MINDEN oldalon konzisztensek
