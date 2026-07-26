[← Lab 2 Guide](labguide2.md) · **Step 4 of 5**

# Lab 2 · Step 4 — Prompt the Agent to Fix It

## 🎯 Goal

Hand the error to Copilot and ask it to diagnose and fix the app. Let the error do the talking.

## 💬 Type this prompt into Copilot

Paste the prompt below into Copilot, using the actual error you copied in Step 3. It should look like this:

```text
Running app.js failed with this error:

ReferenceError: buildGreeting is not defined

Explain in plain English what caused this error, then fix app.js so it
runs correctly. Show me exactly what you changed and why.
```

## 👀 What to expect

- Copilot explains the cause: the code calls `buildGreeting()` but the function is named `makeGreeting()`, so the name does not match.
- Copilot edits `app.js` to fix it (for example, renaming the call to `makeGreeting`, or renaming the function to `buildGreeting`).
- Approve the edit when it asks for permission.

## Learn from the fix

Before moving on, make sure you understand the fix. If anything is unclear, ask a follow-up such as:

```text
Why did the names have to match exactly? What is the difference
between defining a function and calling it?
```

> [!TIP]
> Fix one error at a time. If a new error appears after this fix, repeat the same loop: run it, copy the new error, paste it back to Copilot.

## ✅ What success looks like

- You understand what caused the error.
- Copilot has updated `app.js` with the fix.

---

| ← Previous | ↑ Guide | Next → |
|:--|:--:|--:|
| [Step 3 — Run It and Capture the Error](3-run-and-capture-error.md) | [Lab 2 Guide](labguide2.md) | [Step 5 — Run Again and Verify the Fix](5-run-and-verify-fix.md) |
