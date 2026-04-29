# Components

All SharpSell UI components. Each has its own JSON spec file.

## Index

### Actions

| Component | File | Description |
|---|---|---|
| Button | [`button.json`](./button.json) | Primary and secondary action triggers |
| Button Link | [`button-link.json`](./button-link.json) | Low-emphasis text-style actions |
| Icon Button | [`icon-button.json`](./icon-button.json) | Compact icon-only action buttons |

### Forms — Text Input

| Component | File | Description |
|---|---|---|
| Input Field | [`input.json`](./input.json) | Single-line or multi-line text entry |
| Search | [`search.json`](./search.json) | Searchable filter input |
| Date Time Input | [`date-time-input.json`](./date-time-input.json) | Combined date and time picker |
| Date Range Input | [`date-range-input.json`](./date-range-input.json) | Start and end date-time range picker |

### Forms — Selection

| Component | File | Description |
|---|---|---|
| Dropdown Single Select | [`select.json`](./select.json) | Choose one value from a list |
| Dropdown Multi Select | [`multi-select.json`](./multi-select.json) | Choose multiple values from a list |
| Checkbox | [`checkbox.json`](./checkbox.json) | Independent on/off option |
| Radio Button | [`radio-button.json`](./radio-button.json) | Mutually exclusive option in a group |
| Switch | [`switch.json`](./switch.json) | Immediate binary toggle |

### Containers

| Component | File | Description |
|---|---|---|
| Collapsable Card | [`collapsable-card.json`](./collapsable-card.json) | Expandable/collapsible content card |
| Section Card | [`section-card.json`](./section-card.json) | Expandable page section with footer |
| Footer | [`footer.json`](./footer.json) | Action bar for modals, cards, and sections |

### Overlays

| Component | File | Description |
|---|---|---|
| Modal | [`modal.json`](./modal.json) | Dialog overlay for focused tasks |

### Display

| Component | File | Description |
|---|---|---|
| Badge | [`badge.json`](./badge.json) | Status, count, or category label |
| Featured Icon | [`featured-icon.json`](./featured-icon.json) | Decorative icon with colored background |

### Navigation

| Component | File | Description |
|---|---|---|
| Breadcrumb | [`breadcrumb.json`](./breadcrumb.json) | Hierarchical navigation trail |
| Page Header | [`page-header.json`](./page-header.json) | Top-level page title, breadcrumbs, and actions |

## Component File Structure

Every component JSON follows this shape:

```json
{
  "name": "ComponentName",
  "description": "What it does and when to use it",
  "category": "Actions | Forms | Containers | Overlays | Display | Navigation",
  "variants": {},
  "states": ["enabled", "hover", "focused", "disabled"],
  "props": { "propName": { "type": "...", "default": "...", "description": "..." } },
  "tokens": { "surface": "...", "text": "...", "border": "..." },
  "spacing": { "padding-x": "...", "height": "..." },
  "typography": { "font-family": "...", "font-size": "...", "font-weight": "..." },
  "usage": { "do": ["..."], "dont": ["..."] },
  "accessibility": { "role": "...", "aria": ["..."], "keyboard": "..." },
  "examples": [{ "label": "...", "props": {} }]
}
```

## Adding a New Component

1. Copy `_template.json` from this folder
2. Rename it to `component-name.json`
3. Fill in all fields
4. Add a row to the index table above
5. Update `/agent/manifest.json` with the new raw URL
