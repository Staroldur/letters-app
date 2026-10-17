# Dino companion website

Static HTML/CSS for https://staroldur.github.io/letters-app/.
Keep `index.html` and `privacy.html` at the repository root to preserve the existing public URLs. There is no build step, package install, JavaScript or backend. Fonts and artwork are served locally.

Preview locally:

```sh
python3 -m http.server 8765 --bind 127.0.0.1
```

Open `http://127.0.0.1:8765/index.html` and `http://127.0.0.1:8765/privacy.html`.

## Artwork and font provenance

Reused from `Staroldur/hebrew-letters-game`, without generating new artwork:

- `assets/dino.webp` ← `art/dino/Dino.png`
- `assets/bunny.webp` ← `art/bunny/bunny.png`
- `assets/turtle.webp` ← `art/turtle/turtle.png`
- `assets/forest.webp` ← `art/ForestBackground.png`
- `assets/Heebo.ttf` ← `assets/Heebo/Heebo-VariableFont_wght.ttf`; SIL Open Font License is included as `assets/Heebo-OFL.txt`.

Images were resized and encoded to WebP (quality 85). The page assets total approximately 350 KB. No outside image or font requests are needed.

## Validation and policy review

On 17 October 2026, both pages passed W3C Nu HTML validation with no messages. Responsive checks at 320–1440 CSS pixels found no horizontal overflow. Hebrew RTL, English LTR, isolated addresses, internal links, image loading and accessibility structure were checked. The App Store destination returned HTTP 200 after redirect. No email or purchase was submitted.

The privacy policy was revised against game scripts, local storage, parent actions, native sharing and the StoreKit integration. It distinguishes app processing from Apple, GitHub Pages and voluntary support correspondence. Before publication, the developer must confirm mailbox retention/deletion practices, legal operator details, StoreKit binary provenance, release privacy disclosures and applicable children's-app requirements. No fixed support retention period or unverified certification is promised.

The full implementation/testing report is in the game checkout at `docs/website-privacy-refresh.md`. All changes remain uncommitted and unpushed. The new pages have not been deployed.
