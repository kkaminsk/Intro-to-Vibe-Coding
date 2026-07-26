# Intro to Vibe Coding

Materials for a one-hour introductory session on **vibe coding** — building working software by describing what you want in plain English and letting an AI coding assistant (GitHub Copilot CLI) write the code.

The session frames AI as an **assistant, not an oracle**: the human owns the specification, review, and final decisions, while the agent handles the typing.

---

## 📦 What's in This Repository

| Item | Description |
|------|-------------|
| **[Agenda.md](Agenda.md)** | The 1-hour session run-of-show — schedule, talking points, and environment checklist. |
| **[Slides/Vibe_Coding_Manual.pptx](Slides/Vibe_Coding_Manual.pptx)** | The intro slide deck: what AI is, why it can write code, its limits, and the prompt-driven workflow. |
| **[Lab/](Lab/)** | **Lab 1 — Build Your First App** with Copilot CLI. |
| **[Lab2/](Lab2/)** | **Lab 2 (Bonus, Optional) — Fix a Broken App** with Copilot CLI. |

---

## 🧪 The Labs

Both labs are hands-on and prompt-driven — you don't write application code by hand, you describe it to Copilot CLI. Each lab is a set of numbered prompt files plus a guide that explains the objectives and walks through every step.

### Lab 1 — Build Your First App
📘 **[Lab 1 Guide → Lab/labguide.md](Lab/labguide.md)**

Install and authenticate Copilot CLI, trust a folder, then generate, run, explain, improve, and document a small greeting app — entirely through prompts.

Prompt files (work through them in order):

1. [Open PowerShell and Create Your Lab Folder](Lab/1-open-powershell-and-create-folder.md)
2. [Install Copilot CLI](Lab/2-install-copilot-cli.md)
3. [Trust the Working Directory](Lab/3-trust-working-directory.md)
4. [Authenticate](Lab/4-authenticate.md)
5. [Create a Simple App](Lab/5-create-a-simple-app.md)
6. [Run It](Lab/6-run-it.md)
7. [Explain and Improve It](Lab/7-explain-and-improve.md)
8. [Add a Small Test or README](Lab/8-add-test-or-readme.md)

### Lab 2 — Fix a Broken App *(Bonus, Optional)*
📕 **[Lab 2 Guide → Lab2/labguide2.md](Lab2/labguide2.md)**

> [!NOTE]
> **This lab is an optional bonus** for students who want to explore troubleshooting in a structured way. It is not required to complete the session.
>
> **Prefer to keep building?** That's the spirit of vibe coding — instead of Lab 2, keep going with your Lab 1 app: add a new feature, redesign it, or start something completely new and see how far you can take it with prompts.

Real code often fails the first time. In this lab you deliberately start with a **broken** app, read the error, prompt the agent to fix it, and verify the fix — the core **run → read the error → fix → re-run** loop of real development.

Prompt files (work through them in order):

1. [Set Up and Trust a New Folder](Lab2/1-setup-and-trust.md)
2. [Create the (Broken) App](Lab2/2-create-broken-app.md)
3. [Run It and Capture the Error](Lab2/3-run-and-capture-error.md)
4. [Prompt the Agent to Fix It](Lab2/4-prompt-agent-to-fix.md)
5. [Run Again and Verify the Fix](Lab2/5-run-and-verify-fix.md)

---

## Prerequisites

- **Node.js 18+** and **npm** (`node --version`, `npm --version`)
- An active **GitHub Copilot** subscription (Individual, Business, or Enterprise)
- A terminal (PowerShell 7 recommended on Windows, not required) — VS Code optional

> [!IMPORTANT]
> **Why Node.js?** You need it either way: it runs the Node.js demo app you build in the labs, and it's required if you install the Copilot CLI with `npm`. The recommended `winget` method below doesn't need Node.js for the CLI install itself — but the labs still do, so install Node.js regardless.

Install Node.js on Windows:

```
winget install OpenJS.NodeJS.LTS
```

Or download and run the installer manually from **<https://nodejs.org/en/download>**, then verify with `node --version` and `npm --version`.

Install Copilot CLI and sign in. On Windows, `winget` is recommended — it adds `copilot` to your PATH automatically and the install itself doesn't require Node.js (the labs still do — see above):

```
winget install GitHub.Copilot     # recommended on Windows
# — or, cross-platform (requires Node.js): —
npm install -g @github/copilot

copilot          # then run /login inside the session
```

---

## 🧭 Suggested Flow

1. Review the **[Agenda](Agenda.md)** to see how the hour is structured.
2. Present the **[slide deck](Slides/Vibe_Coding_Manual.pptx)** (AI for code).
3. Run **[Lab 1](Lab/labguide.md)** — build a working app.
4. **Then keep vibing** — expand your app with new features, or start something new. Students who want a structured troubleshooting exercise instead can do the optional **[Lab 2 (Bonus)](Lab2/labguide2.md)**.

> [!NOTE]
> GitHub's docs indicate Copilot CLI is available with all Copilot plans, but organizations may need to enable the policy. It supports trusted directories, tool access, and file/URL permissions.
