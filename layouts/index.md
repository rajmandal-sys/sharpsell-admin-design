# Layouts

Screen-level layout patterns used across SharpSell.

## Index

| Layout | File | Description |
|---|---|---|
| Base Layout | [`base-layout.json`](./base-layout.json) | Application chrome shell — header, sidebar, and empty content slot. Every screen sits inside this. |
| Detail View | [`detail-view.json`](./detail-view.json) | Two-column detail page — collapsable form sections on the left, summary panel on the right. |

## Layout File Structure

```json
{
  "name": "LayoutName",
  "figma": { "fileKey": "...", "nodeId": "..." },
  "description": "When to use this layout",
  "viewport": { "min": "1366px", "reference": "1366px" },
  "regions": {
    "region-name": {
      "figmaNodeId": "...",
      "description": "...",
      "position": "top | left | right-of-sidebar",
      "width": "...",
      "height": "fill",
      "sticky": true,
      "surface": "token/path",
      "padding": "app-spacing/s16",
      "children": {}
    }
  },
  "tokens": {},
  "spacing": {},
  "effects": {},
  "tokenSources": {
    "colors": "../tokens/colors.json",
    "spacing": "../tokens/spacing.json",
    "typography": "../tokens/typography.json",
    "borders": "../tokens/borders.json"
  },
  "behavior": {},
  "constraints": [],
  "usage": { "do": [], "dont": [] },
  "examples": []
}
```

## Adding a New Layout

1. Create a new `.json` file following the structure above
2. Add a row to the index table above
3. Add its URL to `/agent/manifest.json` under `layouts`
