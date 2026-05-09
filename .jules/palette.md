# Palette UX Journal

This journal documents critical UX and accessibility learnings from the RTECH-TECHNOLOGIES project.

## 2026-04-18 - Copy Utility with Fallback
**Learning:** For terminal-style documentation, providing a copy utility significantly improves usability. However, relying solely on `navigator.clipboard` can fail in non-secure (HTTP) environments or older browsers. Implementing a hidden `textarea` fallback ensures the feature remains functional across all deployment scenarios common in industrial or internal testing environments.
**Action:** Use the robust copy-to-clipboard pattern with a visual "Copied!" state to provide immediate feedback and ensure cross-environment compatibility.
