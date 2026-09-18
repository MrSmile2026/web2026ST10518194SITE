# KO TECH — Responsive E-Commerce Website

**Student:** NJABULO SHANDU  
**Student Number:** ST10518194  
**Project:** Web Development / KO TECH E-Commerce Website

## 1. Project overview

KO TECH is a responsive front-end e-commerce website for technology products and accessories. The project contains a home page, product catalogue, product details, deals, cart, wishlist, checkout, payment methods, order confirmation, tracking, account registration/sign-in, reviews, contact and about pages.

The project is implemented with HTML5, one shared external CSS stylesheet (`style.css`) and a shared JavaScript file (`auth.js`). The design uses a consistent desktop visual system and responsive breakpoints for tablets and mobile screens.

## 2. Main files

- `1Index.html` — home page
- `Product.html` — product catalogue
- `PRODUCT NEW.html` — alternate product catalogue page retained from the original project
- `Product-Details.html` — product details
- `Deals.html` — deals page
- `About.html` — about page
- `Contact.html` — contact page
- `Cart.html` — shopping cart
- `Wishlist.html` — wishlist
- `Checkout.html` — checkout
- `Payment-Methods.html` — payment information
- `Order-Confirmation.html` — order confirmation
- `Track-Order.html` — order tracking
- `Login.html` — sign in
- `Register.html` — registration
- `Reviews.html` — reviews
- `style.css` — shared external stylesheet used by every HTML page
- `auth.js` — shared front-end functionality and responsive menu behaviour
- `Images/` — product, brand and interface images
- `README.md` — project information and rubric evidence
- `CHANGELOG.md` — development record
- `REFERENCES.md` — external resources used during development
- `PART2-FEEDBACK.md` — Part 1 feedback/improvement record

## 3. How to run the website

1. Extract the ZIP folder.
2. Open `1Index.html` in a modern web browser.
3. Navigate using the desktop navigation or the mobile menu.
4. Registration, cart, wishlist and demo order data are stored in the browser's local storage. There is no production database or real payment gateway.

## 4. Responsive design evidence

### Images — 5 marks

Images use responsive rules such as `max-width: 100%` and `height: auto`. Product cards use `object-fit: contain` so product images remain visible without distortion. Product-detail images have a responsive maximum height. Image rules are applied globally and refined at mobile breakpoints.

### Layout — 5 marks

The site uses flexible rows, responsive containers and a responsive product grid. Product cards use CSS Grid with four columns on wide screens, three on medium screens, two on smaller screens and one on very narrow screens. Forms wrap and the cart table is horizontally scrollable on small displays.

### Typography — 5 marks

Typography is controlled centrally in `style.css`. Heading sizes use `clamp()` so text scales between desktop and mobile sizes. Body text has a consistent line height, and mobile breakpoints reduce the base font size and heading dimensions for readability.

### Navigation menu — 5 marks

The navigation collapses below 800px. A native `<button>` opens and closes the menu, has an accessible label and `aria-expanded` state, and works with keyboard focus. The menu is full-width on mobile and remains a horizontal navigation on larger screens.

## 5. Desktop CSS styling evidence

### Typography styles — 5 marks

`style.css` defines font family, heading hierarchy, font sizes, weights, line heights, link states, buttons and form typography.

### Layout structure — 5 marks

The stylesheet defines containers, rows, columns, product grids, cards, forms, footer columns and page-specific layouts using Flexbox and CSS Grid.

### Decoration and colour — 5 marks

The project uses a consistent KO TECH colour system based on the brand orange, neutral text, white surfaces, borders, shadows, rounded corners, hover states and gradients.

### External stylesheet — 10 marks

Every HTML page links to the same external `style.css`. Styling is not dependent on a page-specific CSS file. The previously duplicated unused `style NEW.css` file was removed to keep `style.css` as the single canonical stylesheet.

### Default style code — 5 marks

`style.css` begins with a CSS reset/default rules and establishes body font, colour, spacing, box sizing, links, paragraphs, headings, images and form controls. CSS variables provide a consistent default design system.

## 6. GitHub and development record

The supplied project includes a Git history with descriptive commits. The commit history is intended to be pushed to the student's GitHub repository so the assessor can inspect the development record directly.

Suggested descriptive commits included in the project history are:

1. `Initial KO TECH website structure and pages`
2. `Add shared interactive site functionality and mobile menu support`
3. `Improve responsive navigation accessibility and mobile layout`
4. `Add rubric documentation and development evidence`
5. `Final responsive image and layout validation`

When submitting through GitHub, push the repository rather than uploading only individual files so that the commit history is preserved.

## 7. Part 2 / feedback response

Part 2 improvements are documented in `PART2-FEEDBACK.md`. The changes focus on responsive images, responsive layout, typography, mobile navigation, consistent external CSS, accessibility, documentation and functional JavaScript.

## 8. References and assets

Development references and external resources are listed in `REFERENCES.md`. Product images and other media are stored under the project `Images/` folder. The project does not claim ownership of third-party product imagery; such material is included for the academic demonstration website.

## 9. Accessibility improvements

- Semantic buttons are used for the mobile menu.
- Navigation has `aria-label`.
- Menu state is exposed with `aria-expanded`.
- Images include alternative text where an image conveys information.
- Keyboard focus styles are defined for links, buttons and form controls.
- Form controls use labels/placeholders and required validation where appropriate.

## 10. Validation checklist

- [x] All HTML pages use the shared external `style.css`.
- [x] All HTML pages contain a responsive viewport declaration.
- [x] Images have responsive sizing rules.
- [x] Product layout changes across desktop, tablet and mobile breakpoints.
- [x] Typography scales at responsive breakpoints.
- [x] Mobile navigation collapses and expands below 800px.
- [x] `auth.js` is included and provides shared front-end functionality.
- [x] README, changelog, references and Part 2 documentation are included.
- [x] Git history contains descriptive development commits.

## 11. Modern UI refinement

The final presentation layer adds a cohesive modern visual system while preserving the original KO TECH content and page set. It uses CSS custom properties, responsive containers, rounded product surfaces, consistent spacing, accessible focus states, touch-friendly navigation, responsive product imagery, modern form controls, and reduced-motion support. These improvements directly reinforce the rubric categories for desktop styling, responsive layout, typography, images, navigation and external stylesheet implementation.
