---
name: weekly-product-update
description: >-
  Use this when drafting the user weekly the product / product update. Iterate in markdown; Lock Glance first; post to the product channel only after explicit approval.
---

Draft the user weekly product update. Apply [Writing rules](sand-workflow:writing-rules) for voice. Write in first person as the user. Product name is **the product** (former name the former product name only in legacy channel/repo names or literal URLs).

This skill produces a **markdown draft for the user to edit**. Never post to Slack until he explicitly says to send. Drive `.md` archive in folder `YOUR_DRIVE_ARCHIVE_FOLDER_ID` only after he approves posting.

## Fixed destinations (do not re-search)

- `the product channel` channel id: `YOUR_PRODUCT_CHANNEL_ID` (default team post)
- the user self-DM id: `YOUR_SLACK_SELF_DM` (only when he asks for DMs)
- Drive archive folder id: `YOUR_DRIVE_ARCHIVE_FOLDER_ID`

## Iteration rule (hard)

Always draft and revise in `.md` first. Put the working file under `/workspace/weekly-product-update/YYYY-MM-DD/draft.md` (week start date). If he wants another revision, edit the `.md`. After he approves posting, Slack gets the `.md`; Drive folder gets the same `.md` with the proper filename.

### Glance-first lock (hard; locked 2026-09-25)

Do **not** show a full draft on the first pass.

1. Draft **only** This Week at a Glance (plus title / week window).
2. Share that Glance alone in chat. Get an explicit yes (or his rewrite).
3. Only then draft Build, Key Scoping, Open Product Questions, Customer, Next Week, ICYMI, Future.
4. Share the full stand-alone draft after Glance is locked.

Most Friday thrash is Glance and Key Scoping. Locking Glance first cuts rebuilds.

### Stand-alone handoffs (hard)

When sharing Glance or any later draft in chat, paste the readable markdown as the team will see it. Never narrate edits ("Dropped the Notion aside", "I shortened X", "per your last note"). No edit-history contrast. Each share must stand alone. Same bar as Writing rules for published drafts.

## Prior weeks (structure only, not voice)

Use these for **section order and what kinds of content belong where**. Do **not** copy their prose rhythm. the user finds those Docs Claude-sounding; matching them is a failure.

- Week of Aug 3–7, 2026 — `YOUR_DOC_URL
- Week of July 27–31, 2026 — `YOUR_DOC_URL
- Week of July 21–24, 2026 — `YOUR_DOC_URL

Better voice references: the user own Slack messages that week (direct, concrete, short). Prefer that over any prior Product Update Doc.

Gold structure reference after Sep 11, 2026 edits: `/workspace/weekly-product-update/2026-09-07/draft.md` (one home per topic, Build by dimension, Open Questions after Build as product questions, Key Scoping as closed company facts). Still do not copy its prose.

## Slack post heading (hard rule)

When posting the weekly product update to Slack (`the product channel`, self-DM, or any other Slack destination), the **only** allowed message heading is:

```text
:page_with_curl: **Weekly Product Update: <Mon D>-<D>**
```

Examples:
- `:page_with_curl: **Weekly Product Update: Aug 3-7**`
- `:page_with_curl: **Weekly Product Update: Aug 31-Sep 4**`

Rules:
- Bold the title line with `**...**` (emoji stays outside the bold).
- Dates are the Mon–Fri window label only (`Aug 31-Sep 4`).
- That heading is the entire Slack message text above the `.md` attachment. No alternate titles, no soft openers, no "here's this week's update", no extra preamble.
- Post that heading with the final `.md` file attached under it. Do **not** use a Google Doc link as the Slack post body.
- Any other Slack heading format for this update is a failure.

## Post path (hard; locked 2026-09-25)

Default after the user says post (or "go ahead and post"):

1. Post to `the product channel` (`YOUR_PRODUCT_CHANNEL_ID`): locked heading + attach final `.md`.
2. Archive the same `.md` into Drive folder `YOUR_DRIVE_ARCHIVE_FOLDER_ID` with filename matching the H1. Keep markdown (`disableConversionToGoogleType: true`). Do not convert to a Google Doc.

Self-DM (`YOUR_SLACK_SELF_DM`) only when he explicitly asks for DMs (e.g. "post to my dms"). Do not default to self-DM first.

## One home per topic (hard)

Do not retell the same story at three depths. Pick a home.

- **Customer / partner paper** (term sheet, MOU, design-partner close tied to the $1M / EoY goal): one line in Glance because it is the company goal, full story only in **Customer Insights & Updates**. Not a Build subsection.
- **Process / cadence / brand calls** (demo cadence, logo/brand color, who owns marketing vs site): **Key Scoping Decisions** only. Not Glance detail, not a Build subsection. Do not write that named people "are aligned." Describe the decision in words the company can read (a chosen logo and brand color), not an internal option number.
- **Partner waits** (still need their answer before we can date or cut): **Customer Insights** only. Not Key Scoping, not Open Product Questions.
- **Engineering movement + one key product conversation** (recovery workshop, architecture review): **Build Progress**. Link the notes. Put the unresolved choice in Open Product Questions, not as a second Build essay.
- **Personal product P0s** that are not in customer Slack (example: publishing an internal plugin) still belong in the update if the user owned them this week. Check Open Items and Linear assigned to him. One Build line + Next Week if still open.

### Hard output rules (locked 2026-09-18; Glance + speedups 2026-09-25)

(Template excerpt: remaining steps follow the same conventions—generalize channel/repo names from memory; never invent commitments; ask before external posts.)

