# Accessibility Guidelines

SharpSell follows WCAG 2.1 Level AA as the baseline for all admin interfaces.

---

## Color Contrast

| Element | Minimum ratio |
|---|---|
| Body text (14px regular and below) | 4.5:1 |
| Large text (18px+ or 14px bold) | 3:1 |
| UI controls and borders | 3:1 |
| Disabled elements | Exempt — but must look visually distinct |

**Rule:** Never rely on color alone to convey meaning. Pair color with text, icons, or patterns.

---

## Keyboard Navigation

- All interactive elements must be reachable via Tab
- Focus order must follow visual reading order (left-to-right, top-to-bottom)
- Focus indicators must be clearly visible — never remove the outline without replacing it
- Modal dialogs must trap focus until dismissed
- Escape must close any overlay (modal, dropdown, popover)

### Component-specific keyboard behavior

| Component | Key | Action |
|---|---|---|
| Button | Enter / Space | Activate |
| Checkbox | Space | Toggle |
| Radio | Arrow keys | Move within group |
| Switch | Space | Toggle |
| Select dropdown | Arrow keys / Enter / Escape | Navigate, select, close |
| Modal | Tab / Shift+Tab / Escape | Cycle focus / close |

---

## Labels and Descriptions

- Every form input must have a visible `<label>` — placeholder text does not count
- Icon-only buttons must have `aria-label`
- Groups of related controls (radio buttons, checkboxes) must use `role="group"` or `<fieldset>` with `<legend>`
- Error messages must be associated via `aria-describedby`
- Required fields must use `aria-required="true"`

---

## States

- **Disabled:** Use `aria-disabled="true"`. Never rely on opacity alone — also set `pointer-events: none`
- **Loading:** Use `aria-busy="true"` on the loading region
- **Error:** Use `aria-invalid="true"` and link to the error message with `aria-describedby`
- **Expanded/Collapsed:** Use `aria-expanded` on the toggle control

---

## Touch Targets

- Minimum touch target size: 40px × 40px (maps to `md` button height)
- Minimum spacing between adjacent targets: 8px

---

## Screen Reader Guidance

- Decorative images and icons must use `aria-hidden="true"`
- Status badges that convey meaning must have `aria-label` text
- Live regions (`aria-live="polite"`) should announce toast notifications
- Page navigation changes should announce the new page title

---

## Testing Checklist

Before shipping any screen, verify:

- [ ] Tab through every interactive element — nothing is skipped
- [ ] Focus is visible on every element
- [ ] All form fields have visible labels
- [ ] All icon-only buttons have aria-labels
- [ ] Error states are announced by screen readers
- [ ] Modals trap focus and close with Escape
- [ ] Color contrast meets minimums
- [ ] Touch targets meet 40px minimum
