# Accessibility review

## Result and scope

The activity received code fixes and automated DOM checks. This is not a conformance certification or a completed assistive-technology test. The local preview browser could not launch, and the separate browser could not reach the local preview. Real keyboard traversal, visual zoom testing, and spoken screen-reader output therefore remain unverified.

## Changes made

- Added heading semantics for the current slide and accordion controls, with named regions and correct expanded/collapsed states.
- Focus now moves to the slide heading on navigation, so users can read the instructions before entering responses.
- Added persistent, screen-reader-readable field guidance instead of relying only on placeholders. Repeated field names include the entry number.
- Community Needs explains its group requirement to assistive technology: any three complete indicators. Additional indicators are not falsely marked required.
- Unavailable Next buttons remain discoverable by keyboard with aria-disabled and an associated explanation. They cannot advance until completion requirements are met. Completion availability changes are announced without adding visible helper text.
- Research tabs use roving tabindex and Left/Right/Home/End keys. Tab then leaves the tab list for the selected panel.
- Both sets of accordion headers support native button activation; Up/Down/Home/End move between headers. Closed content is inert and aria-hidden.
- Research accordions open/close with the same subtle animation as the main activity. All start closed; the pop-up size remains fixed. Reduced-motion preferences disable animation.
- Research answer areas are named keyboard focus stops, allowing long content to be scrolled with standard browser keyboard controls.
- Dialogs have accessible titles and modal semantics, focus their heading on open, and restore focus to their opener on close. Native HTML dialog behavior provides Escape dismissal and focus containment in supporting browsers.
- Resources and Example content regions are keyboard focusable for scrolling; external links announce that they open a new tab.
- Form outlines, placeholder contrast, and visible keyboard focus styles were strengthened.
- Reset has an explicit accessible name and announces when saved work has been cleared.

## Checks completed

- axe-core 4.14.1 in jsdom: 20 slide/dialog states, including all eight slides, Resources, Examples, and expanded research. Zero reported violations in the rules run, using WCAG 2 A/AA, WCAG 2.1 A/AA, WCAG 2.2 AA and best-practice rule tags.
- Color-contrast checks were excluded from axe because jsdom does not provide real rendering. Contrast ratios were calculated independently for key solid-color combinations: placeholder #626262 on #eaeaea = 5.07:1; input border #718184 against #eaeaea = 3.37:1; button text #101010 on #d3dfe1 = 13.96:1; callout text #49372d on #f6d0b1 = 7.80:1; focus outline #205c65 on white = 7.55:1. These are targeted checks, not a complete rendered contrast audit.
- DOM assertions covered labels, unique IDs, ARIA reference targets, roving tab focus, arrow-key handlers, one-open-accordion behavior, closed/inert states, dialog focus initialization/restoration, unavailable Next behavior, completion announcements, and optional indicators.
- Full eight-slide flow, saved work, city assignment persistence, and normal/long PDF generation passed regression checks.
- Automated tests cannot establish screen-reader compatibility. Native Tab/Shift+Tab traversal, Enter/Space activation, native dialog trapping/Escape, and actual keyboard scrolling require a browser check.

## Remaining limitations

1. The activity retains the requested fixed 1000 × 750 layout. It does not reflow to a narrow viewport, so WCAG reflow conformance cannot be claimed. High zoom, large text, and small screens require manual review.
2. The visual worksheet PDF remains untagged; do not treat it as an accessible PDF or claim PDF/UA conformance. The HTML alternative was removed at the user’s request; PDF is the only download format.
3. No live NVDA, JAWS, or VoiceOver test has been performed. Browser and screen-reader combinations can differ.
4. The Reset control is still present for the user's requested testing workflow. It immediately clears this activity's saved data.

## Manual release check

1. Use Tab and Shift+Tab through all eight slides without a mouse. Confirm visible focus, reading order, required-field behavior, adding indicators, and return navigation.
2. Open and close each accordion with Enter and Space. Confirm closed fields are skipped and Up/Down/Home/End move only between the expected headers.
3. Open every dialog. Confirm its title is announced, Tab/Shift+Tab stay inside, Escape closes it, and focus returns to the opener.
4. In Your Research, use Left/Right/Home/End across tabs, Tab to accordion headings, and Tab into long answer regions. Use arrow keys/Page Down to read the complete answer.
5. Test with NVDA plus Firefox or Chrome, and VoiceOver plus Safari. Confirm field names, persistent help, optional indicators, completion announcements, and expanded/collapsed states make sense when spoken.
6. Check browser zoom and increased text/spacing settings. Review focus visibility and clipping, particularly at 200%/400% zoom.
7. Check the worksheet PDF separately if accessible PDF submission is required.

## Pattern references

- W3C APG tabs: https://www.w3.org/WAI/ARIA/apg/patterns/tabs/
- W3C APG modal dialogs: https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/
- W3C APG accordions: https://www.w3.org/WAI/ARIA/apg/patterns/accordion/

