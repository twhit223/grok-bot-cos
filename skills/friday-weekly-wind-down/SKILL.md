---
name: friday-weekly-wind-down
description: >-
  Use this for the Friday 1pm close: Open Items stale/duplicate cleanup first,
  then Linear update, lock next week’s goals, weekly product update, skill
  review, then Friday EoD.
---

# Friday weekly wind-down

Friday close for the user. The **1:00 PM local time Friday** routine starts this skill at phase 0. Later phases wait on the user’s gates. Do not run phases out of order. Do not also fire the old Friday 10:00 AM product-update cron or the Sunday skill-review cron — those routines are deleted.

Use when the Friday 1pm routine fires, when the user asks to start Friday close / wind down, or when a later message continues a Friday already in progress.

## Sequence (hard)

| Phase | What | Gate before next |
| --- | --- | --- |
| 0 | [Open Items Cleanup](sand-workflow:open-items-cleanup) — stale / duplicate / obsolete pass | Board hygiene done; report keep vs closed (and any ask-first cuts settled). Then run the Linear update. |
| 0.5 | Run [Linear update](sand-workflow:linear-update) | Every draft shown; approved items posted; skipped ones settled. Then set next week’s goals. |
| 1 | Next week’s goals (this skill, below) | User **signs off** on #1 / #2 / #3. Propose first; do not lock on silence. Then start the product update. |
| 2 | [Weekly product update](sand-workflow:weekly-product-update) (Product) or the user’s weekly {role} update — locked goals go into Next Week Focus | Draft done **and** posted to Slack (explicit post go; CoS never posts without it) |
| 2.5 | Exec product update (the exec channel) | Very brief draft shown in full and posted only after explicit go |
| 3 | [Weekly skill review](sand-workflow:weekly-skill-review) | Flags shown; get input where a change needs a decision. Do not auto-edit skills. |
| 4 | [End of day brief](sand-workflow:end-of-day-brief) — Friday weekend close | Delivered. User logs off. |

Write phase to memory each advance: `Friday close YYYY-MM-DD phase: open-items | linear-update | week-goals | product-update | exec-update | waiting-slack | skill-review | eod | done`.

If this Friday already finished (`done`), stay quiet on a duplicate 1pm fire. If a later chat message continues an in-progress Friday, resume at the stored phase — do not restart phase 0.

## Phase 0 — Open Items cleanup (before product update)

Run [Open Items Cleanup](sand-workflow:open-items-cleanup) on the personal Open Items board **before** drafting the weekly product update. Same evaluation as a standing stale/duplicate pass (lesson 2026-09-29 Tue afternoon cleanup):

1. Load all non-Done Open Items (This week / Waiting / Inbox / Top of mind).
2. Close or merge **stale, duplicate, and obsolete** rows (calendar already owns attendance; superseded work; duplicate titles; Waiting gates that already cleared in Slack). Put the reason in Notes.
3. Rewrite vague rows to verb + next step when they stay. Ask first on ambiguous cuts.
4. Message a short keep-vs-closed summary (counts + notable closes). Link the Open Items dashboard.
5. Only after that summary is sent (and any ask-first decisions settled), advance to phase 0.5.

Do not invent commitments. Do not skip this phase to “save time” for the update — a clean board is the input spine for goals and Glance in phases 1–2.

## Phase 0.5 — Linear update (before product update)

Run [Linear update](sand-workflow:linear-update). Show every draft in full with health; post only items the user explicitly approves. When all are settled, advance to phase 1 and propose next week’s goals.

## Phase 1 — Next week’s goals (before product update)

Depends on [Set Goals](sand-workflow:set-goals) and [Open Items Cleanup](sand-workflow:open-items-cleanup). Do not invent commitments. Prefer the board state left by phase 0; do a light refresh only if something moved mid-afternoon.

### Goals vs tasks (hard)

**#1 / #2 / #3 are chunks of work** — prepare, write, ship, decide, spec, demo. Each needs strategic thinking and a done-state.

**A scheduling chore is a task, not a goal.** Never lock “schedule a meeting / book a call / get X on the calendar” — **including when the user names it as one.** Push back:

> That’s a task, not a goal. Goals need some strategic thinking and work. What is the work behind the call?

File the booking as a Notion P0 (or P1) if critical. The work behind the call is the week goal.

Lesson 2026-09-11: “schedule the ZF kickoff” is a board P0; week #1 was prepare the internal onboarding v2 demo.

### Inputs

- Locked quarter + month goals (run Set Goals if missing)
- This week’s #1 from memory
- Personal Open Items (non-Done) — post phase-0 cleanup
- Linear plate issues (Todo / In Progress / In Review; Backlog only if due within ~14 days or they named it)
- Daily-focus Slack + calendar reconcile before ranking
- Next week’s already-booked demos as **prep**, not “attend”

### Steps

1. Restate this week’s #1 in a full sentence. Short wrap: closed, moved, or leftover (2–4 lines). Do not retell the product update.
2. Map This week / Waiting / P0 + Linear plate rows to month goals.
3. Rank **work** (scheduling chores do not compete): month #1 work → other month goals → hard external work-deadline → else.
4. Propose **Next week’s #1 / #2 / #3** (one sentence each). Push back on tasks-posing-as-goals.
5. Confirm with the user. Get their input. **Wait for explicit sign-off.** Then lock to memory so Monday–Friday daily briefs can restate them, and advance to phase 2 (the locked goals go into the update's Next Week Focus).
6. Show This week / Waiting under month goals (scheduling P0s live here). Hygiene flags and one cut/park if overloaded. Link Open Items.

## Phase 2 — Weekly product update

Run [Weekly product update](sand-workflow:weekly-product-update) for the week just ending. Put the goals locked in phase 1 into its Next Week Focus section. Iterate in markdown. Before posting, show the exact final post (heading line as sent, full `.md` body, channel, attachment vs Drive link) per that skill's exact-preview gate; post only after the user replies "post" to that preview. After the user says the draft is ready **and** to post, post to the locked channel (Product: the product team Slack channel (`the product channel`)), then advance to phase 2.5.

If they are mid-edit, stay in phase 2. Do not start skill review until Slack is actually posted.

## Phase 2.5 — Exec product update

Right after phase 2, draft a very brief update for `the exec channel` (YOUR_EXEC_CHANNEL_ID) modeled on `your exec-update reference in memory`: same length (~100 words), structure, and tone; only the highest-leverage things (launch status, plan change, biggest risk, outlook, link to the longer the product channel update). Show the user the full exact draft; post only after their explicit go. Then advance to phase 3.

## Phase 3 — Weekly skill review

Run [Weekly skill review](sand-workflow:weekly-skill-review). Flag only. Get input where a flag needs a yes/no or a cut-vs-keep. Apply only what they approve. When the review is settled (including “nothing material”), advance to phase 4.

## Phase 4 — Friday EoD

Run [End of day brief](sand-workflow:end-of-day-brief) as the weekend close: what they achieved today (and this week if it helps them log off), Tonight only if a same-night gate remains, no weekday “tomorrow’s #1.” Say they can log off. Then mark Friday close `done`.

**Last message (hard):** After the Friday EoD brief, send a separate second line that is exactly: `Good work this week. Have a great weekend!`

## Quality bar

1. Good if Friday is one conversation: Open Items cleaned, Linear updates posted, next week’s work goals signed off, update posted, skills flagged, then a close they can log off from — no 10am/Sunday/5:30 double-fires.
2. Improve when they have to say “not yet” because a phase jumped the gate, or when the product update still cites stale Open Items that phase 0 should have closed.
3. Friction: Open Items cleanup, Linear update approval, Slack post, skill-edit approval, and week-goal sign-off are the gates. Do not skip them.
