# Homepage design QA — November 13 revision

final result: passed

**Findings**
- No actionable P0/P1/P2 differences remain against the selected Minimal Light design and the user's requested changes.

**Source and implementation evidence**
- Source visual truth: `../Homepage_Template_Previews/minimal-light-desktop.jpg`, 1280 × 720 pixels.
- User-provided figure truth: `assets/img/publications/simulation-auctions.png` (2034 × 1169) and `assets/img/publications/manufacturing-platformization.png` (1333 × 784). Copied unchanged in the requested first/second order.
- Desktop viewport: 1280 × 720 CSS pixels, density 1; `docs/qa/revision-desktop-top.jpg` is 1280 × 720, and `docs/qa/revision-desktop-full.jpg` is 1280 × 1674.
- Focused publication evidence: `docs/qa/revision-publications.jpg`, 1280 × 720, scrolled to Publications.
- Mobile viewport: 390 × 844 CSS pixels, density 1; `docs/qa/revision-mobile-full.jpg` is 390 × 3208.
- State: light theme, local homepage, no authentication required. Full-page desktop capture normalized to scrollY=0 so the fixed profile is in its correct initial position.
- Full-view comparison: source and revised top-of-page screenshot were inspected together in one comparison input at equal pixel dimensions. The source was also jointly inspected with the full revised page. Different copy length and the requested larger type intentionally move Publications below the first viewport. No density scaling was needed.
- Focused publication inspection confirmed the template's image-left/text-right arrangement and the two correct user figures. Small diagram labels are intentionally thumbnail-size; each thumbnail opens its original image in a separate tab.

**Required fidelity surfaces**
- Fonts and typography: Crimson Pro and Ubuntu Mono retained. Body and paper titles increased from 16px to 18px; related profile and link text scaled modestly. Heading hierarchy and line heights remain coherent; no truncation.
- Spacing and layout rhythm: original 650px content column and fixed desktop profile retained. Publication rows use a 160px image column, 20px gap, and flexible text column. At widths up to 600px, images stack above text and are limited to 320px. Mobile document width equals viewport width (390px).
- Colors and visual tokens: original navy headings, blue links, and neutral text retained. Previews have subtle neutral borders and shadows; focus outlines remain available.
- Image quality and asset fidelity: original PNGs are displayed at natural aspect ratios with no crop or generated replacement. Both load successfully. Photo remains unchanged.
- Copy and content: only the requested adviser hyperlink was added. Two published papers and two working papers remain in their original order. No thumbnails are invented for working papers.

**Interactions and checks**
- Jekyll production build passed. Only upstream Sass import deprecation warnings remain.
- Adviser link opened the Google Scholar page for Professor Mohamed EL MANSORI, Arts et Métiers ParisTech (ENSAM), with verified ensam.eu email.
- First preview click opened the original 2034 × 1169 PNG in a new tab.
- Keyboard Skip to content link activated successfully and returned the page to main content.
- Browser console errors/warnings on local homepage: none.
- Both desktop and mobile screenshots were visually inspected. Physical-device Safari is not covered.

**Comparison history**
- Initial release: passed against original template with approved content substitutions.
- User revision: larger typography, adviser Scholar link, and supplied publication images implemented.
- Initial full-page capture briefly omitted a lazy-painted offscreen image; inspecting Publications displayed both correctly. Captures were refreshed after visible rendering; no site fix was required.
- Initial full-page recapture was taken from a scrolled state; normalized to scrollY=0 before final desktop comparison.
- Revised desktop and mobile comparison: passed; no actionable visual fixes required.

**Open Questions**
- None blocking release.

**Implementation Checklist**
- [x] Add and verify the adviser Scholar link.
- [x] Enlarge body and related typography.
- [x] Add correct publication thumbnails and full-image links.
- [x] Verify responsive layout, images, keyboard link, and build.

**Follow-up Polish**
- None required for this revision.
