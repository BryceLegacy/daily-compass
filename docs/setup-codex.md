# Codex Setup

Daily Compass can run manually or as a recurring Codex automation.

## Manual First

Start with the sample data. In Codex, ask:

```text
Use prompts/daily-compass.md as the operating prompt.
Use daily-compass.config.example.md as the sample configuration.
Use samples/ as the only source data.
Generate a Daily Compass brief.
```

Verify the sample output before adding private note sources or creating an automation.

## Automation Checklist

Before creating a recurring automation, confirm:

- your private `daily-compass.local.md` uses your correct time zone.
- morning delivery time is when you want the brief delivered.
- recurring meetings are configured.
- meeting notes access works.
- private notes live outside the public repo.
- the privacy checklist has been reviewed.

## Suggested Automation Prompt

Use `prompts/daily-compass.md` as the base prompt and fill in the paths and meeting configuration from `daily-compass.local.md`.

For public examples, do not include private filesystem paths, real meeting titles, emails, or transcript text.
