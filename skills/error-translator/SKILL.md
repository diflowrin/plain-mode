---
name: error-translator
description: Turn an error message, red text, stack trace, failed build or crash into a plain-language explanation plus exact steps to fix it. Use whenever the user pastes an error, says something is broken, red, not working, or shows a screenshot of a failure.
---

# Error Translator

The user has pasted something red and frightening. They do not need to understand it. They need it gone.

## Always answer in this shape

```
**What happened:** <one sentence, plain, no jargon>

**Why:** <one sentence — the actual cause, in their terms>

**Fix:**
1. <exact step>
2. <exact step>

**You'll know it worked when:** <what they will see>
```

Nothing else. No stack trace quoted back. No "this is a common issue". No lecture on how the framework works.

## Rules

- **Never paste the error back at them.** They already have it. It scared them once.
- **One cause.** If there are three possible causes, pick the most likely, fix that, and say "if that wasn't it, tell me and we'll try the next thing." Do not hand them a decision tree.
- **Exact commands.** Copy-pasteable, with nothing left to fill in unless you name it explicitly.
- **Say whether it's their fault.** Usually it isn't, and saying so out loud lowers the panic: "This one's normal — it happens to everybody the first time."
- **Say if it's harmless.** Warnings, deprecation notices and yellow text usually change nothing. Say "you can ignore this" and move on.

## Common translations

| The scary text | What it actually means |
|---|---|
| `ENOENT: no such file or directory` | The app looked for a file that isn't there — wrong name, wrong folder, or it was never created. |
| `EADDRINUSE` / `port 3000 already in use` | The app is already running in another window. Close it, or use a different port. |
| `Cannot find module 'x'` | A piece the project needs wasn't downloaded. Usually fixed by `npm install`. |
| `401 Unauthorized` | The server doesn't know who you are. Your key or login is missing or wrong. |
| `403 Forbidden` | The server knows who you are and is saying no. Wrong account or missing permission. |
| `404 Not Found` | That address doesn't exist. Usually a typo in a link or route. |
| `500 Internal Server Error` | Your server crashed. The real cause is in the server's own log, not here. |
| `CORS error` | The browser blocked your app from talking to another site for safety. It's a settings fix on the server side. |
| `undefined is not a function` / `cannot read property of undefined` | The code expected something to be there and it was empty. Almost always data that hadn't loaded yet. |
| `SyntaxError: unexpected token` | A typo in the code — a missing bracket, comma or quote. |
| `permission denied` | Your computer is refusing. Usually a locked file or a folder you don't own. |
| `merge conflict` | Two versions of the same file disagree. Somebody has to pick which one wins. |

## Screenshots

If they send a picture of an error, read it and answer in exactly the same shape. Never ask them to retype it. If part is cut off and you need it, ask for that one specific part.

## When you genuinely don't know

Say so in one line, then give the single best diagnostic step:

> "I can't tell from this alone. Run `<command>` and paste everything it prints — that will show me the real cause."

Never guess at a fix and present it as certain. A beginner cannot tell the difference and will lose an hour.
