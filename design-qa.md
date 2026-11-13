# Homepage design QA

final result: passed

**Findings**
- No actionable P0/P1/P2 differences found against the selected Minimal Light reference and approved content changes.

**Evidence and state**
- Source visual truth: `../Homepage_Template_Previews/minimal-light-desktop.jpg` (1280 × 720 pixels).
- Implementation: `docs/qa/desktop-top.jpg` (1280 × 720 pixels), plus `docs/qa/desktop-full.jpg` (1280 × 1436 pixels).
- Mobile implementation: `docs/qa/mobile-full.jpg`, captured in Chrome with a 390 × 844 CSS viewport, density 1.
- Route: `http://127.0.0.1:4000/`, initial page, light theme, no authentication required.
- Desktop CSS viewport: 1280 × 720, density 1. Both desktop images were inspected together in one comparison input at matching pixel sizes; no density normalization was needed.
- Full-view comparison retained the left profile/right content columns, serif type, navy headings, blue links, and white background. Focused crops were not needed: typography, photo, links, and margins were legible at native comparison size.
- Initial IAB screenshot output had a density/scaling problem. Replaced implementation evidence with Chrome screenshots before judging fidelity.

**Required fidelity surfaces**
- Fonts and typography: original Crimson Pro serif and Ubuntu Mono email style retained, with coherent heading weights and readable line heights. Titles wrap without truncation on mobile.
- Spacing and layout rhythm: desktop content starts at approximately x=470 and retains the 650px content column. Mobile stacks the centered profile above the content; 390px viewport and document scrollWidth both equal 390px. No horizontal overflow or overlapping content was observed.
- Colors and tokens: navy headings, blue links, neutral body text and white canvas match the reference. Focus outlines are present for keyboard use.
- Image quality and asset fidelity: supplied photograph is displayed via a circular CSS crop; the original image file is preserved. Face and upper body are clear. Social icons render correctly.
- Copy and content: approved three-paragraph biography, two research interests, two published papers, two working papers, and GitHub/LinkedIn are present. The second research interest is explicitly an emerging direction. Sample identities and unsupported social profiles are absent.

**Intentional deviations**
- The approved biography is longer than the sample, moving later sections below the initial viewport.
- Portrait increased to 160px on desktop and 144px on narrow mobile for recognizability.
- News and Services omitted because there is no supplied content; Working Papers added as requested.
- Paper thumbnails omitted because none were supplied; publication entries use the full content width.
- CV link remains conditional until a public CV is selected.

**Interactions and technical checks**
- Jekyll production build passed; generated local resource targets exist.
- Clicking the first publication Code link opened Gaojinhan/policy-cce-reproducibility and its matching paper description.
- Mobile image loaded successfully; all four content headings were present.
- Browser console errors/warnings: none on the local homepage.
- Remaining test gap: physical-device Safari has not been tested. GitHub Pages deployment validation is recorded separately by its workflow run.

**Comparison history**
- First normalized reference/implementation comparison: no actionable P0/P1/P2 findings; no visual fixes required afterward.
- Additional mobile review: passed; no changes required.

**Open Questions**
- None blocking release.

**Implementation Checklist**
- [x] Preserve selected template visual language.
- [x] Check desktop and mobile screenshots.
- [x] Verify content, loaded image, links, and console.
- [x] Record intentional differences.

**Follow-up Polish**
- None required for this release.
