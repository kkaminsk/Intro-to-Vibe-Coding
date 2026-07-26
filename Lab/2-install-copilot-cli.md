[← Lab 1 Guide](labguide.md) · **Step 2 of 8**

# Lab 1 · Step 2 — Install Copilot CLI

## 🎯 Goal

Get the GitHub Copilot CLI installed on your machine so you can chat with Copilot directly from a terminal.

## Prerequisites

- Node.js 18 or newer (check with `node --version`)
- npm (check with `npm --version`)
- An active GitHub Copilot subscription (Individual, Business, or Enterprise)

> [!IMPORTANT]
> **You need Node.js for this lab no matter how you install the Copilot CLI** — it runs the Node.js app you build later in this lab (Steps 5–6). Node.js is *also* required to install the CLI with npm (Option B below). The winget install (Option A) is the only piece that doesn't need it, because it bundles everything the CLI itself needs — but don't skip installing Node.js: the rest of the lab still depends on it.

### Install Node.js (Windows)

If `node --version` fails, install Node.js first. Using winget:

```powershell
winget install OpenJS.NodeJS.LTS
```

Or download and run the installer manually from <https://nodejs.org/en/download>.

Then confirm it is on your PATH:

```powershell
node --version
```

Or

```powershell
npm --version
```

## Install command

Pick **one** of the two methods below.

### Option A — winget (recommended on Windows)

Installs the official GitHub Copilot CLI and adds it to your PATH automatically, so you avoid the npm PATH issue in [Troubleshooting](#troubleshooting). The install itself does not require Node.js (you still need Node.js for the rest of this lab — see [Prerequisites](#prerequisites)), and it installs PowerShell 7 if you don't have it:

```powershell
winget install GitHub.Copilot
```

### Option B — npm (cross-platform)

Requires Node.js (see above). Installs the CLI as a global npm package. On some setups the command is not on your PATH afterward — see [Troubleshooting](#troubleshooting) if `copilot` is "not recognized":

```powershell
npm install -g @github/copilot
```

## Verify the install

Confirm the CLI is on your PATH and check the version:

```powershell
copilot --version
```

## Launch it

Start an interactive Copilot session:

```powershell
copilot
```

## ✅ What success looks like

- `copilot --version` prints a version number with no error.
- Running `copilot` opens the interactive prompt where you can type.

## Troubleshooting

**`copilot: not recognized` after the npm install (Option B) succeeded.** npm installed the command, but its folder is not on your PATH. (The winget install in Option A avoids this entirely — switching to it is the easiest fix.) The Copilot command lives in npm's global folder:

```
C:\Users\<you>\AppData\Roaming\npm      (i.e.  %AppData%\npm)
```

First just close and reopen your terminal — that fixes it if the folder is already on PATH. If a **fresh** terminal still fails, the folder is not on PATH at all. Add it permanently (PowerShell), then open a new terminal:

```powershell
[Environment]::SetEnvironmentVariable(
  "Path",
  [Environment]::GetEnvironmentVariable("Path","User") + ";$env:APPDATA\npm",
  "User")
```

To test immediately in the **current** terminal without reopening:

```powershell
$env:Path += ";$env:APPDATA\npm"
copilot --version
```

(Confirm where npm installs global commands with `npm config get prefix`.)

**Permission errors on install.** On Windows, run the terminal as Administrator, or fix your npm global prefix.

**Old Node version.** Upgrade to Node 18+ and reinstall.

---

| ← Previous | ↑ Guide | Next → |
|:--|:--:|--:|
| [Step 1 — Open PowerShell](1-open-powershell-and-create-folder.md) | [Lab 1 Guide](labguide.md) | [Step 3 — Trust the Working Directory](3-trust-working-directory.md) |
