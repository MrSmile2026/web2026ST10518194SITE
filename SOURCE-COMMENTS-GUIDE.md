# KO TECH — source comments guide

**Student:** ST10518194 NJABULO SABELO SHANDU

This coursework submission contains a short explanation at the top of each HTML, CSS, JavaScript, SQL and configuration file. Major functions have additional comments that identify their responsibilities.

## Where to find the main features

- `index.html` and the other `*.html` files: document metadata, accessible landmarks and page placeholders.
- `js/app.js`: shared navigation/footer, cart, checkout, customer accounts, gallery, notifications and tracking.
- `js/catalog.js`: product information and images.
- `js/core.js`: pricing and validation logic.
- `js/cloud.js`: optional Supabase authentication/order integration.
- `js/slip.js`: order PDFs with purchased product details.
- `js/poe-enhancements.js`: accessible form validation.
- `style.css` and `assets/*.css`: layout, mobile responsiveness and gallery styling.
- `setup/ko-tech-supabase.sql`: optional database schema and server-side protections.
- `netlify.toml`: static-site publishing settings.

The student name appears in the visible footer on all customer-facing pages. The contact and enquiry form definitions are intentionally hidden from visitors and used by Netlify at build time.

**Important:** All comments have been written to explain existing code, not to replace or claim functionality that has not been activated. Supabase, Netlify Forms email notifications and a real deployment still require their own setup and verification.
