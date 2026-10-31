# Harshinee Fashion — Mauritius

Website for **Harshinee Fashion**, an Indian bridal and non-bridal specialist with boutiques at Royal Road, Lallmatie and Bypass, St Julien d'Hotman (both opposite Kalimaye).

It is a single self-contained page (`index.html`) built with Tailwind (CDN), Google Fonts and Font Awesome. There's no build step: open it, or host it on GitHub Pages (Settings → Pages → `main` / root).

## Features
- Intro loader: a gold mandala with a lotus centre draws itself in, the letters reveal, and curtains open. The full version plays once per session, and visitors can tap to skip it.
- Section transition: silk pleats drop in, a mandala draws itself and the section name appears, then the pleats lift away.
- 40-piece collection in 6 categories with category tiles, chips, search, price sort and "show more". Cards only show photo, name and price.
- Bag, wishlist, enquiries and visit requests all go to WhatsApp (5799 0933) with the message pre-filled.

## Updating products
In `index.html`, find the `RAW` list. Each row is:

```js
['Name', 'category', price, 'unsplash-photo-id', 'hover-photo-id', 'Tag']
```

Categories are `bridal`, `lehenga`, `saree`, `gown`, `groom` and `men`. To use the shop's own photos, change the `IMG()` helper (or the IDs) so it points at real image files.

**Note:** the photos are Unsplash stock placeholders and the prices are samples. Replace both with Harshinee's real pieces before launch.
