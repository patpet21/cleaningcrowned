# Cleaning Crowned

Responsive static website for Cleaning Crowned in New Jersey. The luxury visual redesign is maintained in this repository; the older `patpet21/crownedcleaning` repository is left unchanged.

## Pages
- `index.html` — homepage, services, benefits, and calls to action.
- `booking.html` — responsive quote request form that posts to the business's Formspree endpoint.
- `about.html` — company information.
- `contact.html` — verified contact methods and location (verify details before launch).
- `thank-you.html` — branded success page; the browser redirects here only after a successful AJAX response from Formspree (JavaScript is required for this custom redirect).
- `style.css` — editorial luxury palette, typography and mobile-first responsive design.
- `assets/crown-mark.svg` — original simplified, scalable website crown mark. The reference artwork supplied by the owner says “Crowned Cleaning” (reverse order), so this new mark is paired with the correct **Cleaning Crowned** text in HTML.
- `site.js` — mobile navigation, service preselection and Formspree success/error handling.

## Launch checklist (important)
1. Confirmed website contact details supplied by the owner: `+1 (551) 449-2066`, `cleaningcrownedvip@gmail.com`, and `Clifton, NJ`. Formspree notification recipient remains independently managed in the Formspree account.
2. Netlify is used for **hosting only**. The quote form uses the supplied Formspree endpoint (`https://formspree.io/f/xbglyayz`). Its JavaScript submission waits for a successful Formspree response before redirecting to `thank-you.html`; errors display a retry message without losing the entered fields. With JavaScript disabled, standard Formspree confirmation appears. Confirm the form is active in Formspree and its notification email is set to the business's monitored inbox. Submit a real test request on the published site and confirm receipt; repository review alone does not validate delivery. The form is an estimate request, not an appointment booking.
3. Confirm the services advertised and actual service ZIP codes with the business owner. Do not add testimonials, insurance/licensing claims, or discounts unless substantiated.
4. Test mobile layout and navigation at 320, 375, 390, 768, and 1280 px, as well as phone/email links, service preselection, and the Formspree submission on the live site.
5. The homepage currently displays editorial interior photos from Unsplash rather than photos of completed Cleaning Crowned jobs. Verify photo licensing and replace with original business photos when available. The reference 3D logo was not used in the mobile navigation because its wording is reversed and fine details would not render well at small sizes. Add a privacy notice for contact form submissions.
6. Do not display customer testimonials, review scores, insurance credentials, discounts or numerical business claims unless the business can substantiate them.

The previous `booking.js` is legacy code and is no longer loaded by the redesigned pages. Its localStorage approach is **not** a working way to send bookings to the business.

## Development
The site is static HTML, CSS and JavaScript; no build command required. For Netlify publish the repository root directory.

## Detailed service pages and link previews
Six detailed service pages link from six homepage cards. Each service has a Home/Services breadcrumb, typical cleaning tasks, intended use cases, and a preselected Formspree quote CTA. Review inclusions with the business before committing to a customer. Open Graph/Twitter metadata references the approved public luxury banner; confirm the image is reachable and note that social apps may cache old previews. No invented reviews, metrics, qualifications, or guarantees.

## Social preview and contact details

The social image used by all public pages is the owner-provided luxury banner at `https://i.ibb.co/278GgjTg/Chat-GPT-Image-Sep-23-2026-11-32-47-AM.png` (1731 × 909). Social crawlers can cache prior previews. The canonical and Open Graph URLs still use the existing Netlify site; update these to `https://cleaningcrowned.com/` when the custom domain is confirmed live and canonical.

The public contact email is `cleaningcrownedvip@gmail.com`, phone `+1 (551) 449-2066` (tel:+15514492066), and location `Clifton, NJ`. Formspree independently manages the destination of form notifications; verify its recipient in the Formspree dashboard. Three lightweight SVG pictograms provide matching luxury-style icons in the contact cards and site footer.
