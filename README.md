# VayuCare — GenAI Family & Community Smog Assistant

Personalised smog-safety plans (Gemini), an exposure/emission simulator and a neighbourhood hub.

## Run
Open `index.html` in a browser (no build step). Tests: `npm test` (Node 18+, zero dependencies).

## Structure
- `index.html` — UI (Tailwind CDN, vanilla JS)
- `js/logic.js` — pure logic (AQI maths, impact model, input sanitising, URL and LLM-output validation)
- `tests/logic.test.js` — unit tests, run in CI via `.github/workflows/test.yml`

## Security notes
No API key is committed. Outside Canvas, route Gemini calls through a small backend proxy. User text is sanitised before reaching the prompt, LLM output is schema-validated before rendering, and a CSP limits network access to the Gemini endpoint.

## Accessibility
Skip link, ARIA tabs with arrow-key support, labelled controls, live regions, focus-trapped dialog, AA colour contrast, reduced-motion support.
