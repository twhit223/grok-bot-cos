---
name: 1-1-meeting-prep
description: >-
  Use this when preparing a 1:1 agenda for the user with a named counterpart,
  or when drafting night-before shareable agendas for tomorrow’s 1:1s — gather
  relationship mode, pull discussion Open Items, propose or draft a short
  shareable talking-points list for the user to review before they share it.
---

# 1:1 meeting prep

Prep a 1:1 agenda the user can share. Start from context and relationship. Propose first. Iterate with the user until the final shareable form matches the output format below. Direct writing. No em dashes. No filler.

## Inputs

- Counterpart: display name (required for single-meeting runs)
- Meeting date (default: next scheduled 1:1 with them)
- Optional: Slack user ID, DM channel, email, calendar title keywords
- Optional: topics the user already wants on the agenda (merge in; do not drop)
- Optional: Open Items tagged as discussion with this person (merge in; see Step 3a)
- Optional: **night-before mode** (routine): draft shareable agendas for all of tomorrow’s 1:1s and deliver to the user’s review channel only

## Step 0 — Learn who this 1:1 is with

Before drafting topics, establish **relationship and mode**. Check agent/user memory for a prior profile of this counterpart. If missing, infer from calendar title, org context, and past notes, then confirm briefly with the user on first run and save to memory.

Capture at least:

- Name and role
- Relationship to the user (manager, report, peer, partner/customer, skip-level, other)
- What “good” looks like for agendas with them

Known examples (also in memory; refresh if contradicted):

- your manager (CEO): user’s manager → **manager mode**
- your direct report: reports to the user → **report mode**
- your peer: user’s peer → **peer mode**

### Relationship modes (filter the agenda)

**Manager (or CEO/skip-level upward)**

- Agenda informs them what the user wants to discuss. It is not a status dump.
- Favor high-leverage strategic decisions and places the user needs their feedback or input.
- Cut laundry lists of work in progress unless an item needs a decision or unblock from them.
- Keep the shareable version short and to the point. They should not need to answer questions in advance.

**Report (user manages them)**

- Agenda is for someone the user leads. Different goal than manager mode.
- Favor: their priorities and focus, blockers the user can clear, feedback/coaching, career/growth, decisions or clarity the user owes them, how their work ties to team goals.
- Include space for what *they* need from the user, not only what the user wants to tell them.
- Still avoid a dump of the user’s own cross-org status. The user’s work appears only when it sets context for the report’s priorities or a decision affecting them.
- Shareable version can be slightly more directive (priorities, asks, follow-ups) while staying short. Still no homework essay for them before the meeting unless the user wants that.

**Peer (same level; e.g. eng counterpart)**

- Agenda is shared working ground, not upward asks and not downward coaching as the default frame.
- Favor: joint decisions, handoffs, mutual blockers, sequencing across product/eng, ownership clarity, process agreements.
- Equal airtime: what each side needs from the other this week.
- Avoid turning it into a status recital or a manager-style “need your blessing” list unless a real decision needs both of you.
- Keep shareable version short and concrete (decisions, owners, next steps).

**Partner / customer**

- Favor joint decisions, handoffs, and mutual blockers with external or design-partner framing.
- Match their cadence and formality.

If mode is ambiguous, ask one clarifying question, then proceed.

## Step 1 — Find the meeting

- Calendar: primary calendar for the counterpart + “1:1” / “1-1” on the target day.
- Also treat clear 1:1-shaped titles (e.g. “the user <> your peer Sync”, “your direct report / the user”) as 1:1s when attendees are exactly the user + one counterpart.
- Record: start/end (user TZ), Meet/Zoom link, attendees, recurrence.

## Step 2 — Prior 1:1 notes

Search in order; stop when you have the latest usable notes:

1. Gmail: Gemini notes with both names / “1:1” in subject (newest first)
2. Google Drive: both names + `1:1`
3. Notion: “{{Name}} 1:1”

Extract: topics, decisions, open next steps with owners.

## Step 3 — Past-week context

Last 7 days through today, filtered by relationship mode:

- Slack DM and messages from/with them
- Notion Open Items: Waiting / This week / Open involving them
- Shared meetings and decisions that affect them
- For **report mode**: their recent deliverables, feedback threads, workload signals, career notes
- For **manager mode**: items needing the manager’s input or unblock; skip pure FYI busywork
- For **peer mode**: shared projects, eng/product seams, open handoffs, process docs you both own
- **ZF Launch / Product Timeline:** when the agenda covers ZF Launch module order, demo sequencing, or Product Timeline, pull the live primary product launch Linear initiative before drafting. Do not reuse stale sequencing from prior agendas or self-DMs.

Flag conflicts (Slack says done, Open Item still Waiting) instead of resolving silently.

## Step 3a — Discussion Open Items become agenda topics

Open Items whose only next step is “talk this through with this counterpart” are **agenda material**, not a second task list.

- Merge those items into the agenda proposal. Do not drop them. Do not keep a parallel Open Item once the user confirms the agenda.
- After the user locks the agenda (or locks a single topic onto it), mark those Open Items Done with a note that they live on this 1:1 agenda. Post-meeting notes-check extracts follow-ups into new Open Items.
- Do not file “attend this 1:1” or “give feedback in this scheduled review” as Open Items. Calendar owns showing up.
- Prep the user must finish *before* the meeting (a doc, a decision they owe async) can stay as an Open Item. The conversation itself cannot.

## Step 4 — Propose a working agenda (for the user first)

Build a **proposal for the user to edit**, not the final shareable note yet.

Rules for the proposal:

- Prefer decisions and input-needed items over status theater.
- For **manager mode**: every topic should answer “why does this person need to be in the room?” If it is only FYI, drop it or park under a single short FYI line.
- For **report mode**: every topic should answer “how does this help them do their job, grow, or get unblocked?” Mix their world and the user’s obligations to them.
- For **peer mode**: every topic should answer “what do we need to align or unblock together?” Prefer shared ownership over one-sided asks.
- It is OK if the highest-leverage asks are not obvious from the raw priority list. Propose anyway. The user will correct.
- Group into 4–6 top-level **bullet** topics. Under each, use nested bullets for subpoints. Do not number topics. Do not use a./b./c.
- Include a bit of context per bullet (one short clause), similar to a tight working draft — denser than the final shareable version is fine at this stage.
- If useful, add a private note for the user only (talking points, tension to watch). Do not put that in the shareable version unless they ask.

Shape for a 30 min slot: denser; park anything that needs >5 min debate.

Send the proposal to the user and **stop for iteration**.

## Step 5 — Iterate with the user

Expect rounds like:

- Add / cut / reframe topics
- Add a bit more or less context
- Correct facts
- Clarify form: all-bullets with each subpoint on its own line

Keep iterating until they say the substance is right. Then produce the final shareable form.

Do not send the counterpart anything unless the user explicitly asks you to.

## Step 6 — Final shareable output

When the user is happy with substance, rewrite to this form factor (**all bullets** — locked after Slack format test 2026-09-10):

```markdown
**1:1 agenda — {Day Mon D}**

- {Topic}
  - {Short point with a bit of context}
  - {Short point}
  - {Short point}
- {Topic}
  - {Short point with a bit of context}
- {Topic}
  - {Short point}
```

Requirements:

- Top-level topics are bullets; subpoints are nested bullets. Each subpoint on its **own line**.
- Do **not** use numbered `1.` / `2.` / `3.` for topics.
- Do **not** use `a.` / `b.` / `c.` (or `a.)` / `b.)` / `c.)`) for subpoints.
- Context level: enough that the counterpart knows what will be discussed; not so much they must prepare answers in advance.
- No asks that demand homework before the meeting (unless the user wants that).
- No CoS meta, no “locks table,” no private math, unless the user asks those in the shareable note.
- Apply Writing rules.
- Same form factor for all modes and surfaces (chat and Slack); **content** differs by mode.
- When posting to Slack, use standard markdown nested bullets (`-` with indented `-`).

Offer a paste-ready block. Optionally stash the final agenda in memory or an Open Item for the meeting day if the user wants.

## Step 7 — Night-before delivery (routine mode)

Use when a nightly routine asks for tomorrow’s 1:1 agendas, or the user asks to prep all of tomorrow’s 1:1s overnight.

### Detect tomorrow’s 1:1s

From tomorrow’s calendar (user TZ), keep meetings that are clearly 1:1s:

- Title contains `1:1`, `1-1`, or `one on one`, **or**
- Exactly two humans (user + one other) and title looks like a sync / 1:1 with that person

Skip declined, focus, OOO, all-day, and multi-attendee team meetings.

### Draft without waiting for chat iteration

For each 1:1, run Steps 0–3a + Step 6 **in one pass**: produce a **shareable draft** (not a long working proposal). Use memory themes, last notes, and discussion Open Items. Label it clearly as a draft for review.

If relationship mode is unknown and cannot be inferred, still draft in a neutral peer-like shape and note in chat that mode needs confirmation next time.

### Deliver for review only

1. Message the user in chat: short list of which 1:1 agendas are ready.
2. Post each shareable draft to the user’s **self-review Slack DM** (routine supplies the channel id). One message per 1:1, header includes counterpart name + time. Use Step 6 all-bullets form.
3. Tell them to clean up in Slack, then forward/share with the counterpart themselves.
4. **Never** message the counterpart. Night-before never auto-sends outbound.

### After they lock

When they say the agenda is good (or “done” / “sent”):

- Mark discussion Open Items Done (Step 3a)
- Store any new recurring theme in memory
- If they corrected the draft, patch this skill or counterpart memory so the next night-before run improves

### Quality bar (this automation)

1. **Good:** draft matches Step 6 all-bullets form; topics fit relationship mode; discussion Open Items appear; user can share after light edits.
2. **Better:** each correction updates skill/memory; recurring themes live in counterpart memory, not permanent Open Items.
3. **Friction:** night-before posts to self-DM only; user must review before sharing; never auto-send to the other person.

## Anti-patterns

- Treating report 1:1s like manager 1:1s, or peer 1:1s like either
- Laundry list of everything the user is doing
- Dual-tracking the same item in Linear and Open Items inside the agenda
- Dual-tracking a discussion topic as both an Open Item and an agenda line
- Inventing deadlines or commitments
- Final shareable note that is one long semicolon paragraph
- Final note packed with questions the counterpart must answer async first
- Skipping Step 0 relationship mode and treating every 1:1 the same
- Numbered top-level topics (`1.` / `2.`) with nested bullets in Slack or chat
- Prefixing nested bullets with a./b./c. labels
- Filing “attend the meeting” as an Open Item
- Auto-sending a night-before draft to the counterpart

## After first successful run with a new counterpart

Write a memory fact: `{Name} 1:1 mode: {relationship}; agenda style: {notes}`.
