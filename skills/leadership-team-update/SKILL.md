---
name: leadership-team-update
description: >-
  Use this when Leadership (or an equivalent exec product meeting) is the next
  day, or when the user asks to craft the team update. Weight Top 3 from the
  curated weekly product update Glance (then Key scoping); other sources only
  confirm or fill gaps. Discussion = only strategic questions needing
  whole-Leadership alignment. Draft slide copy in CoS chat only (not Slack
  self-DM); no Figma unless asked. When Top 3 claims a teammate bot shipped,
  verify the live team-store display name.
---

# Leadership team update

Use this when the user’s next Leadership (or equivalent exec product meeting) is tomorrow, or when they ask to craft the team update for that meeting.

This is a **spoken/slide copy draft**, not a status dump and not the weekly product update. Match the user’s existing Leadership slide pattern. Do not build Figma or other slide files unless they ask.

## Format (hard)

One weekly slide. Title: `Week of <that week’s Monday>`.

Left/main: **Top 3 things from last week**
- Numbered `01` `02` `03`
- Each item: short title (a completed fact, not a noun-only label) plus one line of subtext
- Subtext can name a remaining concrete action (who/what). Do not use empty “[X is next]” / “X next” / “Next is X” labels

**Top 3 filter (hard):** the three **highest-strategic things Product (the user and their team) got done** last week that the **whole company should hear**.

Count:
- Work the user personally did: demos, explanations, scoping with a counterpart, shipping a team tool, workshops they owned
- Wins by people who report to them (**the team**, not only the user). Design work from a report is in scope when Product owns the outcome. Do not dismiss design as “not worth reporting.”
- Name the person in subtext when a report did the work

Do not count:
- Decisions already made in an exec/leadership forum last week. The room already heard them. Read those notes before ranking.
- Follow-on execution someone else owned after the user already reported their part (example: user provided product scope last week; BD took feedback and got the paper signed. The sign is not Product’s top 3.)
- Work a peer function owns even if a Product report helped (example: brand / marketing wrap → marketing owner reports it, even if a Product designer did the design). Leave that off Product’s slide.
- Adjacent company news or “schedule a meeting”

## Primary source: weekly product update (hard; locked 2026-09-28)

the user curates the weekly product update. Treat that post (especially **This Week at a Glance**, then Key scoping) as the **default candidate pool and weighting** for Top 3.

1. Load the latest posted Weekly Product Update for the week that is “last week” relative to Leadership (Slack `the product channel` and/or `/workspace/weekly-product-update/<week-start>/draft.md`).
2. Parse Glance beats in order. Lead sentence / first paragraph is usually the #1 candidate. “Alongside” / second beat is usually #2. Later beats compete for #3. Soft closers (“Lastly…”, writing polish, ICYMI) are lower weight unless he marked them as the company story.
3. Prefer Key scoping closed facts when they are company-visible Product decisions.
4. Use calendar, exec notes, Pipeline Review, Linear, Open Items, and report wins only to (a) confirm what Leadership already heard, (b) fill a clear gap Glance under-weighted, or (c) name people/dates in subtext. Do **not** invent a Top 3 from archaeology that contradicts what Glance led with.
5. Show the ranking in chat: Glance beats → proposed `01`/`02`/`03` with one-line why → any reject with why. Then draft slide copy.

Gold example (Week of Sep 13, locked 2026-09-15): design partner progress (demo + explain with your counterpart, verbal MOU in flight); a design-partner review (with your peer, waiting on comments); shipped CoS (published, piloting with EA). Rejected: Q4 scope (exec call already heard); partner term-sheet execution (BD, after last week’s product-scope #1); the product brand as Product top 3 (marketing owns the report, even though your direct report did design work).

Right/discussion: **Open items**
- Only **strategic questions** that need **input or alignment from the entire Leadership team**
- Phrase as real questions (decision, tradeoff, constraint)
- Prefer thin and right over padded. One real question beats three soft ones.
- Carry unresolved whole-room questions from the prior Leadership slide; drop ones that closed

**Discussion bar (hard) — do NOT put on the slide:**
- Feature / product-design calls the user should make with Eng (example: recovery set-once default). Too low-level for all executives.
- Strategic questions that only need a quick check with one person (usually Report 1:1), even if the topic is company-level (example: Q4 thesis mostly locked in Research; confirm with your manager, not Leadership).
- Updates already aligned elsewhere (Pipeline Review, BD/Prod/Eng sync). Those are status, not Discussion. Read those notes before proposing.
- Waits on an outside party, personal scheduling, or restating a top-3 outcome as “should we pursue”
- Open Product Questions from the weekly update that are Eng/product design calls (recovery root key, spend policies) stay off Discussion unless they need whole-Leadership alignment

Gold Discussion example (Week of Sep 13): who from Leadership needs to be in the room for design-partner working sessions (first kickoff and ongoing). Rejected same day: recovery default (feature / Eng); Q4 thesis (Report 1:1); partner capacity (already aligned in Pipeline Review — update, not a question).

Optional standing **month goals** slide: leave it unless a goal line is now wrong. Do not restyle it every week.

## Voice

Write as the user would say it in the room. Short. Specific names, dates, and closed calls. Product name as the user uses it. No em dashes. No assistant preamble on the slide copy.

A first-time listener should understand each line without last week’s slide.

## Inputs

1. **Posted weekly product update for last week** (Glance first, then Key scoping, Build, Customer) — primary
2. Prior Leadership updates (last slide’s top 3 and open items)
3. Last week’s exec/leadership notes and **Pipeline Review / BD–Prod–Eng notes** (only to drop already-heard / already-aligned items)
4. Direct-report wins only when they are missing from Glance and Product owns the outcome
5. Research bot / thesis state before proposing product-direction Discussion
6. Do not invent partner or eng certainty
7. When Top 3 claims a teammate bot shipped, verify the live team-store display name (open the bot store URL / published bot page). Do not hard-code “External Writing” or any stale internal name.

## Steps

1. Confirm the meeting is Leadership **tomorrow** (or today if they asked in the morning). Resolve dates in the user’s local timezone.
2. Load last week’s Weekly Product Update. Extract Glance beats + Key scoping. Read prior Leadership Discussion carryovers and Pipeline/exec notes only to filter already-heard items.
3. Rank Top 3 from Glance weighting. Show ranking + rejects in chat before locking copy, unless they already named the three. If any candidate is a shipped teammate bot, confirm the live team-store display name first.
4. Draft Discussion only if a real whole-room strategic question exists. Prefer one strong question over filling the box. Cut feature calls, 1:1-only asks, and updates.
5. Draft the slide copy **in this CoS chat** for the user to paste into slides. Night-before and morning runs use the same path.
6. **Do not** post Leadership slide copy to Slack self-DM (or any Slack channel). 1:1 agendas still use self-DM via [1:1 meeting prep](sand-workflow:1-1-meeting-prep); Leadership does not. Do not message the Leadership attendees.
7. Stop. Do not post to a team channel. Do not build slides unless asked.

## Quality

Good: three Product-team outcomes that match what Glance led with, plus Discussion questions only Leadership as a whole can answer.
Bad: archaeology that ignores the curated update, feature decisions in Discussion, Alex-only checks in Discussion, Pipeline Review updates dressed as questions, peer-owned reports in Top 3, dismissing design, listing tickets.
