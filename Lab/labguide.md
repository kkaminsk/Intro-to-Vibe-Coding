# Lab 1 — Build Your First App with Copilot CLI

## Lab Guide

---

## Overview

This is your introduction to *vibe coding* — building working software by describing what you want in plain English and letting an AI agent write the code. You won't type a single line of application code yourself. Instead, you'll install **GitHub Copilot CLI**, sign in, and use prompts to create, run, understand, improve, and document a small app.

By the end you'll have a complete, working, documented project built entirely through conversation with an AI — and a feel for the basic prompt-driven workflow you'll use in every lab that follows.

---

## Lab Objectives

By the end of this lab, you will be able to:

1. **Install and launch Copilot CLI** from your terminal.
2. **Authenticate** the CLI against your GitHub Copilot subscription.
3. **Trust a working directory** so Copilot can read, edit, and run your files.
4. **Generate a working app from a prompt** — describing behavior in plain English instead of writing code.
5. **Run your app** and see it work end to end.
6. **Use the agent to explain and improve code**, learning from it rather than just running it.
7. **Document or test your project** by prompting Copilot to add a README or a small test.

---

## What You'll Build

A small Node.js command-line app (`app.js`) that asks the user for their name and prints a friendly greeting along with the current date and time. Over the course of the lab you'll improve it (time-of-day greetings, input handling) and finish it off with a README or a small automated test — all through prompts.

> The examples use **Node.js**. If you prefer Python, most steps include a variation you can substitute.

---

## Prerequisites

- **Node.js 18+** — check with `node --version`
- **npm** — check with `npm --version`
- An active **GitHub Copilot** subscription (Individual, Business, or Enterprise)

> **Need Node.js?** It's required for the Copilot CLI itself (the CLI installs via npm). On Windows: `winget install OpenJS.NodeJS.LTS`, or install manually from <https://nodejs.org/en/download>.

---

## Lab Steps

The lab is split into eight files. Work through them in order — each step builds on the same `C:\temp\lab1` project.

### Step 1 — Open PowerShell and Create Your Lab Folder
**File:** `1-open-powershell-and-create-folder.txt`

Open a PowerShell terminal (PowerShell 7 / `pwsh` recommended, but not required), then create and enter the folder for this lab: `mkdir C:\temp\lab1` and `cd C:\temp\lab1`. Everything you build lives in this one folder.

> **Goal:** A PowerShell terminal open in an empty `C:\temp\lab1` folder.

---

### Step 2 — Install Copilot CLI
**File:** `2-install-copilot-cli.txt`

Install the CLI — on Windows `winget install GitHub.Copilot` is recommended (it adds `copilot` to your PATH automatically and needs no Node.js), or use `npm install -g @github/copilot`. Verify it with `copilot --version`, and launch an interactive session with `copilot`.

> **Goal:** `copilot --version` prints a version, and running `copilot` opens the interactive prompt.

---

### Step 3 — Authenticate
**File:** `3-authenticate.txt`

Sign in with the `/login` command. Copilot shows a one-time device code and a URL; you approve the CLI in your browser, then return to the terminal. Confirm your identity with `/user`.

> **Goal:** Copilot reports a successful login tied to your GitHub account with active Copilot access.

---

### Step 4 — Trust the Working Directory
**File:** `4-trust-working-directory.txt`

Confirm you are in `C:\temp\lab1` (from Step 1), start Copilot, and **trust** the folder when prompted. Trust is what lets Copilot read your files, create and edit them, and run commands.

> **Goal:** A trusted `C:\temp\lab1` folder with Copilot ready to work in it.

---

### Step 5 — Create a Simple App
**File:** `5-create-a-simple-app.txt`

Write your first prompt: ask Copilot to create `app.js` — a single-file app that asks for a name and prints a greeting with the date/time. Approve the file creation and review the code Copilot shows you.

> **Key idea:** State the language, the file name, the behavior, and any constraints (e.g. "single file, no dependencies"), then ask it to show the result.

---

### Step 6 — Run It
**File:** `6-run-it.txt`

Ask Copilot to run the app (`node app.js`) and approve the command, or run it yourself. Provide input when prompted and watch it work. If it errors, paste the error back to Copilot to fix it.

> **Goal:** The program runs and prints its expected output — your first generated app working end to end.

---

### Step 7 — Ask Copilot to Explain and Improve It
**File:** `7-explain-and-improve.txt`

Two parts: first ask Copilot to **explain** `app.js` line by line and point out weaknesses; then ask it to **improve** it (handle empty input, add comments, make the greeting change with the time of day). Approve the edits and re-run to confirm.

> **Key idea:** Ask for *one* improvement at a time so you can follow the changes, and always re-run afterward.

---

### Step 8 — Add a Small Test or README
**File:** `8-add-test-or-readme.txt`

Finish like a real developer: prompt Copilot to add a beginner-friendly **README.md**, and/or a small **automated test** for the greeting logic. If you add a test, ask Copilot to run it and show the results.

> **Goal:** A documented and/or tested project — a small, complete app built entirely by prompting.

---

## The Prompt-Driven Workflow (Summary)

This lab establishes the basic loop of vibe coding — you'll reuse it constantly:

```
 DESCRIBE what you want (a clear prompt)
        │
        ▼
 AGENT generates or edits the code
        │
        ▼
 REVIEW and approve the change
        │
        ▼
 RUN it to see it work
        │
        ▼
 REFINE with the next prompt ──┐
        ▲                      │
        └──────────────────────┘
```

---

## Success Criteria

You have completed Lab 1 when:

- ✅ `copilot --version` works and you can launch an interactive session.
- ✅ You are signed in with active Copilot access (`/user` confirms it).
- ✅ You opened PowerShell, created `C:\temp\lab1`, and trusted the folder.
- ✅ Copilot generated `app.js` from your prompt and you reviewed it.
- ✅ The app runs and prints a correct greeting.
- ✅ You had Copilot explain the code and make a meaningful improvement.
- ✅ Your project has a README and/or a passing test.

---

## Key Takeaways

- **Describe intent, not syntax.** A good prompt says *what* you want in plain English, with the language, file name, and constraints.
- **Review before you approve.** The agent proposes; you decide. Always read what it created.
- **Run early and often.** Working software is the goal — confirm it actually runs.
- **Use the agent as a teacher.** Ask it to explain code and edge cases; you learn while you build.
- **Finish the job.** A README or a test turns a script into a real, shareable project.

---

*Next: **Lab 2 — Fix a Broken App with Copilot CLI**, where you'll learn what to do when the first attempt *doesn't* work.*
