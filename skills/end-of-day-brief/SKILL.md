---
name: end-of-day-brief
description: >-
  Use this for Mon–Thu end-of-day wrap: Tonight, Today accomplishments, this week’s goals with status emoji only, and a short Tomorrow preview — pair with the morning daily focus brief. Friday is phase 4 of Friday weekly wind-down.
---

# End of day brief

Produce a short weekday close-out brief: what got done today, anything urgent still worth doing tonight before logging off, and a preview of tomorrow. Use when the Mon–Thu EoD routine fires, when the user asks for an end-of-day / wrap / “what’s left tonight,” or as **phase 4** of [Friday weekly wind-down](sand-workflow:friday-weekly-wind-down).

Depends on [Set Goals](sand-workflow:set-goals) for month/quarter context and the locked **this week’s #1** from Friday weekly wind-down phase 3 (or the latest week #1 in memory). Uses [Open Items Cleanup](sand-workflow:open-items-cleanup) judgment lightly — do not invent commitments. Pair with [Daily focus brief](sand-workflow:daily-focus-brief) (morning); do not duplicate that brief’s “Today’s #1” lead. Match daily focus brevity for goals and calendar sections.

Runs Monday–Thursday around wrap time (default **5:30 PM PT**). Friday EoD is **not** a cron — it runs only after Friday close phases 1–3 (product update posted, skill review settled, next-week goals signed off). Weekends stay off unless the user asks.

## Friday weekend close

When called from Friday wind-down phase 4:

- Lead with **Today** (what they achieved) so they can log off.
- Restate this week’s goals (full plain text + status emoji only) for the week just ending.
- **Tonight:** only a true same-night gate; default “clear — log off.”
- Skip weekday **Tomorrow** / “likely tomorrow’s #1.” Monday’s daily brief owns that.
- Do not retell the product update or skill-review flags.
- **Last message (hard):** After the brief, send a separate second chat line that is exactly: `Good work this week. Have a great weekend!`

## Do not assume memory of weekly goals

The user will **not** remember this week’s #1/#2 from Friday. Restate them in full plain sentences. Never use opaque shorthand alone (“week #1”, “Custody #2”) without naming the actual goal in the same breath. Status is emoji only — no run-on progress essays after the goal line.

## Inputs

- Locked month #1 and this week’s goals from memory
- Personal Open Items (This week / Waiting / recently Done / due today or overdue)
- Linear (**required for the user** — always on): issues assigned to them that **completed or meaningfully changed status today**
- Calendar for **today** (what happened) and **tomorrow** (user TZ) — skip tomorrow on Friday
- Optional: notes-check results from today (Added/Updated/Closed)
- Optional: light Slack / email only when something is clearly awaiting a same-night reply (do not dig for busywork)
- Overdue `notes-check-*` one-shots (see [Notes-check catch-up](sand-workflow:notes-check-catch-up))

## Steps

### 0. Notes-check reliability (quick)

Scan for overdue notes-check one-shots from earlier today. If any are overdue, run catch-up (or kick it) so Open Items and **Done today** are current. Mention in **Tonight** or **Watch** only if a miss was recovered or notes are still missing.

### 1. Load focus context

- Read month #1 and this week’s goals.
- If week #1 is missing, infer from Open Items under month #1 and say you are inferring.

### 2. What got done today

Pull a tight accomplishment list (3–7 bullets max):

- Open Items moved to Done today (or Last edited today and clearly finished)
- Linear (always): issues assigned to them (`me`) that completed or changed status today — name issue + change; don’t dump the board. Update the matching Open Item plate row so Notion stays the single plate.
- Calendar meetings that happened today (skip declined / focus / OOO); one clause each if they produced a decision or handoff
- Concrete shipped artifacts the user or CoS finished today that aren’t on Open Items yet (e.g. board pack to Graeme, skill locked) — only if grounded in this chat / memory / tools, never invented
- Prefer outcomes over activity (“sent a partner must-haves split” not “worked on a design-partner review”). Don’t dual-count the same work in Notion and Linear.

### 3. Tonight — urgent before logoff

Only items that are **truly worth interrupting wrap**. Default is empty or one line.

Include when:

- External reply owed same day (partner / customer / manager hard ask)
- Due today Open Item still open with a real consequence if it slips overnight
- Tomorrow morning meeting that needs a draft/agenda **tonight** (e.g. night-before 1:1 not yet posted) — skip this on Friday
- Waiting gate that blocks tomorrow’s first meeting unless nudged tonight

Exclude: nice-to-have cleanup, CoS publish polish, anything that can wait for tomorrow’s [Daily focus brief](sand-workflow:daily-focus-brief).

If nothing qualifies: **Tonight: clear — log off.**

### 4. Score this week’s goals (emoji only)

For each locked week goal, assign exactly one status emoji at the end of the line. No Open Item text, blockers, prep explainers, or progress essays after the goal.

| Emoji | Meaning |
| --- | --- |
| ✅ | Done |
| 🟡 | In progress |
| ⬜ | Open (not started) |
| ❌ | At risk / blocked / likely to miss |

(Template excerpt: remaining steps follow the same conventions—generalize channel/repo names from memory; never invent commitments; ask before external posts.)

