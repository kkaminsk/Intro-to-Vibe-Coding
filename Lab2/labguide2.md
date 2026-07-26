# Lab 2 — Fix a Broken App with Copilot CLI

## Lab Guide *(Bonus, Optional)*

---

> **⭐ This is an optional bonus lab.** It's here for students who want to explore troubleshooting in a structured, guided way. It is **not** required to complete the session.
>
> **Prefer to keep vibing?** Great — that's the whole point. Instead of this lab, go back to your Lab 1 app and keep building: add a feature, redesign it, or start something entirely new and see how far you can push it with prompts. Come back to this lab any time you hit an error and want a repeatable way to work through it.

---

## Overview

In Lab 1 you built a working application from scratch using GitHub Copilot CLI. That went smoothly — but real software development rarely does. Code frequently fails the first time you run it, and the skill that separates a beginner from a confident developer is knowing what to do next.

This lab teaches that skill. You will deliberately start with a **broken** application, run it, read the error it produces, and use Copilot CLI to diagnose and fix it. Then you will run it again to **verify** the fix actually worked.

This "run → read the error → fix → re-run" cycle is the core loop of real-world programming, and doing it with an AI agent is the heart of *vibe coding*.

---

## Lab Objectives

By the end of this lab, you will be able to:

1. **Set up an isolated project** and trust the folder so Copilot CLI can work in it.
2. **Recognize that first attempts often fail** — and treat a broken app as a normal, expected starting point.
3. **Run a program and capture its error output** accurately, instead of guessing what went wrong.
4. **Turn an error message into an effective prompt**, handing the agent the exact information it needs to fix the problem.
5. **Verify a fix** by re-running the app and confirming correct behavior.
6. **Repeat the debugging loop** when new errors appear — the fundamental workflow of software development.

---

## What You'll Build

A small Node.js command-line greeting app (`app.js`) that asks for the user's name and prints a greeting with the current date. It is intentionally created with **one deliberate bug** so you can practice fixing it.

### The bug (for instructors / curious learners)

The code *calls* a function named `buildGreeting()`, but the function is actually *defined* as `makeGreeting()`. Because the names don't match, Node.js can't find `buildGreeting` and throws:

```
ReferenceError: buildGreeting is not defined
```

This is a common, realistic mistake and it produces a clear, readable error — perfect for a first debugging exercise. Learners should **not** fix it by inspection; the point is to let the error message guide the fix.

---

## Prerequisites

- Completion of **Lab 1** (Copilot CLI installed and authenticated).
- If you skipped Lab 1, install and sign in first. On Windows, `winget` is recommended (it needs no Node.js):
  ```
  winget install GitHub.Copilot     # recommended on Windows
  # — or, cross-platform (requires Node.js): —
  npm install -g @github/copilot
  ```
  Then run `copilot` and `/login` inside the session.
- Node.js 18+ (`node --version` to check) — needed to run the `app.js` you'll debug (it's a Node.js program), and for the npm install of Copilot above. The `winget` install of Copilot doesn't need it. On Windows, install Node with `winget install OpenJS.NodeJS.LTS`, or manually from <https://nodejs.org/en/download>.

---

## Lab Steps

The lab is split into five files. Work through them in order — each step depends on the one before it.

### Step 1 — Set Up and Trust a New Folder
**File:** [`1-setup-and-trust.md`](1-setup-and-trust.md)

Create a fresh, empty project folder (`C:\temp\lab2`), start Copilot inside it, and **trust** the folder when prompted. Trust is what allows Copilot to read, edit, and run your files. Starting in a clean folder keeps this exercise isolated from Lab 1's `C:\temp\lab1`.

> **Goal:** A new trusted folder with Copilot running and ready.

---

### Step 2 — Create the (Broken) App
**File:** [`2-create-broken-app.md`](2-create-broken-app.md)

Prompt Copilot to create `app.js` using the exact broken code provided — **without correcting it**. This guarantees the app fails on the first run so everyone gets the same error to practice on.

> **Key idea:** We *want* it broken. Do not ask Copilot to fix it yet, and don't over-analyze the code — let the error tell you what's wrong in the next step.

---

### Step 3 — Run It and Capture the Error
**File:** [`3-run-and-capture-error.md`](3-run-and-capture-error.md)

Run the app and watch it crash. Then **copy the full error message** — the error type (`ReferenceError`), the message (`buildGreeting is not defined`), and the file/line reference.

> **Why it matters:** Accurate fixes come from the *actual* error text, not a guess. Reading errors carefully is one of the most valuable developer skills, and it makes the agent's fix far more precise.

---

### Step 4 — Prompt the Agent to Fix It
**File:** [`4-prompt-agent-to-fix.md`](4-prompt-agent-to-fix.md)

Paste the captured error into a prompt and ask Copilot to **explain the cause** and **fix the file**. Approve the edit when Copilot proposes it, and read the explanation so you understand *why* the fix works — not just that it does.

> **Pattern to learn:** Error in → explanation + fix out. Always ask the agent to explain what it changed and why.

---

### Step 5 — Run Again and Verify the Fix
**File:** [`5-run-and-verify-fix.md`](5-run-and-verify-fix.md)

Re-run the app and confirm the error is gone and the greeting prints correctly. If a *new* error appears, repeat the loop from Step 3. Finish with an optional challenge: have Copilot introduce a fresh bug for you to debug on your own.

> **Never trust a fix you haven't re-run.** Verification is what closes the loop.

---

## The Debugging Loop (Summary)

This lab drills one repeatable cycle. Memorize it — you'll use it constantly:

```
   ┌─────────────────────────────────────────────┐
   │                                             │
   ▼                                             │
 RUN the app                                     │
   │                                             │
   ▼                                             │
 READ / COPY the error                           │
   │                                             │
   ▼                                             │
 PROMPT the agent with the error → get a fix     │
   │                                             │
   ▼                                             │
 VERIFY by re-running ──── still broken? ────────┘
   │
   ▼
 WORKING ✔
```

---

## Success Criteria

You have completed Lab 2 when:

- ✅ `app.js` failed on the first run with a `ReferenceError`.
- ✅ You captured the full error and used it to prompt Copilot.
- ✅ Copilot explained the cause and fixed the code.
- ✅ The app now runs cleanly and prints a correct greeting.
- ✅ You can describe the run → error → fix → verify loop in your own words.

---

## Key Takeaways

- **Broken first attempts are normal.** The measure of a developer isn't avoiding errors — it's how effectively they resolve them.
- **Errors are information, not failure.** The message tells you (and the agent) exactly where to look.
- **A good prompt includes the evidence.** Paste the real error; don't paraphrase.
- **Always verify.** Re-running the app is the only proof a fix worked.
- **The loop scales.** The same cycle you used on a one-line bug works on real, complex software.

---

*Next: apply this loop the next time your own code — or an AI's — doesn't work the first time.*
