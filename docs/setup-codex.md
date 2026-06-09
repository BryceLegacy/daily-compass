# Codex Setup

Daily Compass is designed around Codex Automations. The reference workflow is:

1. Codex runs around 6:00 a.m. on weekdays.
2. It uses sample data until private configuration is provided.
3. It reads your private Daily Compass configuration when `daily-compass.local.md` exists.
4. It reads the newest daily or nightly brief first, if configured.
5. It checks recent meeting notes through your configured meeting-note source.
6. It gives you a short morning brief before your recurring 10:00 a.m. team meeting.

The expected setup flow is conversational: ask Codex to create the automation, then confirm it appears in the Codex Automations tab.

## Create The Automation

In Codex, paste:

```text
Use prompts/create-codex-automation.md to create the Daily Compass Codex Automation.
It should run on sample data until I configure private notes or a private Daily Compass configuration.
```

Codex should create a recurring automation named `Daily Compass`. After creation, verify it appears in the Codex Automations tab.

## Sample Mode First

The automation should use sample data until configured otherwise:

- `daily-compass.config.example.md`
- `prompts/daily-compass.md`
- `samples/daily-briefs/`
- `samples/meeting-notes/`
- `samples/context-packs/`
- `samples/people/contacts.example.yaml`

Only after the sample run works should you add private note paths, private context, or a real meeting-note connector.

## Automation Checklist

Before creating a Codex Automation, confirm:

- your private `daily-compass.local.md` uses your correct time zone.
- morning delivery time is set to 6:00 a.m. or another time that works for you.
- the schedule runs before the recurring 10:00 a.m. team meeting or whichever meeting you configure.
- recurring meetings are configured.
- meeting notes access works.
- private notes live outside the public repo.
- the privacy checklist has been reviewed.

## Suggested Codex Automation Setup

Schedule:

```text
Weekday mornings at 6:00 a.m. in your configured time zone.
```

No-code setup steps:

1. Ask Codex to create a new Automation using `prompts/create-codex-automation.md`.
2. Set the schedule to weekday mornings at 6:00 a.m. in your configured time zone.
3. Set the workspace to this repo or your private Daily Compass folder.
4. Keep sample mode enabled until private config exists.
5. Run once manually before relying on the recurring schedule.

Prompt:

```text
Run Daily Compass.

Use prompts/daily-compass.md as the operating prompt.
Use my private Daily Compass configuration at daily-compass.local.md.
Read the newest daily or nightly brief first if configured.
Then check recent meeting notes from my configured meeting-notes source.
Prioritize today's recurring meetings and produce a short brief with:

1. today's meeting map
2. what to remember
3. what appears to be happening next
4. my follow-ups
5. risks / watchouts
6. source trail

Do not invent owners, deadlines, decisions, or approvals.
If a source is unavailable, continue with the remaining sources and clearly label the limitation.
```

## Suggested Automation Prompt Source

Use `prompts/daily-compass.md` as the base prompt and fill in the paths and meeting configuration from `daily-compass.local.md`.

For public examples, do not include private filesystem paths, real meeting titles, emails, or transcript text.
