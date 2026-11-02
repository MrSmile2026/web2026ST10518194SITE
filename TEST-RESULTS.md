# KO TECH — Assessment upgrade test report (2 November 2026)
**Student:** ST10518194 NJABULO SABELO SHANDU

- **Static verification:** 760 of 760 checks passed using `python tests/check_project.py`. This covers safe filenames, SEO fields, links/assets, Netlify form declarations, product/gallery asset paths and JavaScript syntax.
- **Isolated Chromium interaction verification:** 29 of 29 checks passed using `python tests/test_interactions.py`. This covers Gallery lightbox/arrow keys, product live search, zero-result feedback, form field validation, simulated successful form responses, OpenStreetMap iframe URL/region switching, and tracking page rendering.
- **Design checks:** `evidence/Gallery-local-preview.png` and `evidence/Contact-local-preview.png` were rendered locally with project CSS and images.

## What these tests do not verify
- The tests did not use a real Netlify URL; direct site navigation was blocked by the test environment.
- Form success responses were mocked; they do **not** prove that a real Netlify form submission or notification email was delivered.
- The OpenStreetMap iframe URL was verified but remote map tile loading was not.
- Supabase accounts/order persistence, payment services, email delivery, the site URL and GitHub activity require external configuration and human confirmation.
- Real third-party image provenance and actual lecturer Part 2 comments were not supplied.

See `SUBMISSION-EVIDENCE-GUIDE.md` for what to provide with the Portfolio of Evidence.
