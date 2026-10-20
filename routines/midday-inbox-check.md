# Midday inbox check

**When it fires:** Weekday ~11:00 AM local: reconcile email and Slack since the morning brief, refresh Open Items, and message only if something changed.

## Job text

Run the **Inbox reconcile** from Open Items Cleanup for the window since today's morning daily focus brief (email, Slack, and work finished in chat with the user since then).

Apply board updates before messaging:

- **Close** Open Items that are done, subsumed by work already sent, or answered by someone else (reason + link in Notes).
- **Flip** Waiting rows when the named gate replied (user's next action or Done).
- **Add** Open Items for new asks that need the user's action (Source = message link). Skip when ownership is unclear — ask first.
- Skip FYI-only traffic and automated mail.

If **Closed**, **New asks**, or **Updated** are all empty, stay quiet (no chat message).

Otherwise send one terse chat message with three short lists: **Closed** (reason each), **New asks** (who, what, link), **Updated**. Offer drafts for replies the user owes; never send on their behalf.

Stay quiet only if Open Items/email/Slack are unreachable and you already reported that auth failure on the last run (then pause this routine).
