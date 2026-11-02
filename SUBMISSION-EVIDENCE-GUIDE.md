# WEDE5020 — Final submission and evidence checklist

**Owner:** ST10518194 NJABULO SABELO SHANDU  
**Goal:** Present honest, verifiable evidence for each marking criterion.  
**Status:** Website source has been improved and checked locally. An assessment score of 99% cannot be verified or promised before the external steps below are completed.

## 1. Prove Part 2 feedback was addressed
Open `PART2-FEEDBACK-EVIDENCE.md`, paste the lecturer's **actual words**, then link the specific changed file/page and a screenshot. The supplied rubric screenshots are not the lecturer's feedback. Do not make up feedback.

## 2. Publish a working website
1. Extract this ZIP and drag the extracted **folder** to https://app.netlify.com/drop . If your site uses a GitHub repository, prefer publishing the repository instead.
2. Open the live Netlify URL and check `index.html`, `Product.html`, `Gallery.html`, `Contact.html`, `Enquiry.html`, `Cart.html`, `Track-Order.html` and `References.html`.
3. Capture a screenshot with the live URL visible. Copy the public URL into your POE submission. **A local screenshot is not proof of deployment.**

## 3. Verify contact/enquiry email processing
1. In the Netlify dashboard, go to **Forms** and enable automatic form detection. **Deploy the site again** to register the two static forms.
2. Under **Forms > Submission notifications**, add an **Email notification** to an email address you actually own. Select both `ko-tech-contact` and `ko-tech-enquiry` (or one notification per form).
3. Submit realistic test messages through both forms from your live domain, then verify each submission under **Forms > Active forms** (including the Spam tab if necessary).
4. Check the destination mailbox for the notification, including spam/junk. Capture a screenshot of a verified form submission and delivered notification without exposing customer data.
5. **Do not claim test emails are delivered** if they were never received. Netlify's notification recipient is a dashboard setting, not a code value.

## 4. GitHub evidence: genuine descriptive commits
1. Create a GitHub repository under your own account. Do not accidentally commit any private API keys, emails or passwords.
2. Push the project; after making genuine changes, commit each change with a descriptive message and push it. Examples: `feat: improve KO TECH forms and SEO`, `test: add browser and static validation`, `docs: document rubric evidence and attribution`. Do not fake old timestamps or a lecturer's work.
3. Capture the repository URL, meaningful commit history and a green GitHub Actions validation run. `tests/check_project.py` runs automatically via `.github/workflows/validate.yml`.

### GitHub commands (new repository)
```bash
git init
git add .
git commit -m "feat: submit KO TECH rubric-aligned website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```
Replace the placeholder repository URL with the real one. For existing Git repositories, retain their original history; do not run `git init` or overwrite the existing repository.

## 5. Image references and permissions
Open `IMAGE-ATTRIBUTION-REGISTER.csv` and enter the genuine original image source/creator, URL, licence and verification status for each image. Unknown source fields are intentionally blank. Do not invent licences. Use your own/licensed photos if sources cannot be verified. Update `IMAGE-SOURCES.md` and `REFERENCES.md` accordingly.

## 6. Accounts and live orders (extra functionality)
The ordering demo works in browser storage, but **real cross-device accounts and orders require Supabase**. Follow `SETUP-ACCOUNTS.md`; test registering, signing in, placing a demo order, tracking the status and downloading a PDF on your actual hosted domain. Do not put Supabase service-role secrets in JavaScript. No real card payments are collected.

## 7. Test evidence and scope
- Local isolated-browser tests: `python tests/test_interactions.py` — gallery, search, map, forms and tracking.
- Static checks: `python tests/check_project.py` — local links, assets, SEO fields, Netlify form registration, filenames and JS syntax.
- `evidence/Gallery-local-preview.png` and `evidence/Contact-local-preview.png` are **local design previews**, not screenshots from a live URL.
- Run mobile and desktop checks yourself after deployment. Test external map tiles and any email/service integrations on the real deployed website.

## Final handwritten/lecturer items still missing
- [ ] Actual Part 2 lecturer feedback and proof of changes
- [ ] Live Netlify URL and proof of successful deployment
- [ ] Confirmed Contact/Enquiry submission and received email notification
- [ ] GitHub repository URL and genuine descriptive commits
- [ ] Verified original source links and rights for all third-party images
- [ ] Supabase configured if you claim working real accounts/orders

**Academic integrity:** The above external evidence must be genuine. A ZIP of code alone cannot establish the lecturer's final marks.
