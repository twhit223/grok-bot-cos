---
name: automation-quality-bar
description: >-
  Use this when proposing, designing, launching, or critiquing any automated task, bot workflow, skill, or routine for the user.
---

Use this whenever you propose, design, launch, or critique an automated task, bot workflow, skill, or routine for the user or your company.

Before the automation ships (or before you recommend shipping it), answer all three in writing:

1. **How do we know the output is good?**
   Name the acceptance check. Prefer a concrete artifact: a checklist, a sample of good vs bad output, a human review gate with a named reviewer, or a measurable pass/fail. If you cannot say what "good" looks like, do not automate yet.

2. **How do we make the output better the next time?**
   Name the learning loop. Prefer: edit the skill after each review, log failure modes, keep a short "known bad patterns" list, or require a post-run note that updates the template. Automation without a feedback path is a one-shot, not a system.

3. **Where do we inject friction so quality bars are met?**
   Name the forced pause. Prefer: human approval before send/publish/merge, a dry-run draft the user must accept, a second-agent critique step, or a blocked external action until a checklist is green. Put friction where a bad output would hurt: outbound messages, partner docs, code merge, spend, and public claims.

## Default shape for a new automation

1. Capture the current manual flow in 5 to 10 steps.
2. Write the three answers above before building.
3. Build the smallest useful version (skill, bot, or routine).
4. Run one real task with the user in the loop.
5. Patch the skill or prompt from what failed.
6. Only then reduce friction where the quality bar held.

## Friction defaults

- Outbound Slack/email/partner docs: human approve before send.
- Repo changes: cloud agent + PR review, never silent merge.
- Spend / Ramp: explicit approval every time.
- Internal drafts and research: low friction, but keep a critique pass on a schedule.

## Critique cadence

When you run a periodic AI-process critique, score each live automation against these three questions. If any answer is missing or stale, flag it and propose the patch.
