<!-- HOW TO USE: In README.md (1) update the Pages list and project structure with the block below,
     (2) paste the "Part 3" section after Part 2, (3) paste the Part 3 changelog ABOVE "### Part 2",
     (4) add the new references. Replace every [BRACKETED] item with your real details. -->

## Pages
- `index.html` — Home
- `menu.html` — Full menu
- `enquiry.html` — Catering / bulk order enquiry form (new in Part 3)
- `about.html` — About / our story
- `gallery.html` — Photo gallery with lightbox
- `contact.html` — Contact details, message form and map

## Part 3 — Functionality, SEO and Deployment

**Live site:** [PASTE YOUR NETLIFY / GITHUB PAGES LINK]

### JavaScript enhancements
- **Accordion** (`js/enhancements.js`) — FAQ on `enquiry.html`. Buttons use `aria-expanded` / `aria-controls`; the panel opens with a CSS transition and only one answer is open at a time.
- **Modal** — a native `<dialog>` on `enquiry.html` confirms the enquiry and shows the estimate.
- **Gallery lightbox** — built with DOM manipulation (`createElement`, `appendChild`); supports click, keyboard (Enter, Esc, arrow keys) and returns focus to the thumbnail on close.
- **Interactive map** (`js/map.js`) — Leaflet with OpenStreetMap tiles on `contact.html`, with a marker and popup for the shop address.
- **Animations / transitions** — hero copy rises in on page load, accordion and lightbox fade/slide, gallery image zoom on hover. All of it is disabled by the `prefers-reduced-motion` rule in `style.css`.

### Forms and validation (`js/forms.js`)
- `enquiry.html`: HTML5 attributes (`required`, `type`, `min`, `max`, `minlength`) plus JavaScript checks for name, email, South African phone format, number range and future date. Errors appear beside each field (`aria-invalid` + `aria-describedby`). A valid form is processed into a cost estimate and an availability message, then sent with **AJAX** (`fetch` + `FormData`) so the page does not reload.
- `contact.html`: same validation, plus message-type select and a free-text message. A valid form is compiled into a `mailto:` email to the shop address, ready for the customer to send.

### SEO
| Area | What was done |
|---|---|
| Titles and descriptions | Unique `<title>` and meta description on every page, including the town and service keywords |
| Headings | One `<h1>` per page, then `<h2>` / `<h3>` in order |
| Images | Descriptive file names and meaningful `alt` text; `loading="lazy"` on below-the-fold images |
| URLs and linking | Short lowercase file names; every page links to the others in the header and footer; links in body copy to the menu and enquiry pages |
| Mobile-friendly | Viewport meta tag; breakpoints at 1024 / 768 / 480px (Part 2) |
| Local SEO | `Restaurant` JSON-LD with address and opening hours; address repeated in the footer |
| Crawling | `robots.txt` and `sitemap.xml` in the site root |
| Social / backlinks | [LIST WHAT YOU DID OR PLAN: e.g. Facebook page link, Google Business Profile, local directories] |
| Page speed | Preconnect for Google Fonts with `display=swap`; scripts use `defer`; images exported at 480w / 768w / 1200w with `srcset` |
| Security | HTTPS from the host; `_headers` file sets `X-Content-Type-Options`, `X-Frame-Options`, `Referrer-Policy`; form data is validated on the client, and the form service validates on the server side; external links use `rel="noopener noreferrer"` |

### Deployment
Deployed on [NETLIFY / GITHUB PAGES] from the `main` branch of this repository. Every push to `main` redeploys the site.

## Changelog

### Part 3
- **Added** `enquiry.html` with enquiry form, FAQ accordion and confirmation modal.
- **Added** `js/forms.js` — client-side validation, error messages, cost/availability response, AJAX submit, `mailto` compile for the contact form.
- **Added** `js/enhancements.js` — accordion and gallery lightbox.
- **Added** `js/map.js` — Leaflet map on `contact.html`.
- **Added** Part 3 styles to `css/style.css` (accordion, modal, lightbox, form errors, animations, map).
- **Added** `robots.txt`, `sitemap.xml`, `_headers`.
- **Changed** every page: unique title and meta description, canonical link, Enquiry link in navigation, fuller footer links, `defer` on scripts.
- **Changed** `about.html`: added `Restaurant` structured data, Open Graph tags, internal links to menu and enquiry pages.
- **Fixed** [FEEDBACK ITEM 1 FROM PART 2 — what the marker said, what you changed, which file].
- **Fixed** [FEEDBACK ITEM 2 …].

## References (add to the existing list)
- MDN Web Docs. *Client-side form validation*. https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Forms/Form_validation
- MDN Web Docs. *The Dialog element*. https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/dialog
- MDN Web Docs. *Using the Fetch API*. https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch
- Leaflet. *Quick Start Guide*. https://leafletjs.com/examples/quick-start/
- Google Search Central. *SEO Starter Guide*. https://developers.google.com/search/docs/fundamentals/seo-starter-guide
- Sitemaps.org. *Sitemaps XML format*. https://www.sitemaps.org/protocol.html
- Schema.org. *Restaurant*. https://schema.org/Restaurant
- Netlify Docs. *Custom headers*. https://docs.netlify.com/manage/routing/headers/
- Formspree. *Documentation*. https://help.formspree.io/
