# Harshinee Fashion — Mauritius

Website for **Harshinee Fashion**, an Indian bridal and non-bridal specialist with boutiques at Royal Road, Lallmatie and Bypass, St Julien d'Hotman (both opposite Kalimaye).

It is a single self-contained page (`index.html`) built with Tailwind (CDN), Google Fonts and Font Awesome. There's no build step: open it, or host it on GitHub Pages (Settings → Pages → `main` / root).

## Features
- Intro loader: a gold mandala with a lotus centre draws itself in, the letters reveal, and curtains open. The full version plays once per session, and visitors can tap to skip it.
- Section transition: silk pleats drop in, a mandala draws itself and the section name appears, then the pleats lift away.
- 40-piece collection in 6 categories with category tiles, chips, search, price sort and "show more". Cards only show photo, name and price.
- Gold dot backgrounds (twinkling on the dark sections, subtle antique gold on the cream sections), a slow-turning hero mandala and rising gold dust.
- "How to Shop With Us" steps: browse, WhatsApp, try on in boutique.
- Bag, wishlist, enquiries and visit requests all go to WhatsApp (5799 0933) with the message pre-filled.

## Admin panel (`/admin`)
Go to **https://doorgesh3136.github.io/HarshineeFashion/admin/** to add, edit, hide, reorder or delete products, upload photos, and edit the rotating announcements. Then press **Publish**. The site updates in about 1–2 minutes.

The site is static (no server), so the admin signs in with a GitHub token instead of a password:
1. GitHub → Settings → Developer settings → **Fine-grained tokens** → Generate new token.
2. Repository access: **Only select repositories → HarshineeFashion**.
3. Permissions → Repository permissions → **Contents: Read and write**.
4. Paste the token into the admin page. Anyone with the token can edit the site, so keep it private.

Every publish is a normal Git commit, so changes can be reviewed or reverted from the repo history. Uploaded photos are resized to 1400px and saved in `images/`.

## Data file
Products and announcements live in `data.js` (written by the admin). It can be edited by hand too. Each product looks like:

```json
{ "id": 1, "name": "Crimson Zari Bridal Lehenga", "category": "bridal", "price": 18500,
  "img": "images/crimson.jpg", "hover": "1654764746225-e63f5e90facd", "tag": "Bestseller", "hidden": false }
```

Categories are `bridal`, `lehenga`, `saree`, `gown`, `groom` and `men`. A photo can be a repo path (`images/…`), a full URL, or an Unsplash photo ID. Keep `id` unique and unchanged so shoppers' saved bags and wishlists still match.

## 404 page
`404.html` is the branded "page not found" screen. GitHub Pages serves it automatically for any missing URL.

**Note:** the photos are Unsplash stock placeholders and the prices are samples. Replace both with Harshinee's real pieces before launch.
