## 2026-05-01 - Preventing Navigation Layout Shifts
**Learning:** Adding a border only on hover causes a layout shift (jump) as the element size changes.
**Action:** Initialize `.nav-link` with `border-bottom: 2px solid transparent;` and transition only the `border-color` on hover.

## 2026-05-01 - Global Event Object in HTML Attributes
**Learning:** Relying on the global `event` object in `onclick` attributes is unreliable and can lead to errors in some environments or strict modes.
**Action:** Always pass `this` (or explicitly pass the event) to the handler function, e.g., `onclick="copyCode(this)"`.
