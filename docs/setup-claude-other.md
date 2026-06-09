# Claude / Other Agent Setup

Daily Compass is agent-neutral. If your agent can read local files and call a meeting-notes connector, it can use this template.

## Manual Mode

Paste this into Claude or another agent:

```text
Use prompts/daily-compass.md as the operating prompt.
Use daily-compass.config.example.md as the sample configuration.
Use samples/ as the only source data.
Generate a Daily Compass brief.
```

Codex users should prefer [Codex Setup](setup-codex.md), which creates a recurring automation in the Codex Automations tab.

For your private setup, copy the example config into a private note and update it with your recurring meetings, note source, and optional local knowledge base paths.

## Scheduled Mode

If your agent does not support recurring automations, use its reminders feature or your calendar to run the prompt at your preferred time.

Keep the actual meeting notes local. Do not schedule jobs in hosted CI systems unless you have reviewed the privacy and credential risks.
