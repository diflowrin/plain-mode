---
name: explain-first
description: Before changing code, tell the user in three plain lines what will change, why, and what could break — then wait for approval. Use when working with a non-technical user who cannot read a diff and needs to stay in control of their own project.
---

# Explain First

A non-technical user cannot read a diff. If you change ten files and say "done", they have lost control of their own project. They will not notice for three days, and then they will not know how to get back.

## Before you touch anything

Post this, then **stop and wait**:

```
I'm about to:
- **What:** <the change, in one plain sentence>
- **Why:** <what it fixes or adds, for them>
- **Risk:** <what could break, or "nothing — this is safe to undo">

Files: <plain names, e.g. "the login page and the settings file">

OK to go ahead?
```

Three lines. Not a design document. If you cannot say what you are doing in one sentence, the change is too big — split it.

## Skip the check when

- The user already said "just do it", "go ahead", "don't ask me", or approved this exact plan a moment ago.
- It's a typo, a colour, a label, a text change — anything visible and instantly reversible.
- They asked for the change in so much detail that repeating it back is just noise.

Approval covers **that** change, not the next one. A "yes" to editing the login page is not a "yes" to also touching the database.

## Always stop and ask, even if told not to

- Deleting files, folders, or data.
- Anything that touches a real database, real users, or real money.
- Installing something big, or changing what the project is built on.
- Anything you cannot undo, or cannot undo without them losing work.

For these, say plainly what is permanent about it before asking.

## After the change

One line. Not a report:

```
Done — <what changed, in plain words>.
You'll see it here: <where to look, what should look different>
```

If you had to do something beyond what you described, say that in one extra line. Never bury an unapproved change inside a summary of an approved one.

## Undo

Any time you make a change that is not trivially reversible, make sure the user knows how to go back — in their words, not git's. If there is no way back, say so **before** doing it, not after.
