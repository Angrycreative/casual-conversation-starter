# Catch-up Topics

A tiny single-page topic spinner for our 30-minute remote catch-ups. Hit **Spin a topic** for a random conversation prompt, or pick one from the list. Everything is work-adjacent — never about the actual work.

Tap a topic to grey it out once it's been covered, so the same one doesn't come up twice in a session. Refreshing the page starts fresh.

**Live page:** https://<your-username>.github.io/<repo-name>/

## Editing the topics

All the prompts live in **`topics.js`** — that's the only file you need to touch to add, remove, or reword a topic. You don't have to understand how the page works, and you can do it without leaving GitHub.

1. Open `topics.js`, then click the pencil ✏️ (Edit) icon.
2. Each topic is one line, wrapped in `"quotes"`, ending with a comma.
3. Add a line to add a topic; delete a line to remove one.
4. Scroll down, commit the change, and the live page updates on the next refresh.

Example:

```js
window.TOPICS = [
  "First computer or console you ever had.",
  "A hobby you're secretly quite good at.",
];
```

The only rules: keep each topic inside `"double quotes"` and end the line with a comma. If a topic itself contains a `"`, put a backslash in front of it (`\"`). A leftover comma on the last line is fine.

## Files

- **`index.html`** — the app: layout, styling, and spinner logic. Rarely needs touching.
- **`topics.js`** — the list of prompts. This is the one you edit.

## Hosting

Served via GitHub Pages from the `main` branch (root). Every push to `main` redeploys automatically — there's no build step.

Setup on a fresh repo: **Settings → Pages → Source: Deploy from a branch → `main` / `(root)`**.

## Running it locally

Open `index.html` in a browser — double-clicking the file works, no server required.
