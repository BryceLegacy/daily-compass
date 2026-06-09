# Create Daily Compass Codex Automation

Use this prompt inside Codex to create the recurring Daily Compass automation.

```text
Create a Codex Automation named Daily Compass.

Use this repository or workspace as the automation context.

Schedule it for weekday mornings at 6:00 a.m. in my local time zone.

The automation should run Daily Compass using:

- prompts/daily-compass.md as the operating prompt
- daily-compass.local.md if it exists
- otherwise daily-compass.config.example.md
- sample files under samples/ until I configure private paths or a private meeting-note source

The automation should prepare a short morning brief before the configured recurring team meeting. The sample configuration uses a recurring 10:00 a.m. Daily Team Sync.

The automation output should include:

1. today's meeting map
2. what to remember
3. what appears to be happening next
4. my follow-ups
5. risks / watchouts
6. source trail

Do not invent owners, deadlines, decisions, or approvals.
If real meeting notes or private local context are not configured, use only the sample files and clearly label the output as a sample run.
Do not write private notes, transcripts, credentials, or raw meeting content into this public repo.
```

After Codex creates it, confirm it appears in the Codex Automations tab.

