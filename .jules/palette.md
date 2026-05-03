## 2026-05-03 - Layout Shift Prevention in Navigation
**Learning:** When using borders as hover indicators in a terminal-style navigation, initializing the element with a transparent border of the same width (e.g., `border-bottom: 2px solid transparent;`) prevents layout shifts (jank) when the active border is applied on hover.
**Action:** Always initialize hover-bordered elements with a transparent border to ensure visual stability.

## 2026-05-03 - Contextual Utility Visibility
**Learning:** Using Tailwind's `group-hover` and `focus` utilities allows for "clean" UI that only shows utility buttons (like "Copy") when relevant. Ensuring `focus:opacity-100` is critical for keyboard accessibility so that tab-navigation reveals these hidden actions.
**Action:** Use `group` on containers and `group-hover:opacity-100 focus:opacity-100` on contextual actions to balance aesthetics and accessibility.
