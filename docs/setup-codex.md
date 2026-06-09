# Codex Setup

Daily Compass is designed around Codex Automations. The reference workflow is:

1. Codex runs around 6:00 a.m. on weekdays.
2. It uses sample data until private configuration is provided.
3. It reads your private Daily Compass configuration when `daily-compass.local.md` exists.
4. It reads the newest daily or nightly brief first, if configured.
5. It checks recent meeting notes through your configured meeting-note source.
6. It gives you a short morning brief before your recurring 10:00 a.m. team meeting.

The expected setup flow is conversational:

1. Ask Codex to start onboarding.
2. Codex creates a near-term sample demo automation using the real automation builder/tool, not just a written checklist.
3. The demo output appears in chat so the user can see what Daily Compass produces.
4. Codex asks for the user's real meeting schedule, meeting-note source, local context, and reminder preferences.
5. Codex creates or updates the recurring `Daily Compass` automation.

## Start Onboarding

In Codex, paste:

```text
Help me get started adding this workflow automation.
Use the onboarding flow in prompts/onboard-daily-compass.md.
```

Codex should first create a sample demo automation named `Daily Compass Demo`. It should use only sample files and should be scheduled for the soonest practical time based on the current time and what Codex Automations supports.

After the demo runs, Codex should start the setup interview and create or update the recurring automation named `Daily Compass`.

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

1. Ask Codex to use `prompts/onboard-daily-compass.md`.
2. Let Codex create a near-term sample demo automation.
3. Review the sample brief when it arrives in chat.
4. Answer the setup questions for your real workflow.
5. Let Codex create or update the recurring `Daily Compass` automation.
6. Keep sample mode enabled until private config exists.

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
