# Daily Compass

Daily Compass is a local-first template for turning recurring meetings, recent notes, and optional local context into a short daily operating brief.

I use this pattern with Granola and Codex. The template is intentionally provider-neutral: bring any meeting-note tool that can expose notes through an MCP connector, exported markdown, or another local source.

## What It Helps With

- Preparing for recurring meetings
- Remembering unresolved follow-ups
- Carrying continuity across days
- Keeping a source trail for decisions, risks, and reminders
- Using a local knowledge base when one exists, without making it required

## How It Works

1. Read your Daily Compass markdown configuration.
2. Identify today's relevant recurring meetings.
3. Read the newest daily or nightly brief, if configured.
4. Check optional people and context files when useful.
5. Pull recent notes from a meeting-notes MCP server, or use sample/local note files.
6. Produce a short daily brief with a source trail.

## Quickstart With Sample Data

```bash
git clone https://github.com/your-name/daily-compass.git
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

## Configure Your Recurring Meetings

Daily Compass does not assume one specific workflow. During setup, define the meetings that matter to you:

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

If you do not have one, set `knowledge_base.enabled = false` and use meeting notes only.

## Meeting Notes

The author uses Granola. You can use Granola, another note taker, a meeting-notes MCP server, or sanitized markdown exports.

See:

- [Meeting Notes MCP Setup](docs/meeting-notes-mcp.md)
- [Granola Example](docs/granola-example.md)

## Automation

Daily Compass works best as a recurring morning automation, but you can also run it manually.

Configurable fields:

- `profile.timezone`
- `profile.morning_delivery_time`
- `profile.daily_brief_expected_time`
- `recurring_meetings`
- `reminders.nightly_brief`
- `reminders.followups`

For Codex setup, see [Codex Setup](docs/setup-codex.md).

For Claude or another agent, see [Claude / Other Agent Setup](docs/setup-claude-other.md).

## Privacy And Security

Do not publish real meeting notes, raw transcripts, emails, private paths, credentials, client names, or proprietary product details.

Before publishing changes, use the checklist in [Privacy And Security](docs/privacy-security.md).

See [Privacy And Security](docs/privacy-security.md).

## Example Output

See [sanitized example output](examples/output/sanitized-daily-compass-brief.md).

## Project Status

This repo is a public-safe starter template. The current version prioritizes setup, learning, mock data, and safe adaptation over code.
