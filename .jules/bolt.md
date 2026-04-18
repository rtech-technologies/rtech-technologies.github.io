## 2026-04-17 - Resource Hints and Variable Fonts
**Learning:** For static sites using third-party CDNs (Google Fonts, Tailwind), `preconnect` hints can shave off significant connection setup time (~20-50ms depending on network). Additionally, using variable font ranges (e.g., `300..900`) instead of discrete weights ensures all used weights are covered (fixing missing `font-black` 900 weight) and allows the browser to optimize font fetching more effectively.
**Action:** Always check for used font weights that might be missing from the CSS request and add `preconnect` for all critical external assets.

## 2026-04-18 - Clean Builds and Resource Hints
**Learning:** External assets (Fonts, CDNs) can be a significant bottleneck on mobile or high-latency connections.  for both `fonts.googleapis.com` and `fonts.gstatic.com` (with `crossorigin`) is essential for minimizing font-load delay. Also, ensure no metadata or artifacts from development (like `server.log`) are committed, as they clutter the repo and can expose environment details.
**Action:** Include `preconnect` for all critical 3rd-party origins and use a strict `.gitignore` or manual check to exclude local logs.

## 2026-04-18 - Clean Builds and Resource Hints
**Learning:** External assets (Fonts, CDNs) can be a significant bottleneck on mobile or high-latency connections. `preconnect` for both `fonts.googleapis.com` and `fonts.gstatic.com` (with `crossorigin`) is essential for minimizing font-load delay. Also, ensure no metadata or artifacts from development (like `server.log`) are committed, as they clutter the repo and can expose environment details.
**Action:** Include `preconnect` for all critical 3rd-party origins and use a strict `.gitignore` or manual check to exclude local logs.
