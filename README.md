# ResearchOps Lab

Plan usability tasks, compare prototype versions and turn anonymous observations into an evidence trail.

An AI-assisted portfolio prototype for Interaction Design & User Experience and Mobile & Web Applications learning. Created 3 October 2026 (Europe/London). Not submitted coursework and not evidence of completed user research.

## Features
- Task planning and consent checkpoint before attempt capture
- Anonymous session observations with version A/B attribution
- Task-filtered independent completion and median-time comparisons
- Local evidence board, deletion and portable study export

## Run
Open `index.html` in Chrome. No dependencies, installation or build step. For consistent browser storage behavior, optionally serve this folder with a static server you already have installed. All project code is HTML, CSS and JavaScript.

## Architecture
`index.html` supplies labeled semantic controls; `style.css` contains responsive styles; `app.js` handles DOM events, validation, derived summaries and localStorage. User text is inserted with `textContent`. Exports download JSON locally. No accounts, API calls, telemetry or backend.

## UX evidence
See `UX-CASE-STUDY.md` for assumptions, design rationale and a proposed evaluation. All initial data is fictional. Actual participant studies and visual/device testing are still pending.

## Limitations
Single-user local prototype. Browser storage is unencrypted and may be cleared; do not enter sensitive data. No cloud sync, automated backup or production authentication. Browser storage failure keeps the current in-memory session usable. JSON export has no matching import flow. Do not claim production deployment or tested accessibility conformance.

## Manual verification
- Operate all controls by keyboard and check visible focus.
- Test empty, invalid and valid form entries.
- Confirm create/delete and any edit/filter interactions.
- Reload and check saved records; verify exports contain the expected data.
- Test narrow (375px) and desktop widths, 200% zoom and a screen reader.

## License
MIT — see LICENSE.

## Offline behavior
The service worker caches the application shell after a successful first load on HTTPS or localhost. Opening the HTML directly works for the main interface but does not enable service workers. Offline availability is not guaranteed until installation finishes. There is no server sync or background submission queue. Uncached external resources are not fetched by the app. The manifest has no app icons, so install promotion varies by browser. Cache versioning must be updated when shipping changed app files.

## Next engineering milestones
Add browser integration tests, safe backup restoration where missing, migration/version compatibility tests and real-device evaluations. Conduct the proposed usability study and publish anonymised findings only with appropriate consent. Treat local persistence and offline caching as prototype implementation, not production reliability evidence.

## Visual identity
Indigo research workspace, humanist type, mint and lavender highlights, a signal illustration and distinct evidence cards.

Hover, focus, button press, entrance and decorative floating motion use CSS. Reduced-motion preferences disable animation and transitions. Typography uses local font stacks; no external font downloads. Exact type appearance depends on fonts installed on the device. Illustrations are inline SVG authored for this project.
