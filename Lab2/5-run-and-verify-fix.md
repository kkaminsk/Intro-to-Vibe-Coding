[← Lab 2 Guide](labguide2.md)

# Lab 2 · Step 5 — Run Again and Verify the Fix

## Goal

Prove the fix actually worked by running the app again and confirming it behaves correctly. Never trust a fix you have not re-run.

## Type this prompt into Copilot

```text
Run app.js again and show me the output. Confirm the error is gone and
the greeting prints correctly.
```

Approve the command, and type a name when prompted.

## Run it yourself (alternative)

```powershell
node app.js
```

## What you should see

No error this time — a working greeting, for example:

```
What is your name? Sam
Hello, Sam! Today is Tue Jul 07 2026
```

## If it still fails

Repeat the debugging loop from Lab 2:

1. Copy the new error message.
2. Paste it back to Copilot (see [Step 4](4-prompt-agent-to-fix.md)).
3. Approve the fix.
4. Run and verify again.

This **run → read error → fix → re-run** cycle is the core loop of real software development.

## Optional challenge

Ask Copilot to break it a different way, then fix it yourself using the same loop:

```text
Introduce one small, realistic bug into app.js and tell me what error
to expect. Do not tell me the fix — I want to practice debugging it.
```

## What success looks like

- The app runs with no errors and prints a correct greeting.
- You have completed a full debug cycle: broken → error → fix → verified working.

## Congratulations — Lab 2 complete!

You learned the most valuable skill in vibe coding: turning an error message into a working fix by prompting the agent, then verifying it.

---

Previous: [Step 4 — Prompt the Agent to Fix It](4-prompt-agent-to-fix.md)
Back to the [Lab 2 Guide](labguide2.md).
