# Nimco House — order-ready storefront starter

A responsive, no-build website for a Pakistani nimco/snacks business. It includes a product catalog, search and category filters, a cart saved in the customer's browser, quantity controls, delivery calculation, customer checkout form, and WhatsApp order handoff.

## Important before taking real orders

The site code is complete, but your business-specific details were not provided. The starter catalog and prices are examples. **Do these steps before publishing**:

1. Open `config.js` and set `WHATSAPP_NUMBER` to your business WhatsApp number in international digits-only format (Pakistan example format: `923001234567`, without `+`, spaces or dashes).
2. Set your real `DELIVERY_FEE`, `FREE_DELIVERY_OVER`, and `MIN_ORDER_SUBTOTAL` values. Set `FREE_DELIVERY_OVER` or `MIN_ORDER_SUBTOTAL` to `0` to disable those rules.
3. Open `products.js` and replace every example item, pack size, description, price, category, badge and availability with your real catalog. Prices are in PKR by default.
4. Set `SHOW_SETUP_NOTICE: false` in `config.js` only after you have replaced the starter catalog and prices.
5. Review the About and FAQ copy in `index.html`, especially service areas, payment options, delivery promises and return/refund policy. Do not advertise policies you do not provide.
6. Test the complete checkout on a phone and desktop using your actual WhatsApp number. Make a test order and confirm that the generated message is accurate before launch.

## How order placement works

This is a **WhatsApp-based checkout**. The customer adds items to the bag, enters their contact/delivery details, and clicks “Send order on WhatsApp.” The site opens WhatsApp with the order message prefilled. The customer must press **Send inside WhatsApp** for the shop to receive it. The website does not automatically send messages, save customer orders to a store database, charge a card, or provide an order-management dashboard.

No payment gateway is connected. Confirm payment, final delivery fee, stock and delivery time directly with the customer. For card/online payments or a backend order dashboard, connect a payment provider and a secure order backend before promising those features.

## Run locally

- Simplest: open `index.html` in a modern browser.
- Or run a static server from this folder, for example `python -m http.server 8000`, then open `http://localhost:8000`.
- No `npm install`, bundler or build step is required.

## Deploy

Upload this folder to any static website host such as Cloudflare Pages, Netlify, GitHub Pages or your existing hosting provider. Keep all files at the same level so `index.html` can load `config.js`, `products.js`, `app.js` and `styles.css`.

## Files

- `index.html` — page structure, checkout form, FAQs and semantic sections.
- `styles.css` — responsive styling and mobile/cart/modal layouts.
- `config.js` — business name, WhatsApp destination, delivery settings and launch notice.
- `products.js` — editable snack catalog.
- `app.js` — filters, search, cart persistence, totals, validation and WhatsApp checkout.
- `favicon.svg` — editable browser icon.

## Notes

- Cart contents are stored only in the customer's browser via local storage.
- Currency formatting defaults to PKR.
- The checkout message includes the items, quantities, subtotal, estimated delivery and customer details.
- The website does not collect analytics or send customer details to a database.
