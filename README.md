# Plain Mode

**Skills for Claude Code, made for people who aren't programmers.**

Claude talks to you like you're a senior developer. You're not. You're building something.

This is a small set of skills that changes how Claude talks — as short as it can be without losing anything, and no jargon you cannot decode. Nothing about how it writes code changes. Only how it talks to you.

---

## Before and after

**Before**

> I've refactored the authentication module to use a middleware-based approach. The `verifyToken` utility now runs before the route handler resolves, which means unauthorized requests short-circuit early rather than hitting the database. This should reduce latency on rejected requests and centralizes the auth logic so we're not duplicating the check across seven route files. I also added TypeScript types for the session payload to catch mismatches at compile time rather than runtime. Let me know if you'd like me to walk through any part of this, or if you'd prefer a different approach to the session handling — there are a few tradeoffs worth discussing around token expiry.

**After**

> Login checks now happen in one place instead of seven. Faster, and easier to fix if something goes wrong later. Log out and back in to make sure it still works for you.

---

## What's inside

Five skills. Each one fixes a specific annoyance.

| Skill | What it fixes |
|---|---|
| **plain-talk** | The jargon. Words get explained, or they don't get used. |
| **short-answers** | The wall of text. As short as the answer allows — long only when it has to be. |
| **explain-first** | Surprise changes. Claude tells you what it's about to change, and waits. |
| **error-translator** | The scary red text. Paste it, get plain English plus the fix. |
| **plain-recap** | "Where am I with this?" Answered in features, not file names. |

Plus two commands you can type any time:

- `/detail` — give me the full technical version, just this once
- `/huh` — that didn't land, explain it again but simpler

---

## Install it

### Option 1 — one command (recommended)

In Claude Code, type:

```
/plugin marketplace add diflowrin/plain-mode
```

Then:

```
/plugin install plain-mode@diflowrin
```

That's it. Restart Claude Code.

### Option 2 — copy the folder

1. Download this repo (green **Code** button → **Download ZIP**) and unzip it.
2. Copy the five folders inside `skills/` into `~/.claude/skills/` on Mac/Linux, or `C:\Users\YourName\.claude\skills\` on Windows. Create the `skills` folder if it isn't there.
3. Restart Claude Code.

---

## Now do this part — it matters

The skills above switch on when they're needed. But the **tone** has to be on all the time, or Claude drifts back to talking like a manual after a few messages.

So: copy the file `templates/CLAUDE.md` into the main folder of your project, next to your code. Keep the name `CLAUDE.md`.

Claude reads that file at the start of every conversation, so the rules stay on permanently.

> **Already have a CLAUDE.md?** Don't overwrite it — paste the contents at the bottom of yours instead.

To apply it to *every* project on your computer instead of one, put it at `~/.claude/CLAUDE.md` (Mac/Linux) or `C:\Users\YourName\.claude\CLAUDE.md` (Windows).

---

## How to use it day to day

You don't call the skills. They just work. Two things worth remembering:

- Answer too short? Type **/detail**.
- Didn't understand? Type **/huh**.

That's the whole thing.

---

## Make it yours

Every skill is a plain text file. Open any `SKILL.md` and edit it — it's written in normal English, not code.

Some things people change:

- **Answers still too long, or now too clipped.** The length rule is a paragraph in `skills/short-answers/SKILL.md` — reword it tighter or looser.
- **You want Claude to stop asking permission.** Delete `skills/explain-first/`, or remove that section from your `CLAUDE.md`.
- **You know more than the README assumes.** Trim the jargon dictionary in `skills/plain-talk/SKILL.md` down to the words you actually don't know.
- **You want it in your own language.** Claude answers in whatever language you write in. The skills work the same.

---

## Does this make Claude dumber?

No. It changes what Claude says to you, not what it does. The code it writes, the problems it solves and the care it takes are unchanged — you just stop getting the essay.

If you ever need the full technical depth, `/detail` gives it back for one answer.

---

## License

MIT. Take it, change it, publish your own version.

---

*Plain Mode is an independent project. It is not affiliated with, endorsed by, or sponsored by Anthropic. Claude and Claude Code are trademarks of Anthropic PBC, used here only to describe what this project works with.*
