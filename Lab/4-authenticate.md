[← Lab 1 Guide](labguide.md)

# Step 4 — Authenticate

## Goal

Sign in to your GitHub account so Copilot CLI can use your Copilot subscription.

## Start authentication

Inside an interactive Copilot session, run the slash command:

```
/login
```

(You should already be in a session from Step 3; if not, run `copilot` first.)

## What happens

1. The CLI shows a one-time device code and a URL (<https://github.com/login/device>).
2. Open that URL in your browser.
3. Paste the device code and confirm.
4. Authorize the GitHub Copilot CLI application.
5. Return to the terminal — it will confirm you are signed in.

## Check your login status

At any time you can confirm who you are signed in as:

```
/user
```

## Alternative (headless / CI environments)

Set a token in your environment before launching:

```powershell
$env:GH_TOKEN = "your_personal_access_token"    # PowerShell
```

## What success looks like

- The CLI reports a successful login with your GitHub username.
- `/user` shows your account and that Copilot access is active.

## Troubleshooting

- **"No Copilot access":** confirm your subscription is active at <https://github.com/settings/copilot>.
- **Wrong account:** run `/logout`, then `/login` again.

---

Previous: [Step 3 — Trust the Working Directory](3-trust-working-directory.md)
Next: [Step 5 — Create a Simple App](5-create-a-simple-app.md)
