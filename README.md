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
1. Confirm that `(201) 759-8569`, `cleaningcrownedvip@gmail.com`, and West New York are current company contact details. **Do not change the live email until the business creates and confirms its replacement.**
2. Netlify is used for **hosting only**. The quote form uses the supplied Formspree endpoint (`https://formspree.io/f/xbglyayz`). Its JavaScript submission waits for a successful Formspree response before redirecting to `thank-you.html`; errors display a retry message without losing the entered fields. With JavaScript disabled, standard Formspree confirmation appears. Confirm the form is active in Formspree and its notification email is set to the business's monitored inbox. Submit a real test request on the published site and confirm receipt; repository review alone does not validate delivery. The form is an estimate request, not an appointment booking.
3. Confirm the services advertised and actual service ZIP codes with the business owner. Do not add testimonials, insurance/licensing claims, or discounts unless substantiated.
4. Test mobile layout and navigation at 320, 375, 390, 768, and 1280 px, as well as phone/email links, service preselection, and the Formspree submission on the live site.
5. The homepage currently displays editorial interior photos from Unsplash rather than photos of completed Cleaning Crowned jobs. Verify photo licensing and replace with original business photos when available. The reference 3D logo was not used in the mobile navigation because its wording is reversed and fine details would not render well at small sizes. Add a privacy notice for contact form submissions.
6. Do not display customer testimonials, review scores, insurance credentials, discounts or numerical business claims unless the business can substantiate them.

The previous `booking.js` is legacy code and is no longer loaded by the redesigned pages. Its localStorage approach is **not** a working way to send bookings to the business.

## Development
The site is static HTML, CSS and JavaScript; no build command required. For Netlify publish the repository root directory.

## Detailed service pages and link previews
Six detailed service pages link from six homepage cards. Each service has a Home/Services breadcrumb, typical cleaning tasks, intended use cases, and a preselected Formspree quote CTA. Review inclusions with the business before committing to a customer. Open Graph/Twitter metadata references assets/social-preview.png for sharing on mobile; confirm the public asset is reachable and note that social apps may cache old previews. No invented reviews, metrics, qualifications, or guarantees.

## Current public domain and preview
Until `cleaningcrowned.com` is live, the canonical URLs and Open Graph preview point to `https://graceful-smakager-014814.netlify.app/`. Social image: `/assets/social-preview.png?v=5` (1200 × 630 PNG). Once the custom domain is connected and active, update canonical, `og:url`, `og:image`, `og:image:secure_url`, and `twitter:image` across all pages to the final domain and trigger a fresh social preview. Do not use the custom domain as canonical before it is active.

The public contact email is `cleaningcrownedvip@gmail.com`. Formspree manages the destination of quote form submissions separately; verify its recipient and notifications in the Formspree dashboard.
