# Setup Guide — Publish to GitHub Pages

Follow these steps once to get the design system live. Takes ~20 minutes.

---

## Step 1 — Create a GitHub account

Go to https://github.com and sign up (free).

---

## Step 2 — Create the repository

1. Click the **+** icon → **New repository**
2. Name it: `sharpsell-admin-design`
3. Set visibility to **Public** *(required for free GitHub Pages)*
4. Click **Create repository**

---

## Step 3 — Upload the files

1. In the new repo, click **Add file → Upload files**
2. Drag and drop the entire folder structure from this ZIP
3. Write a commit message: `Initial design system setup`
4. Click **Commit changes**

---

## Step 4 — Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages** (left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Choose branch: `main`, folder: `/ (root)`
4. Click **Save**

Your site will be live at:
```
https://rajmandal-sys.github.io/sharpsell-admin-design/
```

---

## Step 5 — Update the manifest

1. Open `/agent/manifest.json`
2. Confirm the `base_url` field points to this repository:
   ```
   "base_url": "https://raw.githubusercontent.com/rajmandal-sys/sharpsell-admin-design/main"
   ```
3. Commit the change

---

## Step 6 — Test raw file access

Open this URL in your browser:
```
https://raw.githubusercontent.com/rajmandal-sys/sharpsell-admin-design/main/agent/manifest.json
```

You should see the manifest JSON. This URL is what you give to the AI agent.

---

## Step 7 — Give the agent its system prompt

Use this in your agent's system prompt:

```
Before generating any screen or component, fetch the SharpSell Design System manifest:
https://raw.githubusercontent.com/rajmandal-sys/sharpsell-admin-design/main/agent/manifest.json

Read the priority_load files first (colors, spacing, typography, guidelines).
Then load the component specs for any component you will use.
Follow all token values and rules exactly. Never hardcode values.
```

---

## Updating the design system

Any time you need to update a token or component spec:
1. Edit the file on GitHub (click the pencil icon on any file)
2. Commit the change
3. The new values are live within seconds — no rebuild needed

---

## Sharing with the team

Share this URL with product people to browse the system:
```
https://github.com/rajmandal-sys/sharpsell-admin-design
```

GitHub renders Markdown files beautifully — the README, component index, and guidelines are all readable without any extra setup.
