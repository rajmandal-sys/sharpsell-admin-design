# SharpSell Design Guidelines

## Brand Identity

SharpSell is a B2B sales enablement platform. The visual language is:
- **Professional and focused** — product people are on the job, not browsing
- **Clear over clever** — every element should reduce cognitive load
- **Consistent across surfaces** — admin console, mobile app, and microsites share the same tokens

---

## Color Usage

| Use case | Token | Value |
|---|---|---|
| Primary action surface | `button/primary/bg` | #af1e57 |
| Primary action hover | `button/primary/bg-hover` | #831642 |
| Secondary action surface | `button/secondary/bg` | #ffffff |
| Danger / destructive text | `button/destructive/fg` | #b42318 |
| Page background | `card/bg` | #ffffff |
| Body text | Primitive `gray/900` | #101828 |
| Secondary text | Primitive `gray/600` | #475467 |
| Label text | Primitive `gray/700` | #344054 |
| Default border | Primitive `gray/300` | #d0d5dd |
| Focus border | `input/border-focus` | #dd3b7c |
| Error border | `input/border-error` | #f97066 |
| Mandatory indicator | `input/mandatory` | #af1e57 |

**Rule:** Never hardcode a hex value in a component. Always use a token name from `/tokens/colors.json`.

---

## Typography

- Base font: **Inter**
- Two font sizes in the compact admin system: **12px** (xs) and **14px** (sm)
- Three weights: **regular (400)**, **medium (500)**, **semibold (600)**
- Use semantic roles — `label` for field labels (12px/600), `body` for content (12px/400), `heading` for titles (14px/600)

---

## Spacing

- All spacing must come from the spacing scale (s0 through s32)
- Minimum touch target: 28px (compact button height)
- Standard input width: 320px
- Component gap: s4 (4px) for tight, s8 (8px) for standard, s16 (16px) for sections

---

## Component Rules

- Every screen has **one and only one** primary button
- Error states must use `border-error` token + error message text
- Disabled states must never use opacity alone — also set pointer-events: none
- Loading states replace label with a spinner — never add a spinner beside the label
- Destructive variant is only on Secondary hierarchy buttons — never on Primary

---

## Accessibility Baseline

- All interactive elements must be reachable via keyboard
- Color contrast: minimum 4.5:1 for body text, 3:1 for large text
- Every icon-only button needs an `aria-label`
- Form inputs must have visible labels — placeholder text does not count

---

## Do's and Don'ts

| Do | Don't |
|---|---|
| Use semantic tokens from colors.json | Hardcode colors or sizes |
| Follow component states (enabled, hover, focused, disabled) | Skip disabled/loading states |
| Use Inter font family | Introduce new font families |
| Keep text hierarchy simple (2–3 roles per screen) | Stack 4+ heading levels |
| Design at 320px input width for compact admin | Assume full-width layouts |
