[← Lab 1 Guide](labguide.md) · **Step 1 of 8**

# Lab 1 · Step 1 — Open PowerShell and Create Your Lab Folder

## 🎯 Goal

Open a terminal and set up a clean, empty working folder for this lab. Everything you build in Lab 1 will live in this one folder.

## Open PowerShell

PowerShell 7 (the `pwsh` command) is recommended, but not required — Windows PowerShell works fine too.

- **PowerShell 7:** press Start, type "PowerShell 7", and open it — or run `pwsh` from any terminal (or a Windows Terminal "PowerShell" tab).
- **No PowerShell 7?** The built-in "Windows PowerShell" is a fine fallback.

### Install PowerShell 7 (optional, Windows)

Any terminal works, but PowerShell 7 is a smoother experience. Using winget:

```powershell
winget install Microsoft.PowerShell
```

Or install manually with the MSI installer from [Microsoft's docs](https://learn.microsoft.com/en-us/powershell/scripting/install/install-powershell-on-windows?view=powershell-7.6#msi).

## Create and enter the lab folder

In your PowerShell terminal, create the folder and move into it:

```powershell
mkdir C:\temp\lab1
```

```powershell
cd C:\temp\lab1
```

Notes:

- `mkdir` creates `C:\temp` automatically if it does not already exist.
- If `C:\temp\lab1` already exists, just run `cd C:\temp\lab1` to enter it.

## Confirm where you are

Check your current folder:

```powershell
pwd
```

## ✅ What success looks like

- Your prompt shows you are in `C:\temp\lab1`.
- The folder is empty and ready for Copilot to work in.

---

| ↑ Guide | Next → |
|:--|--:|
| [Lab 1 Guide](labguide.md) | [Step 2 — Install Copilot CLI](2-install-copilot-cli.md) |
