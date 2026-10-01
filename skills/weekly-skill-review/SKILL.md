---
name: weekly-skill-review
description: >-
  Use this for a periodic review of user-created skills, or when the user asks to audit skills for bloat, quality-bar gaps, or missing data sources. Flag proposed edits; do not auto-edit other skills.
---

Use this for a periodic review of user-created skills, or when the user asks to audit skills. Flag proposed edits. Do not edit other skills until the user approves a flagged change.

The default outcome is **leave alone**, **cut**, or **replace**. Adding more instructions is last, not first. Improving skills weekly must not mean they only grow.

Depends on [Automation quality bar](sand-workflow:automation-quality-bar) for question 2. Do not copy that skill into this one.

Default trigger is phase 2 of [Friday weekly wind-down](sand-workflow:friday-weekly-wind-down) (Friday 1:00 PM sequence). There is no Sunday-night routine.

## Evidence this period

Load only what you need to answer the three questions:

- Skill files under the workflows library
- Corrections the user made this period (chat, memory log): especially “you should have looked at X,” “don’t do Y,” wrong owner, wrong shape
- Routines that run those skills
- Last review’s **Already fixed** list — do not re-propose those

Skip usage-count theater, unused-skill nits, and “optional after a few runs.”

## Three questions (every skill)

Answer these and nothing else.

### 1. Efficiency — bloat and stale content

Is the skill getting bloated? Are there data, routines, or instructions that are stale?

- Named people, dates, one-off lessons, or locked examples that belong in **memory** or a worked-example appendix, not the standing recipe
- Duplicate YAML, duplicated rules, or the same instruction in two skills
- Steps that encode a workaround already replaced
- Data that should be fetched live (calendar, Linear, Slack) but is frozen in the skill

If yes, the proposed change is a **cut** or a **move to memory**. Do not patch bloat by adding a fourth copy of the rule.

### 2. Framework — can it succeed at the task

Does the skill have enough context to succeed in the broader automation framework? Score it against the three quality-bar answers (in the skill, or obviously implied by a tight recipe):

- What does a good output look like / what is success?
- How do we improve the next time?
- Where is friction injected so the bar is met?

If an answer is missing, the patch is **a few named lines**, not a new essay. If the skill is a style/rules file rather than an automation, judge whether a run can tell pass from fail; don’t force a fake routine onto it.

### 3. Data sources — does it look in the right places

Does the skill name the sources it needs to do the job?

Propose new monitoring **only** when the user had to tell it to look somewhere this period (or the same miss repeated). Shape: add that source as a required input, or a finite watcher, or a standing scan the existing routine already runs.

Do not add sources “in case.” Do not clone a whole tool (Linear projects, Slack history) onto a personal plate when a filter already exists.

## What to flag

Flag a change only if at least one is true:

- Cutting stale content would make the skill cheaper to run
- The change would have changed a **real output this period** (wrong owner, wrong shape, missed ingest, a ban the user named that did not land)

Each flag: skill name, which question (1 / 2 / 3), proposed action (**cut** / **replace** / rarely **add source** or **name the quality bar**), one sentence why, and the evidence (user correction or stale passage).

## What not to flag

- Hygiene with no effect on output (unless it is true duplicate frontmatter that confuses editors)
- P2 “maybe later”
- Re-proposing already-fixed patches
- New automations the user already declined

## Output

1. Short TLDR: only the flags, grouped by question. If nothing material, say so in one line.
2. Dated report only if the calling routine asks for a file.
3. Wait for approval before any other `SKILL.md` edit.

Friday close (and any on-demand run) stays flag-only even when the recipe feels obvious.
