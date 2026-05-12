## 2026-04-18 - Contextual Action Visibility
**Learning:** Using `opacity-0 group-hover:opacity-100` for contextual actions (like copy buttons) creates a clean UI but can hide functionality from keyboard users. Adding `focus:opacity-100` is a mandatory companion to ensure the element becomes visible when tabbed into.
**Action:** Always pair `group-hover:opacity-100` with `focus:opacity-100` for interactive elements to maintain WCAG accessibility.
