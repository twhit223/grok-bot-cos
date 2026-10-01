# Chief of Staff (Grok Bot)

A reusable [Grok Bot](https://cursor.com) Chief of Staff setup: goals, Open Items, daily/EoD briefs, Friday wind-down, 1:1 prep, and meeting-notes capture.

Designed by [Dr. Tyler Whittle](https://github.com/twhit223).

## What is in this repo

| Path | Contents |
| --- | --- |
| `skills/` | Portable skill recipes (markdown) you can paste into a Grok Bot |
| `routines/` | Job text for the four core routines |
| `CONVENTIONS.md` | Durable workflow conventions (no personal data) |
| `PLUGINS.md` | Marketplace connectors this bot expects |

## How to use it

### Option A — Bot template (when public)

If the live **Chief of Staff** Grok Bot template is shared publicly, import it from the share link in Grok Bot. That is the fastest path (skills + routines + plugins + getting-started).

> Note (Oct 2026): the share link may still be **team-scoped** for some Cursor teams. If you see "This Bot is managed by a team," ask a team admin to allow public templates, or use Option B.

### Option B — Build from this repo

1. In Grok Bot, create a new bot named **Chief of Staff** (or import a blank assistant).
2. Add marketplace plugins / connectors: Notion, Slack, Google Calendar, Gmail, Google Drive, Linear (see `PLUGINS.md`).
3. For each folder under `skills/`, create a matching skill in the bot and paste the `SKILL.md` body.
4. Create four routines using the prompts in `routines/` (schedules in your timezone):
   - Daily focus brief — weekdays morning (suggest 6:00 local)
   - End of day brief — weekdays late afternoon (suggest 17:30 local)
   - Nightly next-day meeting prep — every night (suggest 20:00 local)
   - Friday weekly wind-down — Friday early afternoon
5. Add the facts from `CONVENTIONS.md` as agent memories (profile-tier for standing rules).
6. Run the **getting-started** skill as your first conversation (or follow its questions manually).

## Privacy

This export is scrubbed for public use: no private company names, people, credentials, or internal links beyond generic placeholders. Customize channel IDs and Open Items locations for your workspace.

## License

MIT — see `LICENSE`.
