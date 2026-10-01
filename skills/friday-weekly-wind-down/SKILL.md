---
name: friday-weekly-wind-down
description: >-
  Use this for the Friday 1pm close: Open Items stale/duplicate cleanup first, then weekly product update, skill review, lock next week’s goals, then Friday EoD.
---

# Friday weekly wind-down

Friday close for the user. The **1:00 PM local time Friday** routine starts this skill at phase 0. Later phases wait on the user’s gates. Do not run phases out of order. Do not also fire the old Friday 10:00 AM product-update cron or the Sunday skill-review cron — those routines are deleted.

Use when the Friday 1pm routine fires, when the user asks to start Friday close / wind down, or when a later message continues a Friday already in progress.

## Sequence (hard)

| Phase | What | Gate before next |
| --- | --- | --- |
| 0 | [Open Items Cleanup](sand-workflow:open-items-cleanup) — stale / duplicate / obsolete pass | Board hygiene done; report keep vs closed (and any ask-first cuts settled). Then start the product update. |
| 1 | [Weekly product update](sand-workflow:weekly-product-update) (Product) or the user’s weekly {role} update | Draft done **and** posted to Slack (explicit post go; CoS never posts without it) |
| 2 | [Weekly skill review](sand-workflow:weekly-skill-review) | Flags shown; get input where a change needs a decision. Do not auto-edit skills. |
| 3 | Next week’s goals (this skill, below) | User **signs off** on #1 / #2 / #3. Propose first; do not lock on silence. |
| 4 | [End of day brief](sand-workflow:end-of-day-brief) — Friday weekend close | Delivered. User logs off. |

Write phase to memory each advance: `Friday close YYYY-MM-DD phase: open-items | product-update | waiting-slack | skill-review | week-goals | eod | done`.

If this Friday already finished (`done`), stay quiet on a duplicate 1pm fire. If a later chat message continues an in-progress Friday, resume at the stored phase — do not restart phase 0.

## Phase 0 — Open Items cleanup (before product update)

Run [Open Items Cleanup](sand-workflow:open-items-cleanup) on the personal Open Items board **before** drafting the weekly product update. Same evaluation as a standing stale/duplicate pass (lesson 2026-09-29 Tue afternoon cleanup):

1. Load all non-Done Open Items (This week / Waiting / Inbox / Top of mind).
2. Close or merge **stale, duplicate, and obsolete** rows (calendar already owns attendance; superseded work; duplicate titles; Waiting gates that already cleared in Slack). Put the reason in Notes.
3. Rewrite vague rows to verb + next step when they stay. Ask first on ambiguous cuts.
4. Message a short keep-vs-closed summary (counts + notable closes). Link the Open Items dashboard.
5. Only after that summary is sent (and any ask-first decisions settled), advance to phase 1 and draft the product update.

Do not invent commitments. Do not skip this phase to “save time” for the update — a clean board is the input spine for Glance/day-close later in phase 1.

## Phase 1 — Weekly product update

Run [Weekly product update](sand-workflow:weekly-product-update) for the week just ending. Iterate in markdown. Ask before posting. After the user says the draft is ready **and** to post, post to the locked channel (Product: the product team Slack channel (`the product channel`)), then advance to phase 2.

If they are mid-edit, stay in phase 1. Do not start skill review until Slack is actually posted.

## Phase 2 — Weekly skill review

Run [Weekly skill review](sand-workflow:weekly-skill-review). Flag only. Get input where a flag needs a yes/no or a cut-vs-keep. Apply only what they approve. When the review is settled (including “nothing material”), advance to phase 3.

## Phase 3 — Next week’s goals

Depends on [Set Goals](sand-workflow:set-goals) and [Open Items Cleanup](sand-workflow:open-items-cleanup). Do not invent commitments. Prefer the board state left by phase 0; do a light refresh only if something moved mid-afternoon.

### Goals vs tasks (hard)

**#1 / #2 / #3 are chunks of work** — prepare, write, ship, decide, spec, demo. Each needs strategic thinking and a done-state.

**A scheduling chore is a task, not a goal.** Never lock “schedule a meeting / book a call / get X on the calendar” — **including when the user names it as one.** Push back:

> That’s a task, not a goal. Goals need some strategic thinking and work. What is the work behind the call?

File the booking as a Notion P0 (or P1) if critical. The work behind the call is the week goal.

Lesson 2026-09-11: “schedule the partner kickoff” is a board P0; week #1 was prepare the internal demo for the week.

### Inputs

(Template excerpt: remaining steps follow the same conventions—generalize channel/repo names from memory; never invent commitments; ask before external posts.)

