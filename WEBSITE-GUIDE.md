# WINGSPAN HOLIDAYS — website guide

## Format
This workspace runs React with TanStack Start. This download is the complete supported project source, not the requested standalone index.html/style.css/script.js format. It cannot be opened by double-clicking an HTML file.

## Open locally
1. Install Bun from https://bun.sh.
2. Extract the source ZIP into a folder.
3. Open a terminal in that folder and run `bun install`.
4. Run `bun run dev -- --host 0.0.0.0 --port 8080`.
5. Open http://localhost:8080 in your browser.

## Edit the website
- Destination names, descriptions, highlights, sample itineraries and image imports: `src/lib/travel.ts`.
- Company phone, email, WhatsApp number and Instagram profile: `company` in `src/lib/travel.ts`. Some displayed contact details and links also appear in `src/routes/index.tsx`; update those together.
- Package duration, hotel/flight wording, inclusions, exclusions and “Contact for Price”: the package section in `src/routes/index.tsx`. All current itineraries are sample information. Verify and replace it with your actual offers; do not imply hotels/flights are confirmed before confirmation.
- Photos: replace files in `src/assets/`, or import new local photographs in `src/lib/travel.ts`. Hero and about photographs are imported in `src/routes/index.tsx`. Current destination photos are AI-generated illustrative imagery, not hotel/property proof.
- Colors, spacing and typography: semantic variables and rules in `src/styles.css`.
- Enquiry fields and formatted WhatsApp message: `src/components/enquiry-form.tsx`.
- Creator credit and creator WhatsApp link: footer in `src/routes/index.tsx`.
- Browser title and social descriptions: `head()` in `src/routes/index.tsx`.

## Enquiries and reviews
The enquiry form validates required fields, phone number, date, traveler/night counts and selected services. It opens WhatsApp with the details for the customer to review and send. It does not save enquiries, send email or confirm bookings. If a popup is blocked, the review link remains available in the form.

All three testimonial cards are visibly labeled placeholders, not real customer reviews. Replace only with genuine reviews you have permission to publish.

## Checks
Run `bun run test` for project tests. Test the WhatsApp links on a phone with WhatsApp installed before sharing the website publicly. Local checks verified destination dialogs, mobile navigation, valid/invalid enquiry behavior, formatted WhatsApp links and image loading. Sending a real WhatsApp message was intentionally not performed.
