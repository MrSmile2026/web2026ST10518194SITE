# WEDE5020 Part 3 POE — rubric checklist (provided screenshots)

**Student:** Njabulo Sabelo Shandu — ST10518194  
**Target:** Meet the highest marking band where testable. This checklist is self-audit evidence, not a lecturer's grade.  
**Assessment source:** 12 images from `new ko pic(2).zip` supplied by the student.

| Rubric criterion | Evidence in package | Status and conditions |
|---|---|---|
| Feedback on Part 2 / changelog | `CHANGELOG.md` | Implemented change log; actual marker feedback was **not supplied**, so correlation needs user evidence. |
| Interactive elements | Catalogue search, filters, pagination, cart, wishlist, checkout, notifications, tabs, menus, lightbox | Implemented; verify live interactions. |
| Interactive maps | `Contact.html` and `js/app.js` / `loadMap()` OpenStreetMap pan/zoom & 3 regional views | Implemented; internet required to display map tiles. City only, not a claimed physical business address. |
| Gallery lightbox | `Gallery.html`, `js/app.js` — open/close, next/prev, keyboard navigation | Implemented; static click test recommended. |
| Dynamic content and search | `Product.html`, `js/catalog.js`, `js/app.js` | Implemented; live typed search, filters, sorting and counts. |
| SEO: title tags | All HTML pages with distinct `<title>` | Implemented. |
| SEO: meta keywords | Unique per-page keyword tags | Implemented; rankings depend on many other factors. |
| SEO: meta description | Unique per-page description tags | Implemented. |
| SEO: filename and alt text | Lowercase/safe image names, descriptive product alt text and Gallery alt labels | Implemented; attribute sources still need licensing verification. |
| Enquiry: controls | `Enquiry.html`, dynamically generated form from `js/app.js` | Text inputs, email, phone, category, product, reply preference, message, consent. |
| Enquiry: validation | HTML constraints + `js/poe-enhancements.js` | Client-side native and inline live feedback. |
| Enquiry: process/response | `js/app.js`, `netlify-forms.html` | Can store via Netlify Forms after **enable + redeploy**. Feedback shown on successful response. |
| Contact: controls | `Contact.html`, `js/app.js` | Name, email, subject, message, labels and hints. |
| Contact: validation | `js/poe-enhancements.js` | Native + inline validation. |
| Contact: process email | Netlify Forms + `README.md` email notification setup | **Requires site owner to configure Netlify email recipient and verify live email**; not automatically complete in the ZIP. |
| GitHub: descriptive commits | `README.md` Git workflow, `CHANGELOG.md` | **Requires real GitHub repository and actual multiple commits**; a ZIP cannot create past history. |
| GitHub: README | `README.md` | Detailed overview, features, setup, pages, deployment, testing. |
| GitHub: Changelog | `CHANGELOG.md` | Concrete revisions and limitations, no invented feedback. |
| Website deployed | `netlify.toml`, root `index.html`, URL-safe files | Static deploy-ready; actual Netlify deployment must be performed and tested. |
| References | `REFERENCES.md`, `References.html`, `IMAGE-SOURCES.md` | Technical references in Harvard style; **third-party photo sources still need confirmed attribution**. |

## Final hand-in tasks that require your accounts
1. Deploy to your Netlify URL and save a screenshot of each page + Forms submission confirmation.
2. Enable Netlify Forms detection, then add email submission notification to your *own* address. Test Contact/Enquiry form and confirm email arrival.
3. Set up Supabase (optional rubric extension for account features), test registration/login and a saved order, status update, notification, and PDF.
4. Push to GitHub and make multiple **genuine** descriptive commits; include repository URL and a screenshot of commit history.
5. Insert your lecturer's actual Part 2 feedback and the changes made because of it.
6. Verify image attribution and licences; update `IMAGE-SOURCES.md` with original URLs.
7. Double-check all pages on a desktop and mobile browser; include resulting screenshots in submission.
