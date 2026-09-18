# Food Corner — Website Project (WEDE5020 Portfolio of Evidence)

**Author:** Tumisho Mthombeni — Student Number: ST10441611

A five-page website for Food Corner, a neighbourhood takeaway. Built with
semantic HTML5, a single external CSS stylesheet, and vanilla JavaScript
for the mobile navigation menu.

## Pages
- `index_.html` — Home
- `menu.html` — Full menu
- `about_.html` — About / our story
- `gallery.html` — Photo gallery
- `contact_.html` — Contact details and enquiry form

## Project structure
```
/
├── index_.html
├── menu.html
├── about_.html
├── gallery.html
├── contact_.html
├── css/
│   └── style.css
├── js/
│   └── script.js
└── images/
    └── (site photos, exported at 480w / 768w / 1200w for responsive images)
```

## Part 2 — CSS Styling & Responsive Design

This part builds on the Part 1 HTML structure and adds:

- **External stylesheet** (`css/style.css`) linked from every page, with a
  reset, a CSS custom-property token system (colour, type, spacing), and
  no inline styles.
- **Typography**: Fraunces for headings, Work Sans for body copy, with a
  fluid type scale (`clamp()`) so headings scale smoothly between mobile
  and desktop.
- **Layout**: CSS Grid for the menu and gallery grids, Flexbox for the
  header, hero copy block, and the About/Contact split layouts.
- **Visual styling**: colour, background, border, and hover/focus/active
  states on buttons, nav links, and menu cards — no default browser
  outlines removed without a replacement, so keyboard focus stays visible.
- **Responsive design**: breakpoints at **1024px**, **768px**, and
  **480px**; relative units (`rem`, `em`, `%`, `clamp()`) instead of fixed
  pixel values; a `srcset`/`sizes` responsive-image setup ready for the
  final photography.

### Screenshot evidence

> Add screenshots of each breakpoint here before submitting, e.g.:
>
> | Desktop (1200px) | Tablet (768px) | Mobile (375px) |
> |---|---|---|
> | ![desktop](screenshots/desktop.png) | ![tablet](screenshots/tablet.png) | ![mobile](screenshots/mobile.png) |

## Changelog

### Part 2
- **Added** `css/style.css` — full desktop styling: reset, typography
  scale, colour tokens, Grid/Flexbox layout for header, hero, menu grid,
  about split, gallery grid, and contact layout.
- **Added** `js/script.js` — mobile navigation toggle for screens
  768px and below.
- **Added** responsive breakpoints at 1024px, 768px, and 480px across all
  five pages; menu and gallery grids collapse from 3 → 2 → 1 columns.
- **Added** `srcset`/`sizes` markup on `gallery.html` images in
  preparation for optimised, multi-resolution photography.
- **Fixed** *(example — replace with your real Part 1 feedback)*:
  corrected heading hierarchy on `about.html` so there is a single `<h1>`
  per page.
- **Fixed** *(example)*: added missing `alt` text to all images flagged
  in Part 1 feedback.

### Part 1
- Initial five-page HTML structure, semantic markup, and navigation
  created for Food Corner.

## References
- MDN Web Docs. *CSS Grid Layout*. https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout
- MDN Web Docs. *Flexbox*. https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox
- MDN Web Docs. *Responsive images*. https://developer.mozilla.org/en-US/docs/Web/HTML/Guides/Responsive_images
- MDN Web Docs. *Using media queries*. https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries
- Google Fonts. *Fraunces*. https://fonts.google.com/specimen/Fraunces
- Google Fonts. *Work Sans*. https://fonts.google.com/specimen/Work+Sans
