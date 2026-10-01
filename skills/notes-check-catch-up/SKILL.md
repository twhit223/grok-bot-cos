---
name: notes-check-catch-up
description: >-
  Use this when the user manually asks to run a missed meeting notes-check — find the overdue one-shot (or run from meeting title/time), process notes, then delete the one-shot. No automatic catch-up routine.
---

# Notes-check catch-up (manual)

Run a meeting notes-check that was scheduled but never fired, **only when the user asks**. There is no standing catch-up routine (removed 2026-09-10 as overkill; revisit if misses recur).

## When to use

- User says a notes-check did not run / asks to run it now
- User names a meeting whose end+10 one-shot is still sitting with `lastRunAt` null

## Steps

1. Find the matching `notes-check-*` routine (or reconstruct from calendar: meeting title, end time, date).
2. Execute the one-shot prompt intent: find notes, reconcile Open Items with [Open Items Cleanup](sand-workflow:open-items-cleanup), message Added / Updated / Closed.
3. Say it was a manual run because the scheduled wake missed (if that is why).
4. Delete the one-shot after handling (found or not found).
5. If misses become frequent, offer to restore an automatic catch-up routine.

## Quality bar

1. **Good:** user gets the same Added/Updated/Closed summary as a normal notes-check.
2. **Better:** log repeated misses; propose automation only after a second miss.
3. **Friction:** never run unprompted; never invent Open Items when notes are missing.
