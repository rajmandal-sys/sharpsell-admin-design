# SharpSell Design System

> The single source of truth for SharpSell's visual language — tokens, components, layouts, and guidelines — structured for both human readers and AI agents.

---

## What's in here

| Folder | What it contains |
|---|---|
| `/tokens` | Design tokens — colors, spacing, typography, borders, elevation |
| `/components` | Component specs — props, variants, states, usage rules |
| `/layouts` | Page and screen layout patterns |
| `/guidelines` | Brand voice, accessibility, do's & don'ts |
| `/agent` | Agent-ready manifest files (start here for AI integration) |

---

## For Product People

Browse any folder above. Each file is plain JSON or Markdown — readable in GitHub directly.

**Start with:**
- [`/tokens/colors.json`](./tokens/colors.json) — all color values
- [`/components/index.md`](./components/index.md) — list of all components
- [`/guidelines/overview.md`](./guidelines/overview.md) — brand rules

---

## For AI Agents

Point your agent to the manifest file — it lists every resource with its raw URL:

```
https://raw.githubusercontent.com/YOUR_ORG/sharpsell-design-system/main/agent/manifest.json
```

**Recommended system prompt snippet:**
```
Before generating any screen or component, fetch the SharpSell Design System manifest at:
https://raw.githubusercontent.com/YOUR_ORG/sharpsell-design-system/main/agent/manifest.json

Load the relevant tokens and component specs. Follow all constraints exactly.
Always use token values — never hardcode colors, spacing, or font sizes.
```

---

## How to update

1. Edit the relevant JSON or Markdown file
2. Commit and push to `main`
3. Changes are live instantly — no build step needed

---

## Maintainers

| Role | Person |
|---|---|
| Design System Lead | Raj |
| Design | Akash |
| Product | Navin Prajapati |

---

*Hosted on GitHub Pages. Raw file URLs are stable and safe to use in agent prompts.*
