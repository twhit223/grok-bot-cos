---
name: open-items-cleanup
description: >-
  Use this when triaging or cleaning personal Open Items, or before ANY Open
  Items status (briefs, midday check, "what's left open"): run the inbox +
  today's-work reconcile first, then rewrite vague rows, cut seed leftovers,
  route discussion to 1:1 agendas, send team work to Linear, and set Waiting
  only when blocked.
---

# Open Items Cleanup

Triage personal Open Items so the board stays action-shaped. Use when reviewing the Open Items database, after a messy notes dump, during a standing cleanup pass, or when the user asks to clean / dedupe / rewrite Open Items.

This skill is for **judgment + board hygiene**. Meeting-notes ingestion (reconcile-first, Added/Updated/Closed) is a related pipeline; apply the same rules there, but do not treat this skill as a substitute for the notes-check routine.

## Goal

Every non-Done Open Item should answer: **what does the user do next, and what does done look like?** Cut or rewrite anything that fails that test.

## Inputs

- Open Items database (or dashboard view of non-Done rows)
- **Required:** email and Slack since the last reconcile (see Inbox reconcile below)
- **Required:** work finished in chat with the user today (drafts sent, packages delivered, decisions made)
- Optional: recent meeting notes, Linear issues linked in Notes
- Optional: Slack name roster / people directory (resolve misspellings before writing names)
- Known counterpart 1:1 prep themes (recurring discussion topics)

## Inbox reconcile (required before any Open Items status)

Run this before every brief, midday check, cleanup pass, or "what's left open?" answer. Notion status alone is never the truth. Lesson 2026-10-20: a status listed an item already subsumed by work sent that day, an item a colleague had already answered by email, and missed a new doc and a partner meeting ask.

Window: since the last reconcile (morning brief covers overnight; midday covers morning; EoD covers afternoon; ad hoc covers today).

1. **Today's work in chat.** List what the user and CoS finished today (sent emails/DMs, delivered packages, locked decisions). Any Open Item that work covers or subsumes -> **close** with reason. Don't ask the user to confirm the obvious.
2. **Email.** Search the user's inbox and threads they're on in the window, including replies by teammates on threads the user owns. If someone else already answered or did the thing an Open Item asks -> **close** with reason + thread. If a message asks the user for something new (a reply, review, decision, meeting) -> flag as **Open** (propose a new row).
3. **Slack.** Search mentions of the user, their DMs, group DMs, Slack Connect partner channels, and deal threads (e.g. the BD/GTM channel) in the window. Same rules: close what's resolved; flag new asks (doc shared "for you to review/send", "can we chat / share a scheduling link", questions tagged to the user).
4. **Waiting rows.** For each Waiting item, check whether the named gate replied. If so, flip to the user's next action (or close).
5. **Report** as three short lists: **Closed** (with reason), **New asks** (who, what, link, proposed Open Item), **Updated**. Skip FYI-only traffic (rule 10) and automated mail (builds, receipts).

Apply closes the user already implied without asking. Ask before adding new rows only when ownership is unclear; otherwise add them with Source = the message link.

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

- **Seed leftovers** (bulk import, opaque titles, empty Notes) often lack user context. Confirm origin/meaning before keeping; prefer cut when vague.
- **Ongoing ops** (from a just-processed meeting) should already have clear provenance; apply the same verb/Waiting/agenda rules without treating them as seed noise.

### 10. FYI / informing is not progress

- If the user only **informed** someone about an existing plan (no new decision, no new user next step, no date change they own), that is **not** an Open Item update.
- Do not rewrite Notes, move Due, or mark Updated just because the topic was mentioned in a meeting.
- Optional one-line in Notes (“Informed X on <date> — FYI only”) only when useful for provenance; default is leave the row alone and omit it from Updated.
- Lesson 2026-09-10: a partner integration was wrongly rewritten after the user informed a counterpart; reverted.

## Cleanup pass procedure

Run the Inbox reconcile first. Then work one non-Done item at a time (or a small batch the user is walking with you).

For each item:

1. **Read** Name, Status, Waiting on, Due, Notes, Source.
2. **Classify**: keep / rewrite / Waiting / move to agenda / move to Linear / cut.
3. **Ask the user** when the call is consequential or only they know (keep vs cut, who owns a gate, whether something is already done). Prefer a short question with real options.
4. **Apply** the change in Notion immediately after their call.
5. **Record** in Notes why it was closed or rewritten (one sentence + link).
6. Continue until Inbox is empty and every remaining row passes the verb test.

Do not silently close or rewrite without a reason the user can see in Notes.

## After cleanup (related work, not this skill’s body)

- Patch meeting notes-check to **reconcile existing Open Items before adding**, then report **Added / Updated / Closed** with reasons. Apply rule 10 (FYI ≠ Updated).
- Optional later: finite Slack watchers for Waiting items whose gate is a channel/mention (propose separately; do not invent watchers inside this skill).

## Quality bar

Before ending a cleanup pass or any Open Items status:

1. How do we know the board is good? Every non-Done row has a clear verb, Waiting rows name a gate, and nothing listed as open was already done today or answered by someone else.
2. How do we make it better next time? Every miss the user catches (stale row, missed inbound ask) becomes a dated lesson in the Inbox reconcile section.
3. Where is friction? User confirms keep/cut/agenda/Linear on ambiguous items; never silent mass-close. Obvious closes from today's work don't need confirmation.
