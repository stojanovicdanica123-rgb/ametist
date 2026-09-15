# Ametist — ametist.rs

Statičan sajt. Jedan HTML fajl, bez build koraka.

## Objavljivanje na GitHub Pages

1. Napravi repo i ubaci **sadržaj ovog foldera** u root (ne sam folder).
2. Settings → Pages → Source: `Deploy from a branch` → `main` / `/ (root)`.
3. Settings → Pages → Custom domain: `ametist.rs` (fajl `CNAME` je već tu).

## DNS kod registrara domena

| Tip | Naziv | Vrednost |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | KORISNICKO-IME.github.io |

Kad DNS propagira, uključi **Enforce HTTPS** u Pages podešavanjima.

### Ako NE koristiš domen ametist.rs
Obriši `CNAME` i u `index.html` promeni `<link rel="canonical">`, `og:url` i `og:image` na svoju GitHub Pages adresu. Isto i u `sitemap.xml` i `robots.txt`.

## Video pozadina

Hero i kontakt sekcija imaju video pozadinu. Skripta prvo traži **`hero.mp4`** u root-u repo-a; ako ga nema, koristi rezervni HLS stream.

Taj rezervni stream nije naš — može da prestane da radi u svakom trenutku. Ubaci svoj `hero.mp4` (H.264, bez zvuka, 1920×1080, 8-15 s u petlji, 2-5 MB) u root i sajt ga automatski koristi, bez promene koda.

## Sadržaj

| Fajl | Šta je |
|---|---|
| `index.html` | ceo sajt |
| `404.html` | stranica za nepostojeće adrese |
| `og.png` | slika za deljenje na mrežama (1200×630) |
| `robots.txt`, `sitemap.xml` | za Google |
| `CNAME` | custom domen |
| `.nojekyll` | isključuje Jekyll obradu na Pages |

## Izmene sadržaja

Tekst usluga, procesa, FAQ-a i pravnih strana je u nizovima na kraju `index.html` (potraži `USLUGE`, `PROCES`, `FAQ`). Kontakt: telefon `062 813 7038` i Instagram `@ametistweb.rs`.
