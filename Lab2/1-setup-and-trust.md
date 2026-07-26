[← Lab 2 Guide](labguide2.md) · **Step 1 of 5**

# Lab 2 · Step 1 — Set Up and Trust a New Folder

## 📖 About this lab

In Lab 1 you built a working app. Real development is rarely that clean — code often fails the first time. In this lab you will deliberately start with a **broken** app, read the error, and use Copilot CLI to diagnose and fix it. Then you will run it and verify the fix.

## Prerequisites

- You completed Lab 1 (Copilot CLI installed and authenticated).
- Node.js 18+ (`node --version` to check) — this lab's `app.js` is a Node.js program, so you need Node.js no matter how you installed the Copilot CLI. On Windows: `winget install OpenJS.NodeJS.LTS`, or manually from <https://nodejs.org/en/download>.
- If you haven't installed the Copilot CLI, install and sign in first. On Windows, `winget` is recommended (the CLI install itself needs no Node.js — see [Lab 1, Step 2](../Lab/2-install-copilot-cli.md)):

  ```powershell
  winget install GitHub.Copilot        # recommended on Windows
  ```

  ```powershell
  npm install -g @github/copilot       # or, cross-platform (requires Node.js)
  ```

  Then start it with `copilot` and run `/login` inside the session.

  **If `copilot` is "not recognized" after the npm install,** its folder (`%AppData%\npm`) isn't on your PATH — the `winget` install avoids this. To fix npm's PATH, run this and open a new terminal (full details in [Lab 1, Step 2](../Lab/2-install-copilot-cli.md#troubleshooting)):

  ```powershell
  [Environment]::SetEnvironmentVariable("Path", [Environment]::GetEnvironmentVariable("Path","User") + ";$env:APPDATA\npm", "User")
  ```

## Create and enter a new project folder

In your PowerShell terminal, create a fresh folder for this lab and move into it — kept separate from Lab 1's `C:\temp\lab1`:

```powershell
mkdir C:\temp\lab2
```

```powershell
cd C:\temp\lab2
```

(`mkdir` creates `C:\temp` if it doesn't already exist.)

## Start Copilot in that folder

```powershell
copilot
```

## Trust the folder

When Copilot asks whether you trust the files in this folder, choose to **TRUST** it. Copilot needs this to read, edit, and run your code.

## ✅ What success looks like

- You are in a new, empty folder called `C:\temp\lab2`.
- Copilot is running and the folder is trusted.

---

| ↑ Guide | Next → |
|:--|--:|
| [Lab 2 Guide](labguide2.md) | [Step 2 — Create the (Broken) App](2-create-broken-app.md) |
