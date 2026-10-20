---
name: daily-focus-brief
description: >-
  Use this for Mon–Fri morning focus: short Today’s #1 and optional #2, week
  goals plus named current-month goals with status emoji only, a bare list of
  today’s meetings, a terse list of Open Items to tackle today, and overnight
  news. After the brief, always ask for updates or edits.
---

Produce a short weekday morning brief that helps the user start the day fast: today’s outcome, week/month status at a glance, today’s meetings, the Open Items worth tackling today, and what changed overnight. Use when the Mon–Fri daily routine fires, or when the user asks for today’s focus / “what should I do today.”

Depends on [Set Goals](sand-workflow:set-goals) for month/quarter context and the locked **this week’s #1** from [Friday weekly wind-down](sand-workflow:friday-weekly-wind-down) phase 3 (or the latest week #1 in memory). Uses [Open Items Cleanup](sand-workflow:open-items-cleanup) judgment lightly — do not invent commitments.

Runs Monday–Friday at 6:00 AM local. Week #1 is locked when Friday close phase 3 is signed off. Monday morning uses that lock — do not invent a second weekly brief. If week #1 is missing (first week, or Friday was skipped), infer a candidate from Open Items under month #1 and say you are inferring. Weekends stay off unless the user asks.

## Brevity is the product (locked 2026-10-08)

The user has had to cut this brief back more than once. Every extra clause is a regression. Before sending, delete anything that is context, rationale, prep advice, timing, or sequencing. The user will tell you in the morning what is missing or wrong, and will add tasks through the day as meetings and other things come up. Do not try to anticipate that.

- **Meetings are ONLY a list of meetings.** Time + title, one line each. Never a sub-bullet, prep line, agenda pointer, or note under a meeting. Ever.
- **Never schedule the user’s day** unless they explicitly ask. No “before 7:00”, “8:00–9:00”, “at a named 1:1”, “afternoon”, “then”, or ordering around the calendar.
- **Open Items = a terse list** of what you think they should tackle today. Short verb title only. No times, no due-date parentheticals unless the item is due today and that is the whole reason it’s on the list (“(due today)” max), no explanations, no Waiting-on notes, no “then”.
- **Overnight** section is useful — keep it, but one short line per item.

## Do not assume memory of weekly goals

The user will **not** remember this week’s #1/#2 from Monday. Every daily brief must restate week (and month) goals in full plain sentences. Never use opaque shorthand alone (“week #1”, “Custody #2”) without naming the actual goal in the same breath.

## Inputs

- Locked **current calendar month** goals and this week’s goals from memory (see Month header rule below)
- Personal Open Items (This week / Waiting / Top of mind / recently Done)
- Calendar for **today** and **upcoming ~3–4 weeks** (user TZ) — for meeting list and meeting-owned Open Item reconcile
- Notes-check results since yesterday (Added/Updated/Closed) — required to load, not optional
- Slack since yesterday for due / Waiting / “reply to X” Open Items: counterpart **DMs** and deal threads (especially the business-development GTM Slack channel (`the business-development channel`))
- Linear (**required for the user** — always on): issues assigned to them that **completed or meaningfully changed status yesterday** (use to refresh Open Items; do **not** dump a Yesterday section in the morning brief)
- Overdue `notes-check-*` one-shots (see [Notes-check catch-up](sand-workflow:notes-check-catch-up))

## Steps

### 0. Notes-check reliability (quick)

Before drafting the brief, scan for overdue notes-check one-shots per [Notes-check catch-up](sand-workflow:notes-check-catch-up). If any are overdue from yesterday evening or earlier today, run catch-up (or kick it) so Open Items are current before you rank today’s #1.

For **Engineering Standup**: when notes exist (Gemini, Slack AI, or your peer’s recording), ingest them here like any other notes-check. If notes are still missing, do not invent standup outcomes.

### 0b. Inbox reconcile (required)

Run the **Inbox reconcile** in [Open Items Cleanup](sand-workflow:open-items-cleanup) for the overnight window (since yesterday's EoD) before ranking anything: close rows done or answered, flag new asks from email and Slack. New asks go in **Overnight**. The Slack steps below are the minimum for deal items, not the whole check.


Do **not** treat Notion status as truth for “reply to X” / MOU / partner items until Slack is checked.

For each non-Done Open Item that is due today, overdue, or Waiting on a named person — especially your counterpart / BD / MOU / named partner deals:

1. Search that person’s **DM with the user** since yesterday.
2. Search the business-development GTM Slack channel (`the business-development channel`) threads for the deal name.
3. If the user already replied and the counterpart marked it done (or equivalent), **close the Open Item** with reason + Slack link **before** writing the brief. Do not list it as still due.
4. If the user replied but a new gate appeared, update Waiting on — don’t keep the old “reply to your counterpart” title.

### 0c. Calendar reconcile for meeting-owned Open Items (required)

Scan the next ~3–4 weeks of calendar (not only today). For each non-Done Open Item whose next step is “meet / align / define / schedule with X”:

1. If a matching meeting already exists (same people + topic), **close the Open Item** with reason “calendar owns: {meeting title + date}”.
2. If the only remaining work is prep before that meeting, rewrite to a prep verb with Due = meeting day; otherwise close.
3. Never keep “attend / define in meeting” as This week when the meeting is booked.
4. Never promote “attend meeting X” into Today’s #1 or Optional #2.

### 1. Load focus context

- Read **this calendar month’s** locked goals and this week’s goals from memory.
- Month section always tracks the **current calendar month** (user TZ). Do not show next month’s goals early.
- If week #1 is missing, infer a candidate from Open Items under month #1 and say you are inferring (offer to lock).

### 2. Score week and month goals (emoji only)

For each locked week goal and each locked **current-month** goal, assign exactly one status emoji. No Open Item text, blockers, or progress essays after the goal line.

| Emoji | Meaning |
| --- | --- |
| ✅ | Done |
| 🟡 | In progress |
| ⬜ | Open (not started) |
| ❌ | At risk / blocked / likely to miss |

If week #1 is ✅ Done mid-week, propose the next #1 under month #1 for the rest of the week (ask to lock).

### 3. Today’s #1 and Optional #2

**Today’s #1**
- One short outcome sentence. Lead with the outcome, not the path.
- Default: the next concrete outcome that advances this week’s #1.
- Swap only for a hard same-day external gate. No explanation of the swap.
- **Do not** name meetings, times, or mechanics in this line.

Good: “Today’s #1: Ensure the design-partner sync is ready for Wed.”

**Optional #2**
- Equally short. Only if it advances a still-open week goal the user can actually move today.
- **Never** a meeting.
- Skip the section entirely if nothing qualifies.

### 4. Build Meetings, Open Items, Overnight

**Meetings**
- `- 7:00 Title` one line per meeting (user TZ). Skip declined / focus / OOO noise.
- Nothing nested under any meeting. No prep, no agenda pointer, no attendee notes.

**Open Items to tackle today**
- The Open Items you think the user should tackle today: what advances Today’s #1 / #2, plus hard same-day dues.
- One short verb title per line. No times, no sequencing, no rationale.
- Not a full board dump. Link the Open Items dashboard once at the end.

**Overnight**
- What changed while the user was asleep that matters today (new Slack asks, unblocks, declines, calendar changes). One short line each.
- Skip the section if empty. No Yesterday accomplishments list.

### 5. Message the brief

Strict order:

1. **Today’s #1** — one short outcome line
2. **Optional #2** — one short outcome line, or omit
3. **This week’s goals** — full plain goal text each, status emoji only
4. **{Month} goals** — header names the current calendar month; that month’s locked goals, full text + emoji
5. **Meetings** — bare list
6. **Open Items to tackle today** — terse list + dashboard link
7. **Overnight** — only if something changed

No **Yesterday**. No **Watch**. No prep lines anywhere.

### 6. Ask for updates (required)

After sending the brief, **always** ask:

> Any updates or edits?

When the user replies with corrections or progress — in the morning or as the day goes on — reconcile immediately (Open Items, light memory). Treat their additions as today’s tasks; don’t re-plan their day around them.

### 7. Store

- Optionally write today’s #1 to memory for the day (log-tier).

## Quality bar

1. Good if the user can read the whole brief in under 20 seconds.
2. Improve when they correct a still-open item that Slack already showed done; patch the Slack-reconcile step.
3. Friction (locked 2026-09-29): Today’s #1 naming meetings/times/paths, status essays after goals, or Yesterday/Watch sections — wrong.
4. Friction (locked 2026-09-29): month header must say the current month name.
5. Friction (locked 2026-10-08): ANY line under a meeting, ANY time or ordering in Open Items, or ANY explanation/context clause on an Open Item — wrong. Cut back to the bare structure above.
