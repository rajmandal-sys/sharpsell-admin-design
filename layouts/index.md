# Layouts

Screen-level layout patterns used across SharpSell.

## Index

| Layout | File | Used in |
|---|---|---|
| Dashboard | `dashboard.json` | Admin Console home |
| List View | `list-view.json` | Tables, content lists |
| Detail View | `detail-view.json` | Record / profile pages, pipeline config |
| Form Page | `form-page.json` | Settings, configuration |
| Empty State | `empty-state.json` | Zero-data screens |
| Modal Flow | `modal-flow.json` | Multi-step modals |

## Layout File Structure

```json
{
  "name": "LayoutName",
  "description": "When to use this layout",
  "regions": {
    "header": { "height": "64px", "sticky": true },
    "sidebar": { "width": "240px", "collapsible": true },
    "content": { "padding": "semantic.spacing.lg" }
  },
  "breakpoints": {
    "mobile":  "< 768px",
    "tablet":  "768px – 1024px",
    "desktop": "> 1024px"
  },
  "rules": ["..."]
}
```

## Adding a New Layout

1. Copy the structure above into a new `.json` file
2. Add it to this index
3. Add its URL to `/agent/manifest.json` under `layouts`
