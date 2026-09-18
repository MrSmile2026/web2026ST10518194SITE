# KO TECH Development Changelog

## Commit 1 — Initial KO TECH website structure and pages
- Preserved the original 16 HTML pages and product/image assets.
- Kept the shared `style.css` architecture.
- Retained the existing ecommerce page structure and navigation.
- Confirmed responsive viewport metadata across pages.

## Commit 2 — Add shared interactive site functionality and mobile menu support
- Added `auth.js` as the shared JavaScript file.
- Added browser-local demo account, cart, wishlist, review, contact, order and tracking helpers.
- Added shared currency formatting.
- Added responsive menu behaviour.
- Added graceful local-storage handling.

## Commit 3 — Improve responsive navigation accessibility and mobile layout
- Replaced the mobile navigation image control with a native accessible `<button>`.
- Added `aria-expanded` and an accessible menu label.
- Added keyboard-visible focus styling.
- Added responsive navigation states below 800px.
- Added a `.contaniner` compatibility class for pages using the original spelling.
- Corrected the home-page video path so the local media file resolves from the project root.

## Commit 4 — Add rubric documentation and development evidence
- Added comprehensive `README.md`.
- Added `CHANGELOG.md`.
- Added `REFERENCES.md`.
- Added `PART2-FEEDBACK.md`.
- Added `.gitignore`.
- Documented the responsive image, layout, typography and navigation evidence.

## Commit 5 — Final responsive image and layout validation
- Verified all 16 HTML pages reference the same external `style.css`.
- Verified responsive viewport declarations.
- Verified image alternative text coverage.
- Verified responsive product-grid breakpoints.
- Verified local HTML asset references after HTML entity decoding.
- Verified CSS includes default styling, typography, layout, decoration and colour rules.

## Commit 6 — Modernise visual system and strengthen rubric alignment
- Introduced a cohesive 2026 design system using CSS custom properties for brand, surfaces, spacing, radius and shadows.
- Modernised the hero, navigation, product cards, calls-to-action, forms, offer section, testimonials and footer without removing existing site content.
- Added consistent responsive container aliases for both original `small-contain` / `contaniner` spellings and canonical classes.
- Improved product image presentation with responsive containment, consistent card surfaces and non-distorting object fitting.
- Refined mobile navigation, typography, spacing and touch targets for tablet and phone layouts.
- Added reduced-motion support and clearer keyboard/focus states for accessibility.

## 2026-09-16 — Responsive navigation refinement
- Added a reusable **All Pages** menu to every HTML page so every page is reachable from the site navigation.
- Added `navigation.js` for accessible menu toggle, Escape-to-close, outside-click close and resize handling.
- Refined responsive breakpoints so the desktop layout remains stable and only reflows when viewport width requires it.
- Added fluid media rules to prevent horizontal overflow and make images/video scale with their containers.
- Improved mobile navigation to a single-column, scrollable all-pages panel.
