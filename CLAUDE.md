# Beryl Traders website

Static one-page website for **Beryl Traders**, a cashew business. No build step, no framework: open `index.html` in a browser.

## What the business sells (keep the site to exactly this)
- Four products only: **Whole**, **Splits**, **Pieces**, **Powder** cashews.
- Every product is sold in a **1 kg pouch**. No other pack sizes, no tins, no roasted/masala/gift products.
- No prices on the site. Every call to action asks the customer to request today's price.

## Files
```
index.html          all HTML, CSS and JS in one file
favicon.svg         gold disc + cashew mark (same as header logo)
apple-touch-icon.png 180x180 home-screen icon
.github/workflows/pages.yml  GitHub Pages deploy (copies only public files; CLAUDE.md is not published)
img/            photos (Unsplash License, free for commercial use)
  raw.jpg         hero (masked into a cashew shape) + Pieces card + process step 3
  white.jpg       Whole card + process step 4
  ring.jpg        Splits card + process step 5
  tree.jpg        process step 1 (cashew flower)
  apple-hand.jpg  process step 2 (cashew apple)
  apple-red.jpg   "Why kitchens keep coming back" photo
  og-image.jpg    1200x630 social preview card (Open Graph)
```
Photographer credits are in the footer. Keep them if photos stay; update them if photos change.

## Design (settled — the owner chose these)
- Single colour scheme, **Beryl Green**. CSS variables in `:root`: `--bg #0F3D38`, `--surface #164C46`, `--ink #F6ECD9`, `--muted #B5CCC3`, `--accent #F2B33D` (gold), `--accent-ink #1A1205`, `--pop #E8553A` (cashew-apple red), `--kernel #F4E3C1`.
- There is intentionally **no colour/theme switcher** (removed at the owner's request).
- Fonts: Young Serif (headings) + Figtree (body) from Google Fonts.
- Signature elements: hero photo clipped to a cashew shape (`#cashewClip` SVG clipPath), spinning "Whole" sticker, tilted scrolling ticker, and the "Four cuts. One kernel." picker that draws whole kernels / halves / pieces / a powder heap on a tray.
- The cashew shape is one SVG `<symbol id="nut">` reused for the logo, ticker, tray and wholesale band.

## Page sections (in order)
Header nav → Hero → Ticker → Cuts picker (`#grades`) → Process, 5 numbered steps (`#journey`) → Product cards (`#products`) → Why us → Wholesale band (`#wholesale`) → Order form (`#order`) → Footer.

## Contact details (filled in)
- WhatsApp/phone: +91 83003 81322 (`WHATSAPP_NUMBER = "918300381322"`, `PHONE_DISPLAY` at top of `<script>`).
- Email: beryltraders@gmail.com. Address: CSI Church Street, Thengamputhoor.

## Still to confirm with the owner
- Marketing claims like "Every batch tasted before it's packed" and "sorted by hand" — confirm with the owner they're true.

## Known gaps / good next tasks
- **Photos:** there's no real photo for Powder (the card uses a drawn dust heap), and the Splits and Pieces cards show whole kernels. Swap in the owner's own product photos when available.
- Order form doesn't submit anywhere: it builds a WhatsApp message and opens `wa.me`. That's intentional for a static site.
- Deployment: GitHub Pages via Actions on push to `main`, expected URL https://ebenitosam.github.io/beryl-traders/. The canonical, `og:url` and `og:image` tags use that absolute URL; change them if the repo name or domain changes.
- Could add: Google Maps embed for the shop, a Tamil-language version.

## Working rules
- Keep it a static site with no build tooling unless the owner asks otherwise.
- Keep it responsive (checked at 1440px and 390px wide) and respect `prefers-reduced-motion`.
- Check changes in a real browser before calling them done.
