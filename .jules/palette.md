## 2026-04-30 - Standardizing Navigation Aesthetic and Stability
**Learning:** In a terminal-inspired UI, navigation links benefit from a `/` prefix to reinforce the CLI aesthetic. Additionally, adding a transparent border-bottom to links in their base state prevents a 2px layout shift when the border becomes visible on hover.
**Action:** Always initialize `.nav-link` with `border-bottom: 2px solid transparent;` to ensure smooth hover transitions without vertical jumping.
