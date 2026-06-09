# Setup Worksheet

Use this worksheet before connecting Daily Compass to real notes.

## 1. Choose Your Agent

- Codex
- Claude
- another local or hosted agent

Questions to answer:

- Can the agent read local files?
- Can the agent access your meeting-note source?
- Can it create recurring automations or reminders?
- If not, will you run Daily Compass manually or from a calendar reminder?

Reference setup:

- Codex with a weekday 6:00 a.m. Automation.
- Claude or another agent as a manual or reminder-driven fallback.

## 2. Choose Your Meeting Notes Source

- Granola
- another meeting-notes MCP connector
- markdown exports
- local notes folder
- sample files only

Questions to answer:

- Can notes be searched by date, title, and keyword?
- Can the agent read summaries without exposing full transcripts?
- Can the output include a safe source trail?

## 3. Decide Whether To Use A Local Knowledge Base

A local knowledge base is optional.

Use one if you have:

- daily or nightly briefs
- project context packs
- lightweight people/contact context
- decision logs

Skip it if:

- you only want meeting-note continuity
- your notes are not organized yet
- you are testing with sample files

## 4. Define Recurring Meetings

For each recurring meeting, capture:

- meeting label
- cadence
- usual time
- purpose
- keywords or title patterns
- lookback window
- output focus

Example:

```text
Meeting: Daily Team Sync
Cadence: weekdays
Usual time: 10:00
Purpose: recurring team meeting to coordinate active work, blockers, and follow-ups
Keywords: daily, team sync, coordination
Lookback: 2 business days
Output focus: what changed, open loops, personal follow-ups, risks
```

## 5. Configure Reminders

Common reminders:

- morning Daily Compass brief
- daily or nightly note capture
- afternoon follow-up review

Keep reminders short. They should prompt the workflow, not contain private meeting content.

## 6. Run A Sample First

Paste this into your agent:

```text
Use prompts/daily-compass.md as the operating prompt.
Use daily-compass.config.example.md as the sample configuration.
Use samples/ as the only source data.
Generate a Daily Compass brief.
```

Review the result before connecting private notes.

## 7. Connect Private Context

When the sample works:

1. Copy `daily-compass.config.example.md` to `daily-compass.local.md`.
2. Replace sample meetings with your real recurring meetings.
3. Replace sample paths with private local paths, if using a local knowledge base.
4. Add your meeting-note provider details.
5. Keep `daily-compass.local.md` out of git.
