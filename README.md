# Community Needs Profile and Facility Mission

Extract this entire folder, then open index.html in a current browser. Keep assets, vendor, styles.css, content.js, and app.js alongside index.html. No build step, package installation, or internet connection is required to run the activity or download PDFs. External resource links require internet access.

## What is included

- Eight slides following the supplied storyboard.
- Fixed 1000 × 750 pixel activity; no scaling or responsive resizing. Smaller screens can scroll the surrounding page.
- Locally bundled Figtree font, including PDF fonts.
- Random assignment from the specified 30 cities, retained in local storage with all responses and the current slide.
- One open accordion at a time on slides 3–5. At least three complete indicators, with up to five entries. Extra blank or partial entries do not block navigation.
- Required nonblank responses in every field on the current slide before Next becomes available, except that Community Needs requires only three complete indicators. This checks completion, not evidence quality or citation accuracy.
- Resources tooltip visible on entry to slide 3, dismissible with Got it! or by opening Resources.
- Resources and fictional Portland, Oregon examples in editable pop-ups. Your Research opens previous research without losing current responses.
- Download PDF creates an actual PDF, using 8.5 × 11 inch portrait pages with margins and page numbers. Long responses continue on additional pages; the export is not forced onto a single page.
- Supplied city illustration used as the background on all eight slides at its native 1000 × 750 size.

## Editing

- content.js: Resources and Example pop-up text. The current example statistics, organizations, and citations are fictional placeholders, explicitly labeled as such. Replace with verified examples before student use.
- app.js: slide copy, field labels, city list, navigation, persistence, and PDF export.
- styles.css: colors, spacing, dimensions, and font. The background is assets/background.png, displayed at 1000 × 750 in the #activity rule.
- index.html: document shell and script references.

## Saving and hosting

The storage key is hsm3350-community-needs-v1. Work is saved after every response edit and slide change. Data stay in the same browser profile and origin; they do not sync to another device or browser. Private browsing, blocked browser storage, clearing browser data, moving the activity to a different origin, or changing its local file path can affect saved work. Saving runs silently; storage failures are logged to the browser console.

For dependable student use, host the complete folder together at a stable HTTPS location with browser storage and downloads enabled. If embedded, use a frame sized at least 1000 × 750 and allow downloads. Students submit their downloaded PDF to Canvas; this package does not send submissions or grades automatically. No SCORM integration is included.

## Validation

Programmatic DOM checks passed for the eight-slide flow, required fields, accordion exclusivity, five-indicator flow, pop-ups, research review, city and response persistence, resume, and PDF generation. Normal and long-response PDF exports were verified as US Letter with text within page margins and the last response retained. Full visual browser testing could not run in the build environment; check the extracted activity in your intended browser before release.

## Third-party licenses

Figtree: SIL Open Font License, included in assets/OFL.txt.
jsPDF: MIT License, included in vendor/LICENSE-jspdf.txt. Library version 3.0.4, bundled locally.

## Visual refinements

Routine save messages and required-field helper text are omitted. Required-field navigation checks remain active. Inputs and textareas stretch to the same height as their orange labels. Slide changes are immediate, without entry animations. Subtle transitions remain for the assigned city, accordion expansion/collapse, chevrons, and pop-ups. Reduced-motion preferences disable animations. Closed accordions are inert and hidden from assistive technology.

The Resources callout uses an orange background with a small bordered pointer aimed at Resources and a dark-text Got it! button for clear contrast.

For testing, the small Reset button in the lower-right corner clears only this activity’s local-storage key and returns to the introduction. It immediately clears the assigned city and all responses without a confirmation. Other local-storage data are left alone. Starting again assigns a random city; it may happen to select the same city.

Community Needs uses a 194-pixel label column to keep Population measured on one line.

## Worksheet export and layout updates

The PDF uses section bars, orange label cells, bordered response cells, and running headers/footers. Short entry tables stay together when possible; longer answers continue onto additional letter-size pages with continuation headings. Entirely blank optional indicators are omitted from the PDF. Priority Population labels are wider to keep the first question on one line. The mission page uses consistently spaced bullet prompts. The final Back button uses the same outlined secondary-button style as other slides.

## Research review accordions

Your Research uses Community Needs, Barriers to Care, and Existing Resources tabs. Each tab shows student-titled entry accordions, all closed initially, with at most one open. All fields and their responses appear together inside the expanded entry; there are no Previous/Next controls. The pop-up stays 760 × 600 pixels. Its outer area does not scroll. Unusually long answers can scroll inside the expanded entry so text is never clipped or discarded. Short answers fit without scrolling. The answer area uses available space based on the number of entries.

## Accessibility update

See ACCESSIBILITY.md for changes, completed checks, and remaining manual tests. The activity includes keyboard support for research tabs, focus management, screen-reader guidance, reduced-motion handling. Automated checks do not establish screen-reader compatibility or full WCAG conformance. The fixed-size layout remains, and the worksheet PDF is untagged.


The city-assignment slide displays the state beneath the city name, including when resuming a saved assignment.
