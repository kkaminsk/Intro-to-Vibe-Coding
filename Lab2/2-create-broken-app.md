[← Lab 2 Guide](labguide2.md) · **Step 2 of 5**

# Lab 2 · Step 2 — Create the (Broken) App

## 🎯 Goal

Create a small app that **looks** right but contains a deliberate bug, so you can practice the fix-it workflow. Do **not** fix it yet — we want it to fail first.

## 💬 Type this prompt into Copilot

Paste the prompt below exactly. It asks Copilot to create the app from broken code on purpose.

````text
Create a file called app.js in this folder with EXACTLY the code
below, without correcting anything. I am using this for a debugging
exercise:

// Simple greeting app
const readline = require('readline');

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

rl.question('What is your name? ', function (name) {
  const message = buildGreeting(name);
  console.log(message);
  rl.close();
});

function makeGreeting(name) {
  return 'Hello, ' + name + '! Today is ' + new Date().toDateString();
}
````

## The hidden bug

The code calls `buildGreeting()`, but the function is actually named `makeGreeting()`. When you run it, Node will not be able to find `buildGreeting` and will throw an error. That is intentional.

> [!WARNING]
> - Approve the file creation when Copilot asks.
> - Do **not** ask Copilot to fix it yet.
> - Do **not** read too closely — the goal is to let the **error** tell you what is wrong in the next step.

## ✅ What success looks like

- `app.js` exists in your folder and contains the broken code above.

---

| ← Previous | ↑ Guide | Next → |
|:--|:--:|--:|
| [Step 1 — Set Up and Trust a New Folder](1-setup-and-trust.md) | [Lab 2 Guide](labguide2.md) | [Step 3 — Run It and Capture the Error](3-run-and-capture-error.md) |
