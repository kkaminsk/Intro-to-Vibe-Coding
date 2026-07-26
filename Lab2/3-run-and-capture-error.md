[← Lab 2 Guide](labguide2.md)

# Lab 2 · Step 3 — Run It and Capture the Error

## Goal

Run the broken app, watch it fail, and capture the exact error message. That error is the clue you will hand to Copilot.

## Type this prompt into Copilot

```text
Run app.js and show me the full output, including any error message.
Do not change the code — I just want to see what happens.
```

Approve the command when Copilot asks (it will run `node app.js`).

## Run it yourself (alternative)

```powershell
node app.js
```

Type any name when prompted, then press Enter.

## What you should see

The program crashes with an error similar to:

```
ReferenceError: buildGreeting is not defined
    at ReadStream.<anonymous> (app.js:...)
```

## Copy the error

Select and copy the **full** error text — you will paste it into the next step. Capture:

- The error type (e.g. `ReferenceError`)
- The message (`buildGreeting is not defined`)
- The file and line reference

## Why this matters

Good bug reports come from the actual error text, not a guess. Reading errors is one of the most important developer skills — and it makes the AI's fix far more accurate.

## What success looks like

- You ran the app and saw it fail.
- You have the full error message copied and ready.

---

Previous: [Step 2 — Create the (Broken) App](2-create-broken-app.md)
Next: [Step 4 — Prompt the Agent to Fix It](4-prompt-agent-to-fix.md)
