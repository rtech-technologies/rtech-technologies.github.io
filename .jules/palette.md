## 2025-05-15 - Navigation Layout Shift Fix
**Learning:** Adding a border on hover to navigation links (e.g., `border-bottom`) causes a vertical layout shift if the border isn't already accounted for in the element's height. This creates a jittery "jump" effect that feels unpolished.
**Action:** Initialize navigation links with a transparent border of the same width (`border-bottom: 2px solid transparent;`). On hover, only change the `border-color` (`border-bottom-color: var(--lime);`) to ensure the layout remains stable.

## 2025-05-15 - Unified Terminal Branding
**Learning:** Brand identity is reinforced by consistent interactive elements. A terminal-style blinking cursor (`_`) on the logo provides a subtle but high-impact "live" feel that aligns with the sovereign tech aesthetic.
**Action:** Use a CSS animation with `step-end` to simulate a blinking cursor (`@keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }`) and apply it to a dedicated cursor span in the logo.
