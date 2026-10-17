# Design options for review

These are isolated samples of the three sections in the supplied references. `Glowdom-preview.html`, the original HTML, and `main` remain unchanged. No option has been applied to the full page or published as a website.

## Pictures

- `button-alternatives.png`: A — solid sage; B — sage outline; C — muted plum.
- `sage-layout.png`: proposed spacing, typography, arch decoration and icon size with sage buttons.
- `outline-layout.png`: the same sample with sage-outline buttons.
- `plum-layout.png`: the same sample with muted-plum buttons.
- `mobile-layout.png`: compact mobile sample with sage buttons.

`Glowdom-options.html` is self-contained. Its three colour buttons update the sample enquiry button; they do not modify the main preview. Introductory-card links are display samples only in this partial-page mockup. Serve from the repository root and request `/previews/options/Glowdom-options.html` to try it locally.

## Proposed adjustments

Nine alternating fine rays follow the upper-right curve of each arch, with cream rays on sage cards and muted rose rays on the blush card. The photographs and 5:8 arch proportions are preserved.

Section padding is reduced from up to 100px to 40px on desktop and 32px on mobile. Section headings are 42.4px on desktop, reduced from up to 56px. Body text is 17px in the sample. Class icons are 80px instead of 44px. On mobile the class steps use a compact horizontal layout, with the enlarged icon alongside the text.

Button colours: A sage `#59674F`, B sage outline `#53634E` on cream, C muted plum `#76576F`.

## Checks

Chromium browser checks passed for all three colour selections, all embedded images, 27 curved ray lines, 5:8 card arches and 80px class icons. No horizontal overflow at 320, 390, 768, 1024 or 1440px. No uncaught JavaScript errors or external rendering requests. Desktop and mobile screenshots were visually reviewed.
