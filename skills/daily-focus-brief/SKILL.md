---
name: daily-focus-brief
description: >-
  Use this for Mon–Fri morning focus: short Today’s #1 and optional #2, week goals plus named current-month goals with status emoji only, today’s meetings, and Open Items ordered for the day. After the brief, always ask for updates or edits.
---

Produce a short weekday morning brief that helps the user start the day fast: today’s outcome, week/month status at a glance, today’s meetings, and the Open Items to push between them. Use when the Mon–Fri daily routine fires, or when the user asks for today’s focus / “what should I do today.”

Depends on [Set Goals](sand-workflow:set-goals) for month/quarter context and the locked **this week’s #1** from [Friday weekly wind-down](sand-workflow:friday-weekly-wind-down) phase 3 (or the latest week #1 in memory). Uses [Open Items Cleanup](sand-workflow:open-items-cleanup) judgment lightly — do not invent commitments.

Runs Monday–Friday at 6:00 AM PT. Week #1 is locked when Friday close phase 3 is signed off. Monday morning uses that lock — do not invent a second weekly brief. If week #1 is missing (first week, or Friday was skipped), infer a candidate from Open Items under month #1 and say you are inferring. Weekends stay off unless the user asks.

## Do not assume memory of weekly goals

The user will **not** remember this week’s #1/#2 from Monday. Every daily brief must restate week (and month) goals in full plain sentences. Never use opaque shorthand alone (“week #1”, “Custody #2”) without naming the actual goal in the same breath.

## Inputs

- Locked **current calendar month** goals and this week’s goals from memory (see Month header rule below)
- Personal Open Items (This week / Waiting / Top of mind / recently Done)
- Calendar for **today** and **upcoming ~3–4 weeks** (user TZ) — for meeting list and meeting-owned Open Item reconcile
- Same-day meeting talking points the user asked to raise (memory log + due-today Open Items titled for standup / 1:1 / huddle)
- Notes-check results since yesterday (Added/Updated/Closed) — required to load, not optional
- Slack since yesterday for due / Waiting / “reply to X” Open Items: counterpart **DMs** and deal threads (especially the business-development GTM Slack channel (`the business-development channel`))
- Linear (**required for the user** — always on): issues assigned to them that **completed or meaningfully changed status yesterday** (use to refresh Open Items; do **not** dump a Yesterday section in the morning brief)
- Overdue `notes-check-*` one-shots (see [Notes-check catch-up](sand-workflow:notes-check-catch-up))

## Steps

### 0. Notes-check reliability (quick)

Before drafting the brief, scan for overdue notes-check one-shots per [Notes-check catch-up](sand-workflow:notes-check-catch-up). If any are overdue from yesterday evening or earlier today, run catch-up (or kick it) so Open Items are current before you rank today’s #1.

For **Engineering Standup**: when notes exist (Gemini, Slack AI, or your peer’s recording), ingest them here like any other notes-check. If notes are still missing, do not invent standup outcomes; say notes weren’t recorded only if that changes an Open Item you would otherwise list.

### 0b. Slack reconcile for due / Waiting items (required)

Do **not** treat Notion status as truth for “reply to X” / MOU / partner items until Slack is checked.

For each non-Done Open Item that is due today, overdue, or Waiting on a named person — especially your counterpart / BD / MOU / a named design-partner review:

1. Search that person’s **DM with the user** since yesterday.
2. Search the business-development GTM Slack channel (`the business-development channel`) threads for the deal name.
3. If the user already replied and the counterpart marked it done (or equivalent: “MOU (done)”, unblocked, moving forward), **close the Open Item** with reason + Slack link **before** writing the brief. Do not list it as still due.
4. If the user replied but a new gate appeared, update Waiting on — don’t keep the old “reply to your counterpart” title.

Lesson 2026-09-11: partner MOU replies replies were in GTM threads + your counterpart DM the day before; the brief still listed them as due because it only read Notion.

### 0c. Calendar reconcile for meeting-owned Open Items (required)

Scan the next ~3–4 weeks of calendar (not only today). For each non-Done Open Item whose next step is “meet / align / define / schedule with X”:

1. If a matching meeting already exists (same people + topic), **close the Open Item** with reason “calendar owns: {meeting title + date}” — do not leave it as This week.
2. If the only remaining work is prep before that meeting, rewrite to a prep verb with Due = meeting day; otherwise close.
3. Never keep “attend / define in meeting” as This week when the meeting is booked.
4. Never promote “attend meeting X” into Today’s #1 or Optional #2.

### 1. Load focus context

- Read **this calendar month’s** locked goals and this week’s goals from memory.
- Month section always tracks the **current calendar month** (user TZ). Do not show next month’s goals early even if already locked for Leadership or planning — those wait until that month starts (e.g. on Sep 29 show September goals, not October).
- If week #1 is missing, infer a candidate from Open Items under month #1 and say you are inferring (offer to lock).
- Scan recent memory + due-today Open Items for explicit “raise in X meeting” talking points (these go under **Meetings**, not as goals).

### 2. Score week and month goals (emoji only)

For each locked week goal and each locked **current-month** goal, assign exactly one status emoji. No Open Item text, blockers, or progress essays after the goal line.

(Template excerpt: remaining steps follow the same conventions—generalize channel/repo names from memory; never invent commitments; ask before external posts.)

