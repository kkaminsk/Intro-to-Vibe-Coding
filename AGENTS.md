# AGENTS.md

This file provides guidance to AI coding agents (GitHub Copilot CLI, Cursor, and other agents that read `AGENTS.md`) when working in this repository.

> **Keep in sync with [`CLAUDE.md`](CLAUDE.md).** This repo maintains two guidance files with identical content — `AGENTS.md` for general AI agents and `CLAUDE.md` for Claude Code. When you change one, apply the same change to the other so they never drift.

## What This Repository Is

This is a **curriculum / workshop-materials repository**, not a software project. It holds the teaching content for a one-hour introductory session on "vibe coding" — building software by describing intent to an AI coding assistant (GitHub Copilot CLI). There is **no application source to build, and no test suite or lint config**; the only executable artifacts are tiny `app.js` demos that *workshop participants generate themselves* inside throwaway folders (`C:\temp\lab1`, `C:\temp\lab2`) that are never committed here.

Consequently, requests are almost always about **authoring, editing, or reorganizing instructional content** — prose, prompt files, agendas — not about writing or running code. There is no `npm build`/`test`/`lint` to run in this repo.

## Structure and How the Pieces Relate

Three parallel layers describe the same session at different granularities — keep them consistent when editing:

- **`README.md`** — the top-level index and entry point. Links to every other artifact and states prerequisites (Node 18+, npm, a Copilot subscription).
- **`Agenda.md`** — the minute-by-minute run-of-show for the instructor (0–60 min blocks).
- **`Lab/`** and **`Lab2/`** — the two hands-on labs. Each folder is a self-contained lab consisting of:
  - `labguide.md` / `labguide2.md` — the narrative guide (objectives, steps, success criteria, key takeaways).
  - Numbered Markdown (`.md`) prompt files (`1-…`, `2-…`, …) — the **step-by-step scripts a student works through in order**. Each follows a fixed template: a `# Step N — Title` heading, `## Goal`, the exact prompt to paste into Copilot (in a fenced code block), what to expect, a *What success looks like* section, and back/next links to the adjacent steps.
- **`Slides/Vibe_Coding_Manual.pptx`** — the intro deck (binary; edit externally).

The two labs teach complementary loops:
- **Lab 1** (required): the build loop — *describe → generate → review → run → refine*.
- **Lab 2** (explicitly an **optional bonus**): the debug loop — *run → read the error → fix → re-run*. Its app carries **one deliberate bug** (calls `buildGreeting()` but the function is defined as `makeGreeting()`, yielding `ReferenceError: buildGreeting is not defined`). This bug is intentional pedagogy — **do not "fix" it** when editing Lab 2 content; the whole exercise depends on it failing on first run.

## Editing Conventions

- **A change is rarely local to one file.** Renaming or reordering a lab step means updating the numbered `.md` step filenames, the matching `labguide*.md`, the `README.md` links, the back/next links inside the step files, and possibly `Agenda.md`. Cross-references are maintained by hand — grep for the old name.
- **Match the house voice.** Content consistently frames "AI as an *assistant, not an oracle*," and repeats the workflow motifs (the DESCRIBE→REVIEW→RUN→REFINE loop, "the specification is the source of truth"). Mirror this tone and vocabulary in new material.
- **Preserve the step template** (heading / goal / paste-in prompt block / success criteria / back-next links) when adding a step, so all prompt files stay uniform.
- **Install instructions carry cross-file invariants.** The CLI install is documented in `README.md`, `Lab/2-install-copilot-cli.md`, and `Lab2/1-setup-and-trust.md` — keep them consistent. `winget install GitHub.Copilot` is the **recommended** Windows method (adds `copilot` to PATH, needs no Node.js for the install itself); `npm install -g @github/copilot` is the cross-platform alternative and **requires Node.js**; **Node.js 18+ is required for the labs regardless of install method** (the demo `app.js` runs on Node), so don't "simplify" that note away; and the npm PATH-fix note (`%AppData%\npm` not on PATH) must stay wherever the npm method appears.
- **Lab 2 must stay optional.** The README, guide, and commit history deliberately mark it as a bonus and steer students toward "keep vibing" (extending their Lab 1 app) as the default alternative — don't reframe it as required.
