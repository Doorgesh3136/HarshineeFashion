# Harshinee Fashion — Mauritius

Website for **Harshinee Fashion**, an Indian ethnic wear and bridal couture boutique in Mauritius.

It is a single self-contained page (`index.html`) built with Tailwind CSS (CDN), Google Fonts and Font Awesome. You don't need to build anything: open the file, or host it on GitHub Pages.

## Features
- Branded intro loader: a gold mandala draws in, the name is revealed, and curtains open. The full intro plays once per session; repeat visits get a short version, and visitors can tap to skip.
- Gold/maroon wipe transitions between sections, staggered scroll reveals, a hero line-mask entrance, and a scroll progress bar.
- Product catalogue with combined category, occasion and price-sort filters, quick view with image thumbnails, a wishlist, and a bag. The bag and wishlist are saved in the browser.
- Checkout and fitting bookings go straight to **WhatsApp** with the order or booking details already filled in.
- Respects the "reduce motion" accessibility setting.

## Editing shop details
Open `index.html` and find the `SHOP` settings near the top of the main `<script>`:

```js
const SHOP = {
    name: 'Harshinee Fashion',
    whatsapp: '2304608888',     // WhatsApp number, international format
    freeDeliveryFrom: 15000,    // Rs
    promo: { code: 'DIWALI2026', percent: 10 }
};
```

Products live in the `PRODUCTS` array just below it. The phone numbers and boutique addresses shown in the page text are in the HTML itself.
