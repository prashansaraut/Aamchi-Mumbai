# Amchi Mumbai

A fully responsive city guide to Mumbai's street food, landmark places and local train network. Built from scratch with semantic HTML5 and modern CSS only (no JavaScript, no frameworks) as the Week 2 task of the Yuva Intern frontend programme (implementation of responsive web design).

The design takes its look from the city itself: the black-and-yellow *kaali-peeli* taxi (checker stripes, hard shadows), Devanagari lettering and a sunset over the Arabian Sea.

## Responsive techniques used

| Technique | Where it is used |
|---|---|
| Mobile-first media queries (600px, 900px, 1200px) | Whole stylesheet: columns, navigation, footer |
| Fluid typography with `clamp()` | Headings and body text scale smoothly with the screen |
| Flexible grids (`auto-fit` with `minmax()`) | "At a glance" strip (two tidy columns between 600 and 899px) |
| Fixed-column grids that change at breakpoints | Food cards: 1, 2 then 3 columns |
| Container queries (`@container`) | Place cards switch to a side-by-side layout based on their own width |
| Art-directed images (`<picture>`) | Hero shows a tall crop on phones and a wide crop on larger screens |
| Resolution switching (`srcset` and `sizes`) | Marine Drive banner loads 480, 800 or 1200px wide |
| Fluid images (`max-width: 100%`, `height: auto`) | All images, with width and height set to avoid layout shift |
| Intrinsic grid (`auto-fit`, no media query) | "Getting around" cards reflow from 1 to 3 columns on their own |
| Responsive table | Train lines turn into stacked cards on phones |
| Fluid spacing (`min()`, `clamp()`, CSS variables) | Page gutters and section spacing |
| Feature queries | `hover: hover`, `orientation: landscape`, `prefers-reduced-motion`, `print` |
| Accessibility | Skip link, semantic landmarks, labelled sections, visible focus styles, `prefers-reduced-motion` |

## Breakpoints

| Range | Layout |
|---|---|
| Under 600px | One column, navigation links wrap into pill buttons, stacked train cards |
| 600px and up | Two-column food cards, real train table, horizontal place cards |
| 900px and up | Sticky one-row navigation bar, three-column food cards, two-column places, sticky sidebar |
| 1200px and up | Three-column places grid, wider spacing |

The footer shows which layout is currently active, which makes testing easier.

## Testing

Checked at 11 viewport widths from 320px to 1920px (phones, tablets, laptops, desktops), in landscape on a phone, at 200% zoom and in print preview. No horizontal scrolling at any size. `html-validate` reports no HTML errors and an axe-core accessibility scan reports no violations. Full details are in the Week 2 report.

## Assets

All artwork was created for this project as scalable SVG, so it stays sharp at any screen size and weighs very little.

| Asset | Files | Used for |
|---|---|---|
| Food illustrations (6) | `assets/food/` | Menu cards: vada pav, pav bhaji, misal pav, bhel puri, bun maska, Irani chai |
| Place illustrations (6) | `assets/places/` | Place cards: Gateway of India, Marine Drive, Elephanta Caves, CSMT, Haji Ali, Sanjay Gandhi National Park |
| Hero artwork (2 crops) | `assets/hero-tall.svg`, `assets/hero-wide.svg` | Art-directed with `<picture>` |
| Banner photo-style art (3 sizes) | `assets/marine-480.jpg`, `-800.jpg`, `-1200.jpg` | Resolution switching with `srcset` and `sizes` |
| Local train | `assets/local-train.svg` | Train section, cropped on narrow screens |
| Kaali-peeli taxi | `assets/taxi.svg` | Quick tips panel |
| Transport icons (6) | `assets/icons/` | Getting around cards |
| Warli folk-art patterns (2) | `assets/warli-ink.svg`, `assets/warli-light.svg` | Tiled backgrounds on the hero and train section |
| Favicon and share image | `assets/favicon.svg`, `assets/og-image.png` | Browser tab and link previews |

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
