## 2026-05-13 - Contrast Standards for Pending States
**Learning:** Text elements in "pending" or "disabled" states often fall below WCAG AA contrast standards (4.5:1) when using default slate/zinc shades on dark backgrounds. In this project, the `#475569` color on `#020617` had a contrast of ~2.8:1, which is inaccessible.
**Action:** Always verify contrast ratios for non-interactive or pending states. Use `#a1a1aa` (Zinc-400) or lighter for text on near-black backgrounds to ensure accessibility.

## 2026-05-13 - Clipboard Verification in Playwright
**Learning:** Testing clipboard operations in Playwright (Python sync_api) requires explicitly granting `clipboard-read` and `clipboard-write` permissions to the browser context. Without these, `navigator.clipboard` calls may fail or hang in the test environment.
**Action:** Use `context.grant_permissions(['clipboard-read', 'clipboard-write'])` when testing copy-to-clipboard features.
