# Rang·Ritual

A minimal, editorial-style festive storefront for Rang·Ritual, a collection of Indian festive décor and puja essentials. The site pairs warm ivory tones, refined typography, and product-led imagery with a simple shopping bag and WhatsApp-based order enquiry flow.

## Overview

Rang·Ritual is a lightweight, responsive front-end website built with plain HTML, CSS, and JavaScript. It is designed to work as a static website and does not require a framework, database, or build step.

### Features

- **Responsive storefront:** Home, Collection, and Our Story pages designed for desktop and mobile screens.
- **Product catalogue:** Product photography, category filters, names, and displayed prices.
- **Shopping bag:** Add products, adjust quantities, review the subtotal, and retain the bag in the browser using `localStorage`.
- **Bundle pricing:** Supported multi-item offers are reflected in the bag calculations.
- **WhatsApp order enquiries:** Creates a pre-filled order summary and opens WhatsApp so the customer can contact the seller.
- **Static hosting support:** Suitable for Vercel and other hosts that serve static files.

## Pages

| File | Purpose |
| --- | --- |
| `index.html` | Homepage and featured products |
| `shop.html` | Product collection, filters, and shopping bag entry point |
| `about.html` | Brand story page |
| `style.css` | Layout, typography, colors, and responsive styling |
| `script.js` | Product data, filters, bag state, pricing, and WhatsApp order flow |
| `assets/` | Product photographs and homepage imagery |

## Run locally

No package installation or compilation is required.

1. Download or clone this project.
2. Keep the HTML files, `style.css`, `script.js`, and `assets/` directory together.
3. Open `index.html` in a browser.

For a closer match to a hosted environment, open the project folder in Visual Studio Code and use a local static server such as the Live Server extension.

## Configure WhatsApp orders

The order button uses the `WHATSAPP_NUMBER` constant near the top of `script.js`.

```js
const WHATSAPP_NUMBER = '919408663504';
```

Before publishing, replace this value with the seller's WhatsApp number in international format using digits only. Include the country calling code, and omit the plus sign, spaces, brackets, and hyphens. For example, `14165550123` is a format example, not a real contact recommendation.

Test the order flow on a device or browser where WhatsApp or WhatsApp Web is available. Confirm that the correct business account opens and that the pre-filled order details are accurate.

## Deploy to Vercel

1. Sign in to [Vercel](https://vercel.com/).
2. Import the project from a Git repository, or use Vercel's supported project-upload workflow.
3. For this plain static website, choose **Other** as the framework if asked.
4. No build command is required. Serve the project from its root directory, where `index.html` is located.
5. Deploy, then open the generated URL and test all pages and the order flow.

Keep the complete `assets/` directory in the deployed project. The site references images by relative path.

## Product and pricing notes

- Prices are currently displayed with the `$` symbol and are intended to be **CAD**, as shown on the website.
- Review product names, photo matching, bundle offers, and prices against the seller's current product list before launch.
- Confirm delivery, taxes, availability, and payment arrangements directly with the customer.

## Important limitations

This is a front-end catalogue and order-enquiry website, not a complete e-commerce payment system.

- It does not collect online payments.
- It does not create or store orders on a server.
- The shopping bag is saved only in the customer's browser.
- The seller confirms stock, delivery, taxes, and payment directly with the customer through WhatsApp.
- Anyone with access to the source code can see the configured WhatsApp number; do not place secret keys or private credentials in this project.

## Technology

- HTML5
- CSS3
- Vanilla JavaScript
- Browser `localStorage`
- WhatsApp click-to-chat links
- Google Fonts: DM Sans and Playfair Display

## Project maintenance checklist

Before making the website public, verify:

- All product photos match their names and prices.
- Bundle prices and quantity rules calculate correctly.
- The WhatsApp number belongs to the intended business account.
- Navigation, product filters, bag controls, and mobile layout work as expected.
- The published URL works on both desktop and mobile.

---

**Rang·Ritual** — Thoughtful details for festive moments.
