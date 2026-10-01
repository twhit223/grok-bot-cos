# Nightly next-day meeting prep

**When it fires:** Every night: preview tomorrow's meetings, schedule end+10min notes checks, and draft night-before 1:1 agendas.

## Job text

Nightly next-day meeting prep for the user (their timezone). Runs every night because tomorrow's meetings need scheduled note checks and 1:1 agendas for review.

1. List the user's calendar for TOMORROW (local date). Skip all-day, focus time, OOO, working location, and events they declined. Keep accepted/tentative/needsAction meetings they are on. Slack huddles may not appear on calendar — do not invent huddle checks at night unless calendar shows them.

2. Message a short "Tomorrow's meetings" list: time (local), title, and that a notes check is scheduled for 10 minutes after each end. Stay quiet only if tomorrow has zero meetings AND zero 1:1 agendas to draft.

3. For each meeting, create a ONE-SHOT routine that fires at meeting end + 10 minutes local. Name it like "Notes check: <meeting title> <date>". After it runs, DELETE that one-shot.

   Notes-check intent: apply Open Items Cleanup judgment (FYI / informing someone is NOT an Open Item update). Use Open Items location from memory. Resolve people names against Slack / memory before writing (never copy auto-notes misspellings). Find notes from Meet/Gemini in Drive/Gmail or Slack huddle AI notes. Reconcile before adding: close decided items, update only when the gate actually changed, add only genuine new user actions as verb-titled rows. Team-visible work goes to Linear, not duplicate Open Items. Message a summary with Added / Updated / Closed buckets. Delete the one-shot either way.

4. Skip duplicate one-shots; clean up leftover past-fire one-shots.

5. Night-before 1:1 agendas: run 1:1 meeting prep night-before delivery for every tomorrow meeting that is a clear 1:1. Draft shareable all-bullets agendas, message the user in chat, and post drafts only to their Slack self-DM. NEVER message the counterpart. If tomorrow has no 1:1s, skip quietly.

6. On recurring auth failures: pause this nightly routine and tell the user what to reconnect.
