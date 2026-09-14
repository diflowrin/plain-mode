---
name: plain-recap
description: Give a plain-language status of the project — what works, what is half-finished, what is next — without file trees, git jargon or technical detail. Use when the user asks where they are, what has been done, what is left, or returns to a project after a break.
---

# Plain Recap

When a non-technical user asks "where are we?", they are not asking for a changelog. They are asking: *is my thing working, what's missing, and what do I do now?*

## The shape

```
**Working now:** <what they can actually see or use today>

**Half-done:** <what's started but not usable yet, and what's missing>

**Not started:** <the things still on the list>

**Worth knowing:** <one thing that could bite them — only if there is one>
```

Keep it tight. If a section is empty, delete it rather than writing "nothing here".

## Rules

- **Describe features, not files.** "Users can sign up and log in" — not "auth module complete".
- **Describe them as the user experiences them.** If they can't click it, it's not working yet, no matter how much code exists.
- **Half-done means half-done.** Never round up to "done". If the button exists but doesn't save anything, that's half-done — say what's missing in the same line.
- **No git.** No commits, branches, merges, or "the working tree is clean".
- **No file paths.** Say "the sign-up page", not `src/app/(auth)/signup/page.tsx`.
- **No percentages.** "60% complete" is invented. Count real features instead.

## "Worth knowing"

Use this only for something with a real consequence for them. Say it plainly, with the consequence first:

> "Right now anyone can see everyone else's notes — the privacy part isn't built yet. Fine while it's just you testing, has to be fixed before anyone else uses it."

Not: "Authorization is currently unimplemented."

If there is nothing like that, leave the section out. Do not manufacture worry.

## After a break

If the user is coming back after some time, add one line at the top reminding them what the project is and what the last thing they were doing was. They have been living their life, not thinking about this.
