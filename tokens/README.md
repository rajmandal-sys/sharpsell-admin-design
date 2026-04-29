# Tokens

Design tokens are the atomic values of the SharpSell design language.
Every color, spacing value, font size, border radius, and shadow lives here.

## Files

| File | Description |
|---|---|
| `colors.json` | All color tokens — primitives, semantic, component-level |
| `spacing.json` | Spacing scale used for padding, margin, gap |
| `typography.json` | Font families, sizes, weights, line heights |
| `borders.json` | Border widths and radius values |
| `elevation.json` | Shadow and elevation levels |

## Token Structure

Tokens follow a 3-tier hierarchy:

```
Primitive  →  Semantic  →  Component
#DC2626    →  color/danger/default  →  surface/button/destructive/enabled
```

- **Primitive**: Raw values. Never used directly in components.
- **Semantic**: Intent-based aliases. Use these in guidelines and specs.
- **Component**: Scoped to a specific component. Use these in component JSON files.

## Usage Rule for Agents

> Always resolve to the component-level token first.
> Fall back to semantic, never to primitive.
