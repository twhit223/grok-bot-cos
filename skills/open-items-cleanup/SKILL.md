---
name: open-items-cleanup
description: >-
  Use this when triaging or cleaning personal Open Items: rewrite vague rows, cut seed leftovers, route discussion to 1:1 agendas, send team work to Linear, and set Waiting only when blocked.
---

# Open Items Cleanup

Triage personal Open Items so the board stays action-shaped. Use when reviewing the Open Items database, after a messy notes dump, during a standing cleanup pass, or when the user asks to clean / dedupe / rewrite Open Items.

This skill is for **judgment + board hygiene**. Meeting-notes ingestion (reconcile-first, Added/Updated/Closed) is a related pipeline; apply the same rules there, but do not treat this skill as a substitute for the notes-check routine.

## Goal

Every non-Done Open Item should answer: **what does the user do next, and what does done look like?** Cut or rewrite anything that fails that test.

## Inputs

- Open Items database (or dashboard view of non-Done rows)
- Optional: recent meeting notes, Slack, Linear issues linked in Notes
- Optional: Slack name roster / people directory (resolve misspellings before writing names)
- Known counterpart 1:1 prep themes (recurring discussion topics)

## Status meanings

- **Inbox**: not yet triaged, or parked until triage
- **This week**: user’s action this week (or a dated raise in a named meeting this week)
- **Waiting**: user has no useful action until a named person/gate finishes; keep a verb for the action *after* unblock
- **Done**: closed with a reason in Notes (decision, moved to Linear, locked on agenda, superseded, cut as vague)

## Hard rules (cut / rewrite / route)

### 1. Clear verb + next step

- Title starts with an action verb naming the user’s next step.
- Notes say enough context to act (source, link, what done looks like).
- Outcome-only, surface-only, or program descriptions are not Open Items. Those belong in Linear, scope docs, or product sources of truth.
- If title/notes don’t answer “what do I do?”, cut or rewrite before keep.

### 2. Don’t over-split one conversation

- Related subpoints from the same discussion → **one** Open Item; put subpoints in Notes.
- Do not create sibling rows that are the same workstream under different seed phrasings.

### 3. Notion is the plate; Linear is ticket source of truth

Open Items must show **everything on the user’s plate** — personal next steps *and* assigned Linear work. One board to look at.

- **Linear** owns ticket status (Todo / In Progress / Done) for team-visible work.
- **Open Items** owns the plate view: one row per Linear issue assigned to the user, title includes the id (`Ship CoS plugin — TICKET-ID`), Notes start with the Linear URL.
- Never two rows for the same ticket (that was the TICKET-ID vs Notion P0 conflict). If both exist, keep one linked row; close the duplicate.
- Priority on the Notion row follows Linear (Urgent → P0, High → P1). Status: active work → This week or Top of mind; Backlog → Inbox; Linear Done → Done.
- Briefs: when a Linear issue moves or completes, update the linked Open Item the same run so the plate stays current.
- Do **not** hide Linear work by closing the Open Item “because Linear exists.” Closing is only for true duplicates or work that is no longer on the plate.

### 4. Calendar owns attendance

- Never file “attend this meeting” or “give feedback in this scheduled review.”
- Prep the user must finish *before* the meeting can stay as an Open Item.
- Actions that come *out of* the meeting come from notes-check afterward.
- If an Open Item’s next step is meet/align/define with someone and that meeting is **already on the calendar**, close it with “calendar owns: {title + date}” (or rewrite to prep-only with Due = meeting day). Do not leave it as This week.

### 5. Discussion → meeting agenda, then close

- If the only next step is “talk this through with X,” that is agenda material for [1:1 meeting prep](sand-workflow:1-1-meeting-prep) (or the named recurring meeting), not a standing Open Item.
- Lock the topic on the agenda with the user, then mark the Open Item Done with a note that it lives on that agenda.
- For a discussion that must stay visible until the meeting day, temporary shape is OK: verb title like “Align X and Y on …” or “Raise … in Friday eng daily”, Due = meeting day. After the meeting, notes-check replaces it with real follow-ups.

### 6. Recurring themes → prep memory, not Open Items

- Standing recurring topics (e.g. AI setup review every 1:1 with a report) live in counterpart 1:1 prep memory/skill.
- Close the Open Item; do not leave a permanent row for “keep talking about X.”

### 7. Waiting means blocked on someone else

- Status = Waiting only when the user has **no** useful next action until a named person/gate finishes.
- Always set **Waiting on** to the person or gate.
- Keep a user-verb title for what happens *after* unblock (e.g. “Schedule the partner deep-dive after your counterpart lands the NDA”).
- If the user still has work (nudge, draft, decide), it is not Waiting.

### 8. Names

- Resolve people against Slack (or the workspace roster) before writing Open Items, agendas, or notes-derived names.
- Do not copy Gemini misspellings into the board.

### 9. Seed vs ongoing

(Template excerpt: remaining steps follow the same conventions—generalize channel/repo names from memory; never invent commitments; ask before external posts.)

