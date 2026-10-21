---
name: end-of-day-brief
description: >-
  Use this for Mon–Thu end-of-day wrap: Tonight, Today accomplishments, this
  week’s goals with status emoji only, and a short Tomorrow preview — pair
  with the morning daily focus brief. Friday is phase 4 of Friday weekly
  wind-down.
---

# End of day brief

Produce a short weekday close-out brief: what got done today, anything urgent still worth doing tonight before logging off, and a preview of tomorrow. Use when the Mon–Thu EoD routine fires, when the user asks for an end-of-day / wrap / “what’s left tonight,” or as **phase 4** of [Friday weekly wind-down](sand-workflow:friday-weekly-wind-down).

Depends on [Set Goals](sand-workflow:set-goals) for month/quarter context and the locked **this week’s #1** from Friday weekly wind-down phase 3 (or the latest week #1 in memory). Uses [Open Items Cleanup](sand-workflow:open-items-cleanup) judgment lightly — do not invent commitments. Pair with [Daily focus brief](sand-workflow:daily-focus-brief) (morning); do not duplicate that brief’s “Today’s #1” lead. Match daily focus brevity for goals and calendar sections.

Runs Monday–Thursday around wrap time (default **5:30 PM local**). Friday EoD is **not** a cron — it runs only after Friday close phases 1–3 (product update posted, skill review settled, next-week goals signed off). Weekends stay off unless the user asks.

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
- **Required:** email + Slack since the midday check, via the Inbox reconcile in [Open Items Cleanup](sand-workflow:open-items-cleanup)
- Overdue `notes-check-*` one-shots (see [Notes-check catch-up](sand-workflow:notes-check-catch-up))

## Steps

### 0. Notes-check reliability (quick)

Sweep today's notes-checks (locked 2026-10-09): list today's ended meetings and their "Notes check: …" one-shots. Any one-shot whose fire time has passed without a run is a miss. Run [Notes-check catch-up](sand-workflow:notes-check-catch-up) for each miss before writing the brief, so Open Items and **Done today** are current, and report which one-shots to delete. Mention in **Tonight** or **Watch** only if a miss was recovered or notes are still missing.


### 0b. Inbox reconcile (required)

Run the **Inbox reconcile** in [Open Items Cleanup](sand-workflow:open-items-cleanup) for the window since the ~11 AM midday check, plus today's work finished in chat. Close what's done or answered (counts toward **Today**), and put new asks the user hasn't answered under **Tonight** or **Watch**. Never list a row as open that today's work or a teammate's reply already covered.

### 1. Load focus context

- Read month #1 and this week’s goals.
- If week #1 is missing, infer from Open Items under month #1 and say you are inferring.

### 2. What got done today

Pull a tight accomplishment list (3–7 bullets max):

- Open Items moved to Done today (or Last edited today and clearly finished)
- Linear (always): issues assigned to them (`me`) that completed or changed status today — name issue + change; don’t dump the board. Update the matching Open Item plate row so Notion stays the single plate.
- Calendar meetings that happened today (skip declined / focus / OOO); one clause each if they produced a decision or handoff
- Concrete shipped artifacts the user or CoS finished today that aren’t on Open Items yet (e.g. board pack to a stakeholder, skill locked) — only if grounded in this chat / memory / tools, never invented
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

Status judgment uses Open Items + calendar + Slack/Linear, but that evidence stays out of the goals section (put outcomes in **Today** instead).

If week #1 finished today, say so in **Today** (not as a goals essay) and name the provisional next #1 under month #1 for the rest of the week (offer to lock). On Friday, next week’s goals already signed off in wind-down phase 3 — do not re-propose them here.

### 5. Tomorrow preview (Mon–Thu only)

Keep this as short as daily focus **Meetings** — no arrow stacks, no parenthetical run-ons.

1. **Likely tomorrow’s #1** — one short outcome sentence (provisional; morning brief re-ranks). No meeting names or path mechanics in this line.
2. **Meetings** — tomorrow’s hard meetings with times only (skip declined / focus / OOO). Bare list only: nothing nested under any meeting, ever (locked 2026-10-08).
3. Optional: one **Watch** item that will bite tomorrow if ignored overnight (only if not already under Tonight).

Do **not** write a single “Stack: A → B → C (then X, Y)” line.

Bad Tomorrow:
> Stack: BD Sync 6:30 → Eng Standup 7:00 → Design-partner final check 7:30 → Partner contact 8:00 → Report 1:1 8:30 → Company/design-partner Design Partner Sync 9:00 (then dentist 11:00, User<>Stakeholder 4:00)
> Raise compliance counsel topic in the morning 1:1 (P0, before travel)
> Likely tomorrow’s #1 is run the design-partner sync well

Good Tomorrow:
> Likely tomorrow’s #1: Run the design-partner sync well.
>
> Meetings
> - 6:30 BD Sync
> - 7:00 Eng Standup
> - 7:30 Design-partner final check
> - 8:00 Partner contact
> - 8:30 Report 1:1
> - 9:00 Company/design-partner Design Partner Sync
> - 11:00 Dentist
> - 4:00 User<>Stakeholder

### 6. Message the brief

Mon–Thu:

1. **Tonight** (lead — urgent before logoff, or “clear — log off”)
2. **Today** (accomplishment bullets)
3. **This week’s goals** — full plain goal text each, status emoji only at the end of the line (no trailing status essays)
4. **Tomorrow** — likely #1 (one short line) + Meetings list (+ optional Watch)
5. **Watch** (optional; or fold under Tomorrow)

Friday (from wind-down):

1. **Today** (lead — what they achieved)
2. **This week’s goals** — full plain text + status emoji only
3. **Tonight** — clear / log off, or one real same-night gate
4. One line that Monday’s 6:00 AM brief will pick up the signed-off next-week #1

Link Open Items dashboard when useful. Do not dump the full board. Keep the whole brief scannable in under a minute.

### 7. Store

- Optionally write “EoD YYYY-MM-DD: tonight clear|one urgent; week goal emoji statuses; provisional tomorrow #1” to memory (log-tier).
- Default is always send the brief on Mon–Thu at the routine time. Friday only via wind-down phase 4.
- If the user is clearly mid-ship on a Tonight item in this chat, fold a one-line status into Tonight instead of nagging.

## Quality bar

1. Good if the user knows in under 30 seconds whether they can log off, what they finished, week status via emoji only, and tomorrow’s first move — without run-on goal essays or calendar stacks.
2. Improve when they say Tonight was noise, goals ran long, or Tomorrow was a run-on; tighten those sections to match [Daily focus brief](sand-workflow:daily-focus-brief).
3. Friction: default to “clear — log off”; ask only when two true same-night P0s conflict.

## Automation quality

1. How do we know it’s good? → User acts on Tonight only when real, or logs off without follow-up questions; goals and Tomorrow stay short.
2. Better next time? → After a few runs, note false-urgent Tonight lines and cut them; cut any status essay that creeps back onto a goal line.
3. Friction? → Tonight bar stays high; morning brief owns ranking the new day.

## Out of scope

- Replacing [Daily focus brief](sand-workflow:daily-focus-brief) or night-before 1:1 meeting prep
- Full weekly retro or Open Items cleanup pass
- Posting EoD to Slack unless the user asks
- Starting Friday close — that is [Friday weekly wind-down](sand-workflow:friday-weekly-wind-down) phases 1–3
