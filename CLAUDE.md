# Aurora Branding Co. — Website

## Projekt leírás
Az Aurora Branding Co. publikus marketing weboldala. Statikus HTML, Vercel-re deployolva.
Beauty szakembereknek szóló mentoring brand — blog-központú edukációs platform.

**Lokális mappa:** `~/Projects/aurora-branding-website` (Mac, single source of truth — NEM Google Drive-ról dolgozunk!)

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
│   └── aurorabranding-logo-RGB-01.png  ← Brand logó
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
| Sparkle csillagok | #B0B0B0 | Szürke csillag dekorációk |
| Gradiens | #D38BA1 → #EED6DC | Bal→jobb vagy lent→fel |

## Tipográfia (hivatalos Aurora arculat)

### Betűtípus-készlet
- **EB Garamond** — serif, főcímek (H1-H3)
- **DM Sans** — sans-serif, body szöveg, H4-H6, menü
- **Pinyon Script** — script, CSAK akcentusként (1-2 szó, dekoratív)

### Weboldal heading hierarchia
| Elem | Font | Méret | Vastagság | Átalakítás | Sormagasság | Betűköz |
|------|------|-------|-----------|------------|-------------|---------|
| Body | DM Sans | 1.1rem | 400 | Alapértelmezett | 1.8rem | 0.5px |
| H1 | EB Garamond | 2.8rem | 600 | Capitalize | 3.3rem | 0.03em |
| H2 | EB Garamond | 2.3rem | 800 | Capitalize | 2.6rem | 0.02em |
| H3 | EB Garamond | 2.1rem | 600 | Capitalize | 2.8rem | 0.02em |
| H4 | DM Sans | 1.6rem | 500 | Capitalize | 2rem | 0.02em |
| H5 | DM Sans | 1.3rem | 500 | Capitalize | 1.8rem | 0.02em |
| H6 | DM Sans | 1.1rem | 600 | Capitalize | 1.7rem | 0.5px |

### Brand stílusok
| Stílus | Font | Méret | Vastagság | Betűköz |
|--------|------|-------|-----------|---------|
| Elsődleges | EB Garamond | 3.2rem | 700 Bold | 1.5px |
| Másodlagos | DM Sans | 2rem | 600 Semi Bold | 0.5px |
| Szöveg | DM Sans | 1.1rem | 300 Light | 0.5px |
| Hangsúly | Pinyon Script | 2.4rem | 400 Normal | 0 |
| Menü | DM Sans | 1rem | 600 Semi Bold | 0.08em |

### Homepage hero kivétel
- Script szöveg: Pinyon Script, 2.8rem, #D38BA1
- Főcím: EB Garamond, 3.3rem, 700, uppercase, 0.12em betűköz, #4A4A4A
- Subtitle: DM Sans, 1.15rem, #9C9C9C
- Gomb: DM Sans, #4A4A4A háttér, fehér szöveg, hover: #D38BA1

## Design rendszer szabályok
- **Animated gradient blobs:** 2-3 nagy lágy blob (#D38BA1 → #EED6DC → #FAF7F6), CSS @keyframes morphing, 20-30s infinite, opacity 0.2-0.4, blur(80-120px). Mindig jelen vannak, NEM scroll-triggered.
- **Sparkle stars ✦:** 10-14 db négyágú csillag SVG, szétszórva, 8-30px méret, #B0B0B0 (szürke), staggered pulse animáció.
- **Glassmorphism:** Kártyák: rgba(255,255,255,0.8-0.88), backdrop-blur(10-16px), subtle #EED6DC border.
- **Grain texture:** Finom noise overlay 2-3% opacity.
- **NINCS scroll-triggered animáció.** Minden CSS-only, page load-tól fut.

## Navigáció (minden oldalon azonos)
- Logó: images/aurorabranding-logo-RGB-01.png — centered, link a főoldalra
- Linkek: HOME | ABOUT | BLOG | AURORA CIRCLE (DM Sans, 1rem, 600, uppercase, 0.08em)
- Aktív menüpont: #9C9C9C (szürke), NEM aláhúzott
- Inaktív menüpontok: #D38BA1 (pink)
- Háttér: rgba(255,255,255,0.95), backdrop-blur 16px
- NEM sticky

## Hero szekciók
- Homepage: fehér→rózsaszín gradiens (felülről lefelé), háttérkép alacsony opacity, nav és hero egybeolvad
- Blog listing: tipografikus, nincs háttérkép
- Aurora Circle: lifestyle kép + glassmorphic signup kártya
- Cikk sablon: lifestyle kép, fehér→rózsaszín gradiens overlay, 60vh

## URL struktúra
| Oldal | URL |
|-------|-----|
| Homepage | / |
| Blog listing | /blog |
| Aurora Circle | /aurora-circle |
| Cikk sablon | /blog/salon-policies-for-beauty-businesses |

## Deploy
- **Hosting:** Vercel (külön projekt az Aurora Booking-tól)
- **Staging:** aurora-branding-website.vercel.app
- **Domain:** aurorabrandingco.com (DNS átállítás szükséges WordPress-ről)
- **Repo:** GitHub: aurora-branding-website

## Notion dokumentáció
- Projekt HQ: https://www.notion.so/3377c026e356816f8c42f8604591f174
- Arculat/Színvilág: https://www.notion.so/3307c026e356813abebcfa9ad9ab8287
- Tipográfia: https://www.notion.so/3307c026e35681409425c2c010d8aad8

## Fontos szabályok
1. Új módosítás előtt MINDIG olvasd ki a jelenlegi értékeket és mutasd meg — NE módosíts vakon
2. A színkódokat PONTOSAN használd — ne közelíts, ne kerekíts
3. Az animációk CSS-only — semmi JavaScript scroll observer
4. A szöveg nyelve a content-ben ANGOL
5. A navigáció MINDEN oldalon konzisztens
6. CSAK azt módosítsd amit kérnek — semmi extrát
7. A Pinyon Script CSAK akcentusként — soha nem törzsszövegként
8. A H1-H3 MINDIG EB Garamond, H4-H6 MINDIG DM Sans
