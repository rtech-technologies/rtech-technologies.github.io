## 2026-04-17 - Resource Hints and Variable Fonts
**Learning:** For static sites using third-party CDNs (Google Fonts, Tailwind), `preconnect` hints can shave off significant connection setup time (~20-50ms depending on network). Additionally, using variable font ranges (e.g., `300..900`) instead of discrete weights ensures all used weights are covered (fixing missing `font-black` 900 weight) and allows the browser to optimize font fetching more effectively.
**Action:** Always check for used font weights that might be missing from the CSS request and add `preconnect` for all critical external assets.

## 2026-04-25 - Script Execution vs window.onload
**Learning:** On pages with heavy third-party assets (like fonts or CDN scripts), using `window.onload` to trigger UI updates can cause a significant bottleneck in Time-to-Interactivity (TTI). Executing non-dependent logic immediately at the end of the `<body>` can improve interactivity metrics by >50% as it doesn't wait for the entire asset waterfall to complete.
**Action:** Move non-critical script execution from `window.onload` to immediate calls at the bottom of the body.
