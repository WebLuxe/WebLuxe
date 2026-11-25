# WebLuxe

**Build your dream website.** Website for WebLuxe, a web design studio in Mauritius.

Live: https://webluxe.github.io/WebLuxe/

## Structure

```
index.html            page markup (all routes: home, work, services, pricing, process, contact)
css/style.css         all styles (screen-size tuning for laptops/monitors at the bottom)
js/main.js            interactions, animations, router, price estimator
assets/icons/         favicon / logo mark
assets/img/work/      client website screenshots (WebP)
```

Edit your WhatsApp number, email, prices and add-ons at the top of `js/main.js` (the `EDIT THESE` block).

## Currency

All prices are stored in MUR (`TIERS` / `EXTRAS` in `js/main.js`). Visitors see them converted to MUR, USD, EUR, GBP, ZAR or INR. The currency is picked from their timezone, and they can change it with the switcher. Live rates come from open.er-api.com and are cached for 12h, with fallback rates in the `CCY` block. WhatsApp and contact messages always quote Rs. To convert a new price in the HTML, add `data-mur="12345"` to it (`data-fmt="k"` for the short "Rs 12k" form).

## Analytics

Set `GOATCOUNTER` at the top of `js/main.js` to your GoatCounter code (free, no cookies, from goatcounter.com) to turn on analytics. It counts page views per section and clicks on WhatsApp, email and phone links. When it's empty, analytics is off.

## SEO

`index.html` has a canonical link, Open Graph and Twitter tags (share image: `assets/img/og.jpg`) and JSON-LD `ProfessionalService` data with the tier prices in MUR. If you change prices in `js/main.js`, update the JSON-LD too. `sitemap.xml` can be submitted in Google Search Console.

## Showing or hiding prices

`SHOW_PRICES` at the top of `js/main.js`. When it's `false` (the current setting), only "From Rs 10,000" shows, the other tiers say "Get a quote", and the estimator sends a quote request without prices. When it's `true`, full prices and currency conversion are back.

## Portfolio videos

`assets/video/*.mp4` (720×450, muted loops) plus `.jpg` posters. Only one plays at a time: the one you hover, or the one most in view.
