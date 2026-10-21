---
name: set-goals
description: >-
  Use this when setting or refreshing quarter/month/week/day goals so task
  management has a clear #1 focus and maps Open Items and Linear work to
  outcomes.
---

# Set Goals

Establish and refresh the goal stack that drives task management. Use when the user wants to set, update, or lock quarter / month / week / day goals; when starting a new month or quarter; when priorities feel fuzzy; or when you need authoritative context before prioritizing Open Items, Linear work, or a focus brief.

**Purpose:** give the assistant durable, layered goals so every task call (what to do today, what to cut, what to escalate) maps to a named outcome — not a floating to-do list.

## Goal stack (source of truth by horizon)

| Horizon | What it is | How many | Refresh |
| --- | --- | --- | --- |
| **Quarter** | 3–5 measurable outcomes for the quarter | Stable north star | User locks; do not replace from meeting paraphrases unless they explicitly update |
| **Month** | Outcomes that move the quarter goals this calendar month | Usually 3–4; one is **month #1** | Start of month; mid-month only if reality changed |
| **Week** | Real work that matters this week under month #1 (and hard external work-deadlines) | **#1 / optional #2 / #3** — each a work chunk | Friday wind-down (or on ask) |
| **Day** | Single most important focus | **One** #1; everything else secondary | Morning or on ask |

Always know the current **#1** for the active horizon when helping manage tasks.

## Specificity bar (hard)

Goals must be **actions or full sentences with a done-state**, not noun phrases. Reject or push back on labels like “Product brand,” “Custody demos,” “AI,” “Launch.” Ask what gets finished, shipped, or true this month/quarter. Good shape: “Ship Product brand kit to marketing” / “Run custody demos with 5 users internally for feedback.”

If the user pastes vague nouns, say what’s weak, ask for one clear sentence each, *then* ask which is month #1. Do not rank or lock noun-only goals — you will not know what to prioritize.

### Goals vs tasks (hard)

A goal requires **strategic thinking and real work** to achieve. A task is a single chore you can knock out (book a slot, send a nudge, reply, file an invite).

**If the user ever names “schedule a call / book a meeting / get X on the calendar” as a week, month, or day goal, do not lock it.** Push back, even when they said it:

> That’s a task, not a goal. Goals need some strategic thinking and work. What is the work behind the call?

Then put the booking on Open Items as P0 if it is critical. Ask what the actual goal is (prep the demo, lock the spec, write the paper, get a decision). Same pushback for “nudge X” or “reply to Y” offered as a goal.

Lesson 2026-09-11: “schedule the ZF kickoff” is a Notion P0 task; the week #1 was prepare the internal onboarding v2 demo.

## Task systems (where work lives)

Goals are not the work tracker. Work lives in two places:

- **Linear** — team-visible delivery (projects, issues, eng/product launch work). Status of build lives here.
- **Personal Open Items** (Notion or equivalent) — the user’s concrete next actions and Waiting gates. Verb + next step. See [Open Items Cleanup](sand-workflow:open-items-cleanup).

When prioritizing:

- Map Open Items and Linear work **up** to month and quarter goals.
- Prefer Linear when the critical path is team delivery; prefer Open Items when the critical path is a personal gate (ask, decide, publish, unblock someone).
- Never treat a goal statement as an Open Item. Goals stay in memory; actions stay on the boards.

## Procedure — set or refresh goals

### 1. Load what already exists

- Read agent/user memory for locked quarter and month goals.
- If the user points at a doc, slide, or review form, read that as the candidate source.
- Note product naming conventions the user already locked (e.g. current product name vs legacy names in old docs).

### 2. Quarter (if missing, stale, or user wants to set)

- Collect 3–5 goals with: outcome, measure of success, target date, priority order.
- Each must pass the specificity bar **and** the goals-vs-tasks bar.
- Confirm with the user that this set is **source of truth** for the quarter (or through a named end date).
- Write to durable memory (profile-tier for the locked set). Include source link if any.
- Do not silently merge “what came up in a meeting” into quarter goals.

### 3. Month (under the quarter)

- For each quarter goal, propose 0–1 month outcomes that move it (not every quarter goal needs a month row every month).
- Allow a month goal that is personal/team-process even if it was not on a public team slide — confirm with the user.
- Enforce both bars; push back on nouns and on scheduling chores before locking.
- Name **month #1** explicitly. Design emphasis on a slide is not priority unless the user says so.
- Define “done looks like” in one line per month goal.
- Confirm and write to durable memory.

### 4. Week and day (lightweight; often separate briefs)

- **Week:** from Open Items (This week / Waiting) + Linear due/owned work + next week’s already-booked demos (as prep, not attendance), propose this week’s #1 as a work chunk under month #1, unless a hard external work-deadline forces a swap. One sentence. Optional #2 / #3, same work bar. If the user offers “schedule a call,” push back (goals vs tasks) and do not lock it.
- **Day:** from calendar + due Open Items + blockers, propose today’s #1. One sentence. A day’s #1 can be a hard same-day task when that is the truth; a **week** #1 cannot be “schedule a call.”
- Default: day’s and week’s #1 advance month #1 unless the user overrides with a real work goal.

### 5. Confirm and store

- Show the stack back: Quarter → Month (#1 called out) → optional Week #1 / Day #1.
- On lock, update memory. Forget superseded goal facts when replacing a whole set so old lists do not compete.
- Mention the skill as [Set Goals](sand-workflow:set-goals) when telling the user it is saved or updated.

## Using goals while managing tasks

Whenever prioritizing, scrubbing Open Items, drafting a Friday wind-down, or answering “what should I focus on?”:

1. Load quarter + month goals (and month #1).
2. Rank candidate **work** by: advances month #1 → advances other month goals → hard external work-deadline exception → everything else. Scheduling chores stay on the board; they do not win week #1.
3. Say the #1 for the timespan the user asked about (today / this week / this month).
4. If work does not map to any goal, flag it as cut, park, or ask whether a goal should change.

## Quality bar

1. How do we know goals are good? Each is an action/outcome sentence with a measurable done-state, requires strategic thinking and work, and has a clear #1 at month/week/day — never a bare noun, never a booking chore as the week’s #1.
2. How do we improve next time? After a miss (wrong #1, thrash, accepted vague goals, locked “schedule a call” even when the user said it), ask what should have won and patch this skill or the Friday wind-down.
3. Where is friction? User locks quarter and month; assistant pushes back on nouns and on tasks-posing-as-goals; proposes week/day #1 and only asks when two true work-P0s conflict.
