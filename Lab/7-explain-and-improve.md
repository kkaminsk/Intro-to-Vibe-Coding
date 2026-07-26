[← Lab 1 Guide](labguide.md)

# Step 7 — Ask Copilot to Explain and Improve It

## Goal

Use Copilot to understand the code it wrote and then make it better. This is where you learn from the AI instead of just running it.

## Part A — Explain it

Type this prompt into Copilot:

```text
Explain app.js to me line by line, as if I am new to programming.
What does each part do, and are there any weaknesses or edge cases
it does not handle?
```

Read the explanation. Ask follow-up questions about anything unclear, for example: "What is a function?" or "What happens if I enter a blank name?"

## Part B — Improve it

Now ask Copilot to make a concrete improvement:

```text
Improve app.js: handle the case where the user enters an empty name,
add a friendly comment above each section, and make the greeting
change based on the time of day (morning/afternoon/evening).
Show me the updated file, then explain what you changed.
```

## What to expect

- Copilot edits `app.js` and summarizes its changes.
- Approve the edits, then re-run the app (see [Step 6](6-run-it.md)) to confirm it still works and the improvements are visible.

## Tips

- Ask for **one** improvement at a time so you can follow the changes.
- Always re-run after a change to make sure nothing broke.

## What success looks like

- You understand what the code does.
- The app has been meaningfully improved and still runs.

---

Previous: [Step 6 — Run It](6-run-it.md)
Next: [Step 8 — Add a Small Test or README](8-add-test-or-readme.md)
