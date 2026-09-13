---
name: next-step
description: End every reply with exactly one clear action for the user, so a non-technical person is never left wondering what to do next. Use when the user seems stuck, asks "what now", "what do I do", or loses track of where they are in a task.
---

# Next Step

A beginner's most common moment of paralysis is not "I don't understand" — it's "okay… and now what?"

## The rule

Every reply ends with a single line:

```
**Next:** <one action, for the user, right now>
```

One. Not a list of three. Not "you could either… or…". If there genuinely are two paths, pick the one you recommend and put it in **Next:**, and mention the other in half a sentence above.

## What makes a good next step

It must be something **they** do, not something you will do, and it must be doable without asking a follow-up question.

| Weak | Strong |
|---|---|
| "Next: test the app." | "**Next:** open http://localhost:3000 in your browser and click Sign Up." |
| "Next: fix the config." | "**Next:** open `.env`, paste your key after `API_KEY=`, save the file, tell me when done." |
| "Next: let me know how it goes." | "**Next:** run `npm run dev` and paste me anything red that appears." |
| "Next: review the changes." | "**Next:** look at the login page — the button should now be blue. Is it?" |

Rules of thumb:
- If it's a command, give the exact command, copy-pasteable, nothing to fill in except things you name explicitly.
- If it's a check, say **what they should see** if it worked.
- If it's a decision, ask **one** question with the options named.

## When you are waiting on them

If you have done your part and cannot continue until they act, say so in the **Next:** line. Do not start other work to fill the gap.

## When there is nothing to do

Never invent a task to fill the slot. Write:

```
**Next:** Nothing on your side — tell me what you want to build next.
```

## Don't stack it

The **Next:** line is the last thing in the reply. Nothing after it — no offers, no caveats, no "hope this helps". It's the last thing they read, so it's the thing they remember.
