# Unpublished review — 20 October 2026

This branch is for review only. GitHub Pages remains on `design/gentle-refinements`; neither that branch nor `main` is changed by this review.

## Prepared revisions

- Small Group Class: £20 introductory price, replacing £15. The £80 one-to-one price is unchanged.
- Class enquiries panel: the existing soft sage green from the logo palette (`#E7E8DF`), replacing blush. Dark text and the sage enquiry button are retained.

## Revised using the selected botanical reference

- Removed the rejected large branch and all individual SVG sprigs.
- Created a transparent leaf frame from the supplied portrait botanical reference. Applied that frame around the left introduction panel of What is Face Yoga?, Who is Face Yoga For? and Health & Wellbeing. The text remains live HTML; the reference's sample text is not part of the image.
- The frame uses a CSS mask in the existing sage `#D4D3C7`, faded at 52% opacity. It fits each panel in full; no `cover` cropping is used. The source asset is `assets/botanical-reference-frame.png` and is embedded in the standalone HTML.
- Kept the crescent frame and added a less regular mixture of stars: five existing main accents and 23 irregular satellites, mixing four-point sparkles and fine eight-point stars like the circled example.
- The approved Face Workout icon is unchanged, with matching mauve colour and rendered stroke weight and no eyelash.
- Group panel remains soft sage and £20; One-to-One remains blush pink and £80. The practical questions remain expandable.

## Whole-page review

Reviewed the full-page desktop and mobile renders. Browser checks passed at 320, 390, 560, 768, 860, 861, 1024 and 1440 pixels with no horizontal overflow or JavaScript errors. All eight embedded images loaded; tall 5:8 introductory arches and section order are preserved. The expandable story, mobile menu, internal links, email-copy button and policy accordions work. No checkout, payment provider or external rendering request was introduced. Standalone and embedded Privacy Notice layouts also passed at 320, 390, 768 and 1440 pixels.

## Copy review

The Botox/fillers answer now advises following the treating practitioner's guidance instead of giving a fixed two-week interval or claiming treatment effects fade sooner. The pregnancy answer advises checking with a doctor or midwife when unsure, and discussing participation needs privately during consultation.

Dates remain enquiry-based, online classes are coming soon, and booking/cancellation terms are unchanged. The Privacy Notice wording is unchanged.

## Privacy Notice review

The embedded notice and standalone privacy.html describe Gül Ayan as the individual responsible, identify Gmail, Instagram, GitHub Pages and IONOS, explain the legal bases and explicit health-data consent, and give deletion criteria, rights and a complaint route. No notice wording has been changed in this review.

The notice describes a manual process that still needs to be followed: send the consultation form after booking/payment and before the first session, obtain separate affirmative consent before receiving health information, and manage deletion in both Gmail and the laptop. The supplied PDF form alone does not implement that separate consent. See CONSULTATION-EMAIL.txt and PRIVACY-OPERATIONS.md.

Payment arrangements remain undecided; identify any payment service and its data use before taking payment and update the notice where needed. International-transfer wording is general: confirm the arrangements applicable to the actual Google/Meta account services rather than treating this review as verification of their safeguards.

Avoid requesting a full medical history; collect only information relevant to participation. Consider omitting address and date of birth from a future simplified form unless a specific need is established. The current notice discloses those fields because they appear in the draft form.

This is a content and implementation review, not legal approval. No insurance assumption has been added.
