# Amchi Mumbai

A fully responsive city guide to Mumbai's street food, landmark places and local train network. Built from scratch with semantic HTML5 and modern CSS only (no JavaScript, no frameworks) as the Week 2 task of the Yuva Intern frontend programme: implementation of responsive web design.

The design takes its look from the city itself: the black-and-yellow kaali-peeli taxi (checker stripes, hard shadows), Devanagari lettering, Warli folk-art patterns and a sunset over the Arabian Sea.

## Responsive techniques used

- **Mobile-first media queries (600px, 900px, 1200px):** control columns, navigation and footer layout across the whole stylesheet.
- **Fluid typography with `clamp()`:** headings and body text scale smoothly with the screen.
- **Intrinsic grids (`auto-fit` with `minmax()`):** the "At a glance" strip and the "Getting around" cards reflow on their own, with no media query.
- **Fixed-column grids that change at breakpoints:** food cards go from 1 to 2 to 3 columns.
- **Container queries (`@container`):** each place card switches to a side-by-side layout based on its own width, not the screen width.
- **Art-directed images (`<picture>`):** the hero shows a tall crop on phones and a wide crop on larger screens.
- **Resolution switching (`srcset` and `sizes`):** the Marine Drive banner loads a 480, 800 or 1200px wide image.
- **Fluid images:** `max-width: 100%` and `height: auto` on every image, with width and height attributes set to avoid layout shift. The train illustration is cropped, not squashed, on narrow screens.
- **Responsive table:** the train lines turn into stacked cards on phones and a real table from 600px.
- **Fluid spacing:** `min()`, `clamp()` and CSS variables control page gutters and section spacing.
- **Feature queries:** `hover: hover`, `orientation: landscape`, `prefers-reduced-motion` and `print`.
- **Accessibility:** skip link, semantic landmarks, labelled sections, visible focus styles and reduced-motion support.

## Breakpoints

- **Under 600px:** one column, navigation links wrap into pill buttons, stacked train cards.
- **600px and up:** two-column food cards, a real train table, horizontal place cards.
- **900px and up:** sticky one-row navigation bar, three-column food cards, two-column places, sticky sidebar.
- **1200px and up:** three-column places grid and wider spacing.

The footer shows which layout is currently active, which makes testing easier.

## Assets

All artwork was created for this project as scalable SVG, so it stays sharp at any screen size and weighs very little.

- **Food illustrations (6):** `assets/food/` for the menu cards (vada pav, pav bhaji, misal pav, bhel puri, bun maska, Irani chai).
- **Place illustrations (6):** `assets/places/` for the place cards (Gateway of India, Marine Drive, Elephanta Caves, CSMT, Haji Ali, Sanjay Gandhi National Park).
- **Hero artwork (2 crops):** `assets/hero-tall.svg` and `assets/hero-wide.svg`, art-directed with `<picture>`.
- **Banner art (3 sizes):** `assets/marine-480.jpg`, `assets/marine-800.jpg` and `assets/marine-1200.jpg`, used for resolution switching with `srcset`.
- **Local train:** `assets/local-train.svg` in the train section.
- **Kaali-peeli taxi:** `assets/taxi.svg` in the quick tips panel.
- **Transport icons (6):** `assets/icons/` for the "Getting around" cards.
- **Warli folk-art patterns (2):** `assets/warli-ink.svg` and `assets/warli-light.svg` as tiled backgrounds.
- **Favicon and share image:** `assets/favicon.svg` and `assets/og-image.png` for the browser tab and link previews.

## Project structure

```
amchi-mumbai/
├── index.html
├── styles.css      # Mobile-first, organised into 14 numbered sections
├── assets/
│   ├── food/  places/  icons/
│   └── hero, banner, train, taxi, patterns, favicon, share image
└── README.md
```

## Run it

Open `index.html` in any modern browser. No build step, no JavaScript and no dependencies. Web fonts (Yatra One and Mukta) load from Google Fonts and fall back to system fonts when offline.

## Author

Prashansa Raut | Frontend Web Development Intern, Yuva Intern
