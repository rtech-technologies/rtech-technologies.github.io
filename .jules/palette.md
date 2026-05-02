## 2026-05-02 - Layout Stability on Hover
**Learning:** Using `border-bottom: 2px solid transparent` on navigation links as a baseline prevents layout shifts when applying a colored border on hover, maintaining visual stability.
**Action:** Always initialize interactive elements that gain borders on state changes with a transparent border of the same width.

## 2026-05-02 - Robust Clipboard Utility
**Learning:** For a technical audience, a "Copy to Clipboard" utility in terminal-style code windows significantly improves utility. Providing immediate visual feedback ("Copied!") and a fallback for non-secure/legacy environments (using a hidden textarea) ensures a reliable experience across all browsers.
**Action:** Implement clipboard utilities with both `navigator.clipboard` and an `execCommand('copy')` fallback, accompanied by clear state-change feedback on the trigger element.
