# Daily Compass

Daily Compass helps you maintain focus and direction every morning with a brief drawn from recent meetings, notes, and context.

I use this with Granola and **Codex Automations**. Codex runs the workflow every morning, reads the newest local brief first, checks recent meeting notes, and gives me a short morning brief before my recurring meetings start.

The pattern is provider-neutral. Use Granola, another meeting-note tool with an MCP connector, exported markdown, or local notes.

The repo is intentionally no-code. It gives you prompts, sample files, setup questions, and privacy guardrails you can use with Codex, Claude, or another agent.

## What It Helps With

- Start the day with the right context
- Prepare for recurring meetings
- Remember unresolved follow-ups
- Carry continuity across days
- Keep a source trail for decisions, risks, and reminders
- Use a local knowledge base when one exists, without making it required

## How It Works

1. Run on a morning schedule, usually as a Codex Automation.
2. Read your Daily Compass configuration.
3. Find the recurring meetings that matter today.
4. Read the newest daily or nightly brief, if you keep one.
5. Check optional people and context files when useful.
6. Pull recent meeting notes from your meeting-note source.
7. Produce a short brief with follow-ups, watchouts, and a source trail.

## Quickstart With Sample Data

```bash
git clone https://github.com/BryceLegacy/daily-compass.git
cd daily-compass
```

Then use Codex, Claude, or another agent:

```text
Use prompts/daily-compass.md as the operating prompt.
Use daily-compass.config.example.md as the sample configuration.
Use the files under samples/ as mock source data.
Produce a Daily Compass brief using only the sample data.
```

No Python, package install, or CLI setup is required for the basic workflow.

For your private setup, copy `daily-compass.config.example.md` to `daily-compass.local.md`, update it with your meeting names and local paths, and keep that private file out of git.

## First-Run Setup

Use [Setup Worksheet](docs/setup-worksheet.md) before wiring this into real notes. It helps you answer:

- what recurring meetings should be tracked
- whether you have a local knowledge base
- whether you use Granola, another meeting-note MCP connector, or markdown exports
- whether your agent supports recurring automations
- what reminders should be configured

## Configure Your Recurring Meetings

Daily Compass does not assume one specific workflow. Tell it which recurring meetings matter to you:

- meeting name
- cadence
- usual time
- keywords or title patterns
- lookback window
- output focus

Example configuration lives in [daily-compass.config.example.md](daily-compass.config.example.md).

## Optional Local Knowledge Base

A local knowledge base is useful, but not required. If you have one, point Daily Compass at folders for:

- daily or nightly briefs
- lightweight people/contact context
- durable project or operating context

If you do not have one, write `Local knowledge base required: no` in your private configuration and use meeting notes only.

## Meeting Notes

The author uses Granola. You can use Granola, another note taker, a meeting-notes MCP server, or sanitized markdown exports.

See:

- [Meeting Notes MCP Setup](docs/meeting-notes-mcp.md)
- [Granola Example](docs/granola-example.md)

## Automation

Daily Compass works best as a recurring **Codex Automation**. That is the reference workflow for this repo: Codex runs the prompt on a weekday morning schedule and delivers the brief before the first relevant meeting.

You can also run the same prompt manually in Codex, Claude, or another agent.

Configurable fields:

- time zone
- morning delivery time
- daily or nightly brief reminder time
- recurring meetings
- meeting-note source
- local knowledge base usage
- reminders

For Codex setup, see [Codex Setup](docs/setup-codex.md).

For Claude or another agent, see [Claude / Other Agent Setup](docs/setup-claude-other.md).

For setup questions and reminder configuration, see [Setup Worksheet](docs/setup-worksheet.md).

## Privacy And Security

Do not publish real meeting notes, raw transcripts, emails, private paths, credentials, client names, or proprietary product details.

Before publishing changes, use [Privacy And Security](docs/privacy-security.md) and [Public Review Checklist](docs/public-review-checklist.md).

## Example Output

See [sanitized example output](examples/output/sanitized-daily-compass-brief.md).

## Demo Script

See [Demo Script](docs/demo-script.md) for a short explanation you can adapt for a post, video, or walkthrough.

## What This Is Not

Daily Compass is not a meeting-note connector, transcript store, or project management system. It is a public-safe workflow for agents that can already read the notes and files you choose to provide.

## Project Status

This repo is a public-safe starter template. The current version prioritizes setup, learning, mock data, and safe adaptation over code.
