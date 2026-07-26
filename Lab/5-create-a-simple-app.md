[← Lab 1 Guide](labguide.md)

# Lab 1 · Step 5 — Create a Simple App

## Goal

Have Copilot generate a small, runnable program for you — no manual coding required. This is your first "vibe coding" prompt.

## Type this prompt into Copilot

Copy the prompt below into your interactive Copilot session:

```text
Create a simple Node.js command-line app in this folder called
app.js. It should ask the user for their name, then print a
friendly greeting and the current date and time. Keep it to a
single file with no external dependencies. After you create it,
show me the contents of app.js.
```

## What to expect

- Copilot proposes creating `app.js` and shows you the code.
- Approve the file creation when it asks for permission.
- The file `app.js` now exists in your folder.

> **Note:** Copilot asks before touching your files. You will see a prompt like *"Do you want to edit `C:\temp\lab1\app.js`?"* — select **Yes** to authorize the action. This is the agent proposing while you stay in control: read what it wants to do, then approve.

## Try a variation (optional)

Pick a different tiny app if you prefer, for example:

```text
Create a Node.js command-line app in this folder called guess.js that
plays a number-guessing game: pick a random number between 1 and 100,
then let me keep guessing, telling me "higher" or "lower" after each
guess until I get it. Keep it to a single file with no external
dependencies.
```

## Tips for good prompts

- State the language and the file name.
- Describe the behavior in plain English.
- Add constraints ("single file", "no dependencies").
- Ask it to show the result so you can review it.

## What success looks like

- A new source file exists in your trusted folder.
- You have read the code Copilot produced.

---

Previous: [Step 4 — Authenticate](4-authenticate.md)
Next: [Step 6 — Run It](6-run-it.md)
