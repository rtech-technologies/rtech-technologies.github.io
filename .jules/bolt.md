## 2026-04-17 - Resource Hints and Variable Fonts
**Learning:** For static sites using third-party CDNs (Google Fonts, Tailwind), `preconnect` hints can shave off significant connection setup time (~20-50ms depending on network). Additionally, using variable font ranges (e.g., `300..900`) instead of discrete weights ensures all used weights are covered (fixing missing `font-black` 900 weight) and allows the browser to optimize font fetching more effectively.
**Action:** Always check for used font weights that might be missing from the CSS request and add `preconnect` for all critical external assets.

## 2026-04-18 - Execution Timing and Asset Loading
**Learning:** For scripts at the end of the <body>, using `window.onload` introduces unnecessary delay by waiting for all external assets (like large fonts or CDNs) to finish. Direct execution or `DOMContentLoaded` is more efficient for "Time to Interactive". Additionally, while variable fonts are flexible, requesting large ranges or unused styles (italics) can increase payload size; keep font requests lean to avoid regressions.
**Action:** Always prefer immediate execution for footer scripts and audit font weight requests for unused styles.
