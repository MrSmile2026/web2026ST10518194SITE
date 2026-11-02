# KO TECH — WEDE5020 Part 3 POE

**Project owner:** ST10518194 NJABULO SABELO SHANDU

**Student:** Njabulo Sabelo Shandu  
**Student number:** ST10518194  
**Module:** Web Development (Introduction), WEDE5020  
**Project:** KO TECH ecommerce showcase (HTML, CSS, JavaScript)  
**Assessment:** Part 3 Portfolio of Evidence, 2026

## 2026-11-02 assessment upgrade
This version was reviewed against the supplied Part 3 rubric. It adds:
- Page-specific metadata and robots exclusion for duplicate/private support pages.
- Complete Netlify Forms field matching, bot-field traps, clearer local-preview errors, focus styling and form feedback.
- `IMAGE-ATTRIBUTION-REGISTER.csv` containing all project image paths for genuine source verification.
- `PART2-FEEDBACK-EVIDENCE.md` and `SUBMISSION-EVIDENCE-GUIDE.md` for non-fabricated assessment evidence.
- `tests/check_project.py`, `tests/test_interactions.py`, and a GitHub Actions validation workflow.
- Local design previews under `evidence/` clearly labelled as local, not live deployment proof.

**Result:** 760/760 static checks and 29/29 isolated-browser interaction checks passed in this environment. These checks do not represent an official lecturer score or prove live email, Netlify, GitHub or Supabase completion.

For the remaining evidence steps needed to target the highest marking band, **read `SUBMISSION-EVIDENCE-GUIDE.md` before handing in**.

## Project summary
A responsive ecommerce demonstration specialising in computers, gaming, phones, wearables, headphones and accessories. The glossy orange gallery showcases imagery in two animated rows, while the catalogue has live search, category filters, sorting, pagination and product detail views. Cart, wishlist, checkout, PDF order slips displaying purchased items, demo tracking, and accessibility enhancements are included.

> **Important:** This project does **not** process bank/card payments. Prices are demonstration prices and checkout records an order *request*. The site is in local-preview mode until Supabase is configured.

## Get started in Visual Studio Code
1. Extract the ZIP. Open the extracted folder in VS Code (**File > Open Folder**).
2. Open the terminal and run `python -m http.server 8000` (or use VS Code Live Server). This is preferable to directly opening `file://` because browser storage and network features need a web origin.
3. Open `http://localhost:8000/` in a browser. No npm installation or build step is needed.
4. All site assets are relative paths and all deployed filenames are URL-safe.

## Netlify deployment
1. Extract the folder. In Netlify Drop (`https://app.netlify.com/drop`), drag the **extracted folder**, not the ZIP.
2. For a Git-based Netlify deployment, push the *contents of this folder* to a GitHub repository. Set the publish directory to `.` (project root); `netlify.toml` contains the setting. No build command is required.
3. **Forms:** On the Netlify site dashboard choose **Forms > Enable form detection**; deploy again. Netlify reads `netlify-forms.html` (a static definition for the two dynamically rendered forms). Test a submission from the live Netlify URL and check **Forms > Active forms**.
4. **Contact form email:** Under **Forms > Submission notifications > Add notification**, select **Email notification**, enter an email address owned by the store/project owner, and select `ko-tech-contact` and/or `ko-tech-enquiry`. Test with a new submission; email is *not* automatically enabled by uploading files. Do not add personal email addresses to source code.
5. To make customer accounts and persistent orders work across devices, complete `SETUP-ACCOUNTS.md`, run `setup/ko-tech-supabase.sql`, and provide your **public** Supabase config in `js/backend-config.js`. Never upload private API keys.
6. The `Admin.html` page is a legacy Node.js feature, not a working Netlify admin dashboard; status updates are managed through the authenticated Supabase dashboard as explained in setup. No background push/email for orders is installed.

## Key pages
- `index.html` — home and featured products.
- `Product.html`, `Product-Details.html`, `Deals.html`, `product-new.html` — searchable catalogue, product details, deals and new arrivals.
- `Gallery.html` — glossy orange carousel strips, hover interactions and keyboard-operable lightbox with next/previous controls.
- `Contact.html` — validated contact form, OpenStreetMap interactive map, local-area selector and accessibility hints.
- `Enquiry.html` — product enquiry form with category, contact preference, validation and response.
- `Cart.html`, `Wishlist.html`, `Checkout.html`, `Order-Confirmation.html` — shopping and order PDF.
- `Track-Order.html`, `Account.html` — order progress and notifications (persistent with Supabase, demo locally).
- `References.html` — Harvard-style documentation references.

## Functions and accessibility
- Cart/wishlist browser storage; product filtering and live search; modal gallery; keyboard support; responsive layout; navigation and toasts.
- Required form fields and HTML constraints (email/phone, lengths, consent where appropriate); additional per-field inline feedback with `aria-invalid` and `aria-live`.
- Native OpenStreetMap iframe provides pan/zoom; area tabs select Durban city, Umhlanga and Ballito **map areas**; the map does *not* claim an exact shop address.
- Images have text alternatives; page titles, meta descriptions and relevant meta keywords are included; account/private pages are marked noindex.
- Reduced-motion support for animated gallery.

## Verification and evidence
See `RUBRIC-CHECKLIST.md`, `CHANGELOG.md`, `TEST-RESULTS.md`, and `REFERENCES.md` for evidence. The automated checks confirm static paths, filename safety and script syntax; manual browser testing on Netlify is still required for real submissions, Supabase login and email delivery.

## Development / GitHub workflow
This ZIP does not contain fabricated GitHub history. For genuine descriptive commits, upload project files to your GitHub repository, then make *new actual changes* and commit with meaningful messages such as `docs: document POE criteria`, `fix: validate enquiry fields`, `feat: improve interactive map`. Preserve existing real commits if you already have them. Screenshots of GitHub commit history and your live Netlify URL should accompany your submission.

## Technologies
HTML5; CSS3; vanilla JavaScript; Font Awesome classes from the original design; Google Fonts Poppins; OpenStreetMap; Netlify Forms; Supabase (optional secure accounts/orders); custom browser-side PDF generation in `js/slip.js`. See `REFERENCES.md` for documentation URLs.

## Source code comments and student attribution
- Every HTML page includes its purpose and commented document landmarks.
- CSS, JavaScript, SQL, the Netlify configuration and favicon carry the student ID and name.
- Comments beside important functions explain page rendering, validation, authentication, orders, PDF generation and tracking.
- All customer-facing pages show the student ID and full name at the bottom of the footer.
- The static references page also displays the name; the Netlify form definitions are a technical, hidden page.
- `js/pdf-font.js` and `js/original-design.js` contain machine-generated/serialized data; their headers explain their purpose without changing those encoded payloads.

Do not enter private Supabase service-role keys into client-side files. Real accounts and online order storage require the configuration described in `SETUP-ACCOUNTS.md`.
