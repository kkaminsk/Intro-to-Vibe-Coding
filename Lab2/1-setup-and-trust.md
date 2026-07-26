[← Lab 2 Guide](labguide2.md)

# Lab 2 · Step 1 — Set Up and Trust a New Folder

## About this lab

In Lab 1 you built a working app. Real development is rarely that clean — code often fails the first time. In this lab you will deliberately start with a **broken** app, read the error, and use Copilot CLI to diagnose and fix it. Then you will run it and verify the fix.

## Prerequisites

- You completed Lab 1 (Copilot CLI installed and authenticated).
- If not, install and log in first (needs Node.js — see [Lab 1, Step 1](../Lab/1-open-powershell-and-create-folder.md)):

  ```powershell
  npm install -g @github/copilot
  copilot        # then run  /login  inside the session
  ```

## Create and enter a new project folder

```powershell
mkdir fix-the-app
cd fix-the-app
```

## Start Copilot in that folder

```powershell
copilot
```

## Trust the folder

When Copilot asks whether you trust the files in this folder, choose to **TRUST** it. Copilot needs this to read, edit, and run your code.

## What success looks like

- You are in a new, empty folder called `fix-the-app`.
- Copilot is running and the folder is trusted.

---

Next: [Step 2 — Create the (Broken) App](2-create-broken-app.md)
