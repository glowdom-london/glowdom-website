# Glowdom gentle refinements

Design review only. No website deployment or publishing is configured by this change. The original `Glowdom Face Yoga5.html` and `README.md` remain unchanged.

## Review files

- `../Glowdom-preview.html`: self-contained HTML, with the original seven embedded images and all four font families embedded. The SIL Open Font License notices are retained inside the HTML. No external requests are needed to render the page.
- `desktop-top.png`: desktop opening view, 1440 × 1100.
- `desktop.png`: complete desktop page, 1440px wide.
- `mobile-top.png`: mobile opening view, 390 × 844.
- `mobile.png`: complete mobile page, 390px wide.
- `mobile-menu.png`: mobile navigation open, showing clearance beneath the original logo.
- `validation.json`: results of the Chromium interaction and responsive checks.

Serve locally with Python 3 from the checkout:

```sh
python3 -m http.server 8001 --bind 127.0.0.1 --directory .
```

Request `/Glowdom-preview.html` from that server. GitHub displays HTML source; it does not render this file as a published website. The screenshots are the visual review artifacts.

## Changes

The existing layout, logo, Meet Gül photographs, palette, and 5:8 introductory-card arches are retained. The hero photograph has space around it, with a small handwritten note and the original leaf artwork. Cards have 01–03 labels, fine rays and underlined links; the third heading is Small Group Classes.

The introduction welcomes a broader audience. East Sheen appears where it describes in-person class locations. Class calls to action use enquiries, dates remain to be confirmed, and online classes remain coming soon. Repeated biography copy is shorter and the expandable story is retained. Mobile menu links sit below the overlapping logo; Escape closes the menu.

The Privacy Notice states that consultation forms follow booking and payment, before the first session, and that explicit consent is requested before health information is submitted. Providers, storage arrangements, retention periods, lawful bases and consent-process details are explicitly pending confirmation. This draft must be completed and reviewed before publication; no providers or legal bases have been invented.

## Validation

Checked in installed Chromium via Playwright on 17 October 2026:

- All seven original image sources match the original HTML byte for byte and render successfully.
- Three introductory arches retain a width-to-height ratio of 5:8.
- All internal anchor targets exist.
- Personal story expands and collapses with matching accessibility state.
- Privacy disclosure opens and contains the consultation sequence and pending items.
- Mobile menu opens, its first link is clickable without the logo intercepting it, link selection closes the menu, and Escape closes it.
- No horizontal overflow at 320, 390, 560, 768, 860, 861, 1024 and 1440px widths.
- Email-copy interaction copies the correct email address over the local HTTP server.
- No uncaught JavaScript errors or external rendering requests.
- With network disabled, loading the HTML content directly into Chromium renders all embedded fonts and images; menu and story interactions pass. Direct file-URL navigation could not be checked because Chromium's environment policy blocks file URLs.

External Instagram/ICO destinations and any future booking, payment or consultation providers were not exercised. No booking/payment/form integrations were added.

## Community refinement

`A Little Glow, Together` is now a compact strip with one short paragraph and an Instagram link, with smaller type and less background padding. See `community-desktop.png` and `community-mobile.png`. Full-page screenshots have been refreshed. The section order remains unchanged pending review of the recommendation. Browser checks confirmed no overflow at 320, 390, 768, 1024 and 1440px; the personal story still expands and collapses, and no uncaught JavaScript errors occurred.
