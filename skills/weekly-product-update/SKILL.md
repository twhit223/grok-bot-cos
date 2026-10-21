---
name: weekly-product-update
description: >-
  Use this when drafting the user's weekly Strongpoint / product update.
  Iterate in markdown; Lock Glance first; post to the product channel only
  after explicit approval.
---

Draft the user's weekly product update. Apply [Writing rules](sand-workflow:writing-rules) for voice. Write in first person as the user. Product name is **the product** (former name the former product name only in legacy channel/repo names or literal URLs).

This skill produces a **markdown draft for the user to edit**. Never post to Slack until he explicitly says to send. Drive `.md` archive in folder `YOUR_DRIVE_ARCHIVE_FOLDER_ID` only after he approves posting.

## Fixed destinations (do not re-search)

- `the product channel` channel id: `YOUR_PRODUCT_CHANNEL_ID` (default team post)
- the user self-DM id: `YOUR_SLACK_SELF_DM` (only when he asks for DMs)
- Drive archive folder id: `YOUR_DRIVE_ARCHIVE_FOLDER_ID`

## Iteration rule (hard)

Always draft and revise in `.md` first. Put the working file under `/workspace/weekly-product-update/YYYY-MM-DD/draft.md` (week start date). If he wants another revision, edit the `.md`. After he approves posting, Slack gets the `.md`; Drive folder gets the same `.md` with the proper filename.

### Glance-first lock (hard; locked 2026-09-25)

Do **not** show a full draft on the first pass.

1. Before drafting, propose a short list of candidate "what the team needs to know this week" points (manager-level, most important first). Let the user pick and correct them, then draft **only** This Week at a Glance (plus title / week window) around his picks.
2. Share that Glance alone in chat. Get an explicit yes (or his rewrite).
3. Only then draft Build, Key Scoping, Open Product Questions, Customer, Next Week Focus, ICYMI, Future.
4. Share the full stand-alone draft after Glance is locked.

Most Friday thrash is Glance and Key Scoping. Locking Glance first cuts rebuilds.

### Stand-alone handoffs (hard)

When sharing Glance or any later draft in chat, paste the readable markdown as the team will see it. Never narrate edits ("Dropped the Notion aside", "I shortened X", "per your last note"). No edit-history contrast. Each share must stand alone. Same bar as Writing rules for published drafts.

## Prior weeks (structure only, not voice)

Use these for **section order and what kinds of content belong where**. Do **not** copy their prose rhythm. the user finds those Docs Claude-sounding; matching them is a failure.

- Week of Aug 3–7, 2026 — `YOUR_PRIOR_WEEK_DOC_URL`
- Week of July 27–31, 2026 — `YOUR_PRIOR_WEEK_DOC_URL`
- Week of July 21–24, 2026 — `YOUR_PRIOR_WEEK_DOC_URL`

Better voice references: the user's own Slack messages that week (direct, concrete, short). Prefer that over any prior Product Update Doc.

Gold structure reference after Sep 11, 2026 edits: `/workspace/weekly-product-update/2026-09-07/draft.md` (one home per topic, Build by dimension, Open Questions after Build as product questions, Key Scoping as closed company facts). Still do not copy its prose.

## Slack post heading (hard rule)

When posting the weekly product update to Slack (`the product channel`, self-DM, or any other Slack destination), the **only** allowed message heading is:

```text
:page_with_curl: *Weekly Product Update: <Mon D>-<D>*
```

Examples:
- `:page_with_curl: *Weekly Product Update: Aug 3-7*`
- `:page_with_curl: *Weekly Product Update: Aug 31-Sep 4*`

Rules:
- Bold the title line with Slack mrkdwn single asterisks `*...*` (emoji stays outside the bold). Double asterisks or markdown conversion can render italic; check the posted message.
- Dates are the Mon–Fri window label only (`Aug 31-Sep 4`).
- That heading is the entire Slack message text above the `.md` attachment. No alternate titles, no soft openers, no "here's this week's update", no extra preamble.
- Post that heading with the final `.md` file attached under it. Do **not** use a Google Doc link as the Slack post body.
- Any other Slack heading format for this update is a failure.

## Post path (hard; locked 2026-09-25)

Default after the user says post (or "go ahead and post"):

0. **Exact-preview gate (hard; locked 2026-10-09).** Before posting, paste the exact final post in chat: the Slack heading line exactly as it will be sent (`:page_with_curl: *Weekly Product Update: <dates>*`), the full final `.md` body, the destination channel, and whether it goes as an attached `.md` or a Drive link. Post only after the user replies "post" to that exact preview. Any change after the preview needs a new preview.
1. Post to `the product channel` (`YOUR_PRODUCT_CHANNEL_ID`): locked heading + attach final `.md`.
2. Archive the same `.md` into Drive folder `YOUR_DRIVE_ARCHIVE_FOLDER_ID` with filename matching the H1. Keep markdown (`disableConversionToGoogleType: true`). Do not convert to a Google Doc.

Self-DM (`YOUR_SLACK_SELF_DM`) only when he explicitly asks for DMs (e.g. "post to my dms"). Do not default to self-DM first.

## One home per topic (hard)

Do not retell the same story at three depths. Pick a home.

- **Customer / partner paper** (term sheet, MOU, design-partner close tied to the $1M / EoY goal): one line in Glance because it is the company goal, full story only in **Customer Insights & Updates**. Not a Build subsection.
- **Process / cadence / brand calls** (demo cadence, logo/brand color, who owns marketing vs site): **Key Scoping Decisions** only. Not Glance detail, not a Build subsection. Do not write that named people "are aligned." Describe the decision in words the company can read (a chosen logo and brand color), not an internal option number.
- **Partner waits** (still need their answer before we can date or cut): **Customer Insights** only. Not Key Scoping, not Open Product Questions.
- **Engineering movement + one key product conversation** (recovery workshop, architecture review): **Build Progress**. Link the notes. Put the unresolved choice in Open Product Questions, not as a second Build essay.
- **Personal product P0s** that are not in customer Slack (example: publishing an internal plugin) still belong in the update if the user owned them this week. Check Open Items and Linear assigned to them. One Build line + Next Week Focus if still open.

### Hard output rules (locked 2026-09-18; Glance + speedups 2026-09-25)

- **Glance shape and reader (hard; locked 2026-10-09):** Two short paragraphs. Open with one sentence naming the week's theme, then at most two sentences per paragraph after that. Write for a teammate who attended no meetings and does not track product daily: spell out partner names on first use (the design partner (Partner org), our first design partner), say in plain words what each term means and why it matters, and use no internal labels. Match the user's posted Glance voice (connected sentences, "Alongside that…"). No punchy fragment openers, no "X is the bar", no "the open pressure is", no tidy triads.
- **Glance opens with the quarter's roadmap (hard; locked 2026-10-16):** The FIRST paragraph leads with the quarter's product roadmap (Q4 2026 = primary product launch): its status for launch (on track, ahead, or behind) and how it changed this week. Write it as high-level manager commentary (what mattered, what the broader team needs to know), NEVER an enumeration of the roadmap, sprints, or modules.
- **This Week at a Glance is strategic, not a laundry list (hard):** 1–2 short paragraphs that summarize the most relevant strategic progress the team needs to know. Theme + why it matters + the main open product pressure. Not a checklist of dates, demos, emails, partners, and ship notes. Operational detail (SSO emails, milestone dates, staging surfaces, partner names beyond the theme) belongs in Build, Customer, or Key Scoping. If Glance reads like a bulletin board of “things that happened,” rewrite it. Align Glance to locked week goals (name the work, never `#1`/`#2`/`#3` in published text).
- **Week length spine (first pass):** Draft from the user’s Daily focus Today’s #1, Mon–Thu EoD accomplishments, and locked week goals **before** broad Slack/Linear archaeology. Broad gather is gap-fill only after that spine exists. Prefer a short company-readable update over an exhaustive gather dump.
- **Never invent company framing (hard):** Do not promote Linear-audit takeaways, CoS hypotheses, or module-philosophy slogans into Glance or Key Scoping unless the user said them (example ban: “Onboarding & Recovery as the spine”). Linear audits stay in `sources.md` / handoff, not the team-facing draft.
- **Week-goal numbering:** Never refer to the user’s personal week goals by opaque number (`#1` / `#2` / `#3`) or phrases like “closes week #3.” Readers lack that context. Naming the actual work is fine (e.g. published External Writing bot, finished Product announcement blog).
- **ZF Launch as source of truth for sequencing/testing:** Before writing Key Scoping or Open Product Questions about ZF module order, demos, or testing checkpoints, pull the live Linear initiative **primary product launch** and its module projects/milestones. Do not invent or revive an older product sequencing (e.g. dashboard → approvals+policies → audit) when the initiative already defines the module cadence. Still: only publish framing the user (or a closed company call) actually stated.
- **Post-demo feedback:** Never dump Team Demo feedback themes into the update. Report only the a leadership sync (or a product decision that came out of it). Individual themes stay off the team-facing update until categorized and decided.
- **Teammate-bot rollout:** When reporting Grok Bot / writing-bot publish status, check the live team-store artifact (publish URL / install link) and the bot’s current display name — do not hard-code a stale name (External Writing vs PhD Writing) or rely only on Linear Todo status.
- **Deck / public link verification (hard):** Before publishing slide decks, Figma, Claude Design, Drive, or similar public links, verify the URL from the source thread (e.g. GTM Slack) or the artifact owner. Do not trust Open Items alone; Open Items can hold stale or wrong links.

## Document structure (required sections, in order)

Title: `Product Update: Week of <Month Day> to <Day>, <YYYY>`

**Week window is always Monday through Friday** in the user's timezone (America/Los_Angeles), even if the draft runs mid-week or on Friday. Example: if Friday is Sep 4, the week is August 31 to September 4 (not Sep 1–4). Slack date label matches that range (`Aug 31-Sep 4`). Never use a partial week start.

1. **This Week at a Glance** — 1–2 short paragraphs. A thoughtful strategic summary of the most relevant progress the team needs to be aware of. Theme, why it matters, goal-relevant customer signal if one exists, and the main unresolved product pressure. Narrative prose only. Never a laundry list, date stack, or preview of every later section. If you are listing more than ~2 closed moves plus one open pressure, you are overstuffing Glance. **Lock with the user before drafting later sections.**
2. **Build Progress** — Brief. Group by **dimension of progress**, not by person. Typical buckets: Product (product surfaces), AI process (agent loop, dashboards, internal plugins), and any other real track that moved (e.g. PEAK). Names can appear inside a bucket when they did the work. Do not write a paragraph per engineer.

   Then at most one or two key product conversations, with a notes link. No partner term-sheet recap. No demo-cadence paragraph.

   Include a **Key Scoping Decisions** subsection when eng/product **closed** architecture or process calls that week (do not leave those as open questions). Closed calls live here, not restated in Build prose.

   Closed means someone actually called it (the user, or eng agreement that survived the rest of the week). Not a workshop ranking, "lean," "preferred," "most viable near term," or option 2 of 6 in notes. If the same thread later that day has the user (or the update owner) saying the option is not acceptable, it is **not** Key Scoping. Read the thread to the end before promoting notes. Soft takeaways stay in Open Product Questions or as a Build conversation with a notes link.

   Each scoping item is one or two **actual sentences that explain the decision**. Not a bold telegram label plus a fragment. If Alex would have to decode the heading, rewrite it as prose. No internal option numbers. Partner framing is not Key Scoping until the partner has answered and the cut is real.

   **Do not** add a Linear/Notion "surface status" subsection. Ticket movement is input only. Do not dump ticket IDs.
3. **Open Product Questions** — Directly after Build / Key Scoping. Numbered. Each **bold lead is an actual question**, not a noun label or a snippy dump. **Questions only (hard; locked 2026-09-25):** do not elaborate under each question. No context paragraph, no "Next:" line, no Action Item tag. Do not park closed scoping decisions here. **Only questions the user has actually raised (hard; locked 2026-10-16):** ask them if unsure. Never promote technical open items from proposals or notes into this section.

   Questions are about **the product** (can we implement this, does the backend support it), not "does this belong in partner paper X." Partner-paper membership is Customer Insights, or Key Scoping if it actually closed.
4. **Big Product Changes** — *Only for real product changes shipped or agreed in the product itself.* Skip for BD/partner deals, logo/brand/marketing, research notes, or process updates. If nothing qualifies, omit the section.
5. **Customer Insights & Updates** — One subsection per conversation (Name, Company). This is the home for customer/partner updates, including waits on their answers. Lead with who they are. What changed this week, what is still true, what is next. Link notes (verified). Not a second copy of Glance.
6. **Next Week Focus** (exact heading; locked 2026-10-16) — Short bullets listing only the locked next-week goals, primary first. No actions list.
7. **Last Week (ICYMI)** — Link to the prior week's Doc (or `.md` if no Doc yet).
8. **Future product exploration** — *Optional footnote at the end.* the user's Q4 goal. Short. Not titled Side Quest. Never name `the exec channel` or other exec-only channels in the team-facing update.

Do not invent sections. Do not pad empty sections with filler.

## Audience and channel hygiene

This update goes to the whole team via `the product channel`. Write for company-wide readers.

Assume the reader was not in any of the team meetings this week. Do not use option letters, meeting jargon, or other insider labels. Jargon from a meeting is unacceptable because it assumes the reader has context they do not have. Say the decision in plain company language.

Never:
- Cite `the exec channel` or other exec-only venues as the source. The team does not need "we decided this in execs."
- Ask execs for information, name private exec asks, or surface exec-meeting homework (quarterly goals lists, department source-of-truth debates, "Alex send me X", board-slide prep) in the published update. Keep that in DMs / exec forums only.
- Put deploy/ops minutiae (who wires Northflank Monday, .env handoffs) in **This Week at a Glance**. Those details belong in Build Progress if they matter at all.
- Over-sell internal tools that are still exec-only. The company roadmap tool starts as exec collaboration; in the company-wide update give light context only (that it exists / is being built for planning). Do not frame it as a whole-team rollout, invite the company to use it, or dump deploy/repo instructions.

**Do** put product decisions that closed in execs into **Key Scoping Decisions**, written as company facts (what we ship, what we delay, what capacity we protect). `the exec channel` and leadership notes are a required gather source for Key Scoping. Keep-out is the venue and the homework, not the decision.

Glance is strategic summary only: what moved that matters and why, plus the open pressure. Not a laundry list. Verify design/call claims against Gemini notes or transcripts before summarizing (do not harden a soft takeaway into a kill decision).

## Voice and bar

Writing rules are the voice. Failures to avoid specifically in this skill:

- Citing internal doc section numbers (§3.4, Section 4, etc.) in the company-wide update. Readers do not have that doc open. Say the decision in plain words.
- Padding a decision the user already stated with extra verification archaeology (restating the whole policy model, channel thread meta, acceptance-criteria cross-refs) unless he asked for it. When he gives the cut or the wording, use that. Stop.
- Claude polish: stacked parallel clauses, brochure density, tidy corporate rhythm, soft glue ("clarified the model", "line up with", "forward guidance", "consensus", "the question hanging over everything").
- Monster one-sentence scope dumps. Break into short sentences or bullets.
- Bold on every subsection lead-in. Bold sparingly.
- Meta agent talk ("in sources I pulled", "no writeups this week" as filler).
- Em dashes. Banned vocabulary and negative-parallelism reframes from Writing rules.
- Matching the old Product Update Docs' prose because they "sound official."
- Repeating the same topic across Glance, Build, and Customer at varying depth.
- Referencing a previous draft. The team (and Alex) only see this version. No "not just X" leftovers from an earlier pass, no "I'll update this line," no edit-history contrast. Each rewrite must stand alone.
- Person-by-person Build (Ralph did X, your peer did Y). Group by Product / AI process / other real tracks.
- Key scoping as bold fragment labels. Write the decision in sentences.
- Promoting a workshop lean into Key Scoping. "Seems most viable," "preferred near term," or a ranked option is not a closed call, especially if the user contradicted it the same day.
- Referring to personal week goals by number (`#1`, “week #3”) instead of naming the work.
- Dumping raw Team Demo feedback themes; write a leadership sync / decision only.
- Writing ZF module sequencing or testing Open Questions without checking primary product launch first.
- Glance as a laundry list of things that happened (dates, emails, partner names, staging bullets). Rewrite as strategic summary.
- Inventing company framing from Linear audits or CoS notes the user did not state.
- Publishing deck/links from Open Items without verifying the source thread.
- Elaborating under Open Product Questions (context / Next / Action Item). Questions only.
- Showing a full draft before Glance is locked.

Do:
- Sound like the user talking to the team in Slack.
- Short paragraphs. Contractions. Uneven rhythm. Fragments when natural.
- Names, dates, numbers, concrete tradeoffs.
- Take a stance when the evidence supports one.
- Flag challenges to the company thesis explicitly.
- Keep length tight. Cut when the point is made.

## Gathering inputs (before writing)

Pull what exists. Do not invent meetings or ship claims.

**Order (hard):**

1. Locked week goals (name the work; never publish `#1`/`#2`/`#3`).
2. Daily focus Today’s #1 for each weekday + Mon–Thu EoD accomplishments. This is the draft spine.
3. Prior week's update (continuity + ICYMI link).
4. Then gap-fill only as needed from the sources below.

Typical gap-fill sources (use what is connected; skip what is not):

1. Slack: `the product channel`, Product / `the legacy-product channel`, `the product-testing channel`, `the business-development channel`, `the design channel`, `the exec channel`, the engineering Slack (`the engineering channel`), and the user's DMs/threads that week. Search the user's messages and customer/partner notes. For Key Scoping, also scan `the exec channel` and leadership notes for closed product calls (`DECISION`, what we ship / delay / protect). Publish the facts, not the venue.
2. **Build Progress gather (required for Build section):** Engineering Linear issues that completed or meaningfully moved this week, plus `the engineering channel` (PRs, RFCs, mid-week ship notes). If someone posted a ship snapshot that week, use it as the spine. Cover every engineer who shipped this week, not only whoever asked for a review. Ticket IDs stay in the sources file. **Write** Build by dimension (Product / AI process / other real tracks), not as a paragraph per person.
3. Linear: issues the user touched, Product / product projects moved this week (background only). **Also** issues assigned to them that they would call a P0 (internal tools, plugins). Those belong in the update even if they never hit `the product channel`.
4. Personal Open Items. Useful for reminders; **not** authoritative for public deck/links (verify those from source threads).
5. Calendar / Gmail (when connected): customer or partner calls that week; match to notes.
6. Demo / roadmap / Notion: what actually changed in the product surface.
7. **primary product launch (required for ZF sequencing/testing lines):** Linear initiative + module projects/milestones before Key Scoping or Open Questions about module order, demos, or partner testing checkpoints. Keep invented framing out of the published draft.
8. **Team bot publish (when claiming a bot shipped):** team-store / x.ai bot URL and live display name, not Linear Todo alone.
9. Anything the user already logged as wins that week.

If a source is thin, write from what you have and mark gaps in the handoff (`Missing: …`) rather than fabricating. Do not publish standup asks that exist only in a CoS chat unless he says to include them.

## Output artifacts

1. **`draft.md`** — the only working draft during iteration.
2. **`slack-announcement.txt`** — exactly `:page_with_curl: *Weekly Product Update: <dates>*`.
3. **Handoff to the user** (chat):
   - First: Glance alone for lock (stand-alone; no edit narration).
   - After Glance yes: full stand-alone draft (no edit narration).
   - Optional short bullets only for least-sure claims / missing notes that need his call (not a rewrite diary).
4. After the user says the markdown is final and approves posting:
   - Default: post to `the product channel` (`YOUR_PRODUCT_CHANNEL_ID`) with locked Slack heading + attach the final `.md`.
   - Self-DM (`YOUR_SLACK_SELF_DM`) only if he asked for DMs.
   - Then upload that same `.md` into Drive folder `YOUR_DRIVE_ARCHIVE_FOLDER_ID` with filename `Product Update: Week of <Month Day> to <Day>, <YYYY>.md` (match the H1). Keep it as markdown (`disableConversionToGoogleType: true`). Do not convert to a Google Doc for the archive.

## Quality gate (always)

1. **Good?** Every Build and Customer claim traces to a source from this week. Glance was locked before the full draft. Glance stands alone without retelling later sections. Build is by dimension. Each Open Product Question is a product/implementation question **with no elaboration under it** (not a partner wait). Key Scoping items are closed company facts the user (or a closed call) actually stated (not leans, not option numbers, not invented framing, not partner framing we do not have answers for). Every published deck/link was verified from the source thread, not Open Items alone. Prose passes Writing rules. Chat handoffs are stand-alone (no edit-history narration).
2. **Better next time?** After the user edits the `.md`, patch this skill with what he changed (tone, cuts, facts he added). Default is cut/replace, not a new essay.
3. **Friction?** Glance lock first. Markdown review next. Slack `.md` post and Drive archive only when he says post. Default destination is `the product channel`.

## Out of scope

- Daily launch-war-room updates (different format).
- Partner-facing or external blog posts.
- Replacing Linear project status; this is the user's narrative product brief.
