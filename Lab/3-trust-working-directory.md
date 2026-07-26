[← Lab 1 Guide](labguide.md)

# Step 3 — Trust the Working Directory

## Goal

Tell Copilot CLI it is safe to read, write, and run commands in the folder you are working in. Copilot will not act on files in an untrusted directory.

## Make sure you are in your lab folder

You created and entered `C:\temp\lab1` back in Step 1. Confirm you are still there (and `cd` back in if not):

```powershell
cd C:\temp\lab1
```

## Start Copilot in that folder

```powershell
copilot
```

## What happens

On the first launch inside a new folder, Copilot CLI asks whether you trust this directory. You will see a prompt similar to:

> Do you trust the files in this folder?

Choose to **TRUST** the current folder so Copilot can work with your files.

### Set up multi-line input

After trusting the folder, Copilot may ask:

> Set up terminal for multi-line input support?

Choose **Yes** — this lets you paste multi-line prompts (like the ones in later steps) without them being sent line by line.

## Why this matters

Trusting a directory lets Copilot:

- Read the files in the project
- Create and edit files
- Suggest and (with your approval) run terminal commands

Only trust folders whose contents you recognize.

## Manage trust later

- To review or change trusted folders, use the CLI settings / prompts the next time you enter the folder.
- If you opened the wrong folder, exit with `/exit`, `cd` to the right place, and start `copilot` again.

## What success looks like

- You confirmed trust and the interactive prompt is ready.
- Copilot can now see and modify files inside `C:\temp\lab1`.

---

Previous: [Step 2 — Install Copilot CLI](2-install-copilot-cli.md)
Next: [Step 4 — Authenticate](4-authenticate.md)
