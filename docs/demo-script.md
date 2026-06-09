# Demo Script

## Short Version

Daily Compass helps you maintain focus and direction every morning with a brief drawn from recent meetings, notes, and context.

I use Granola for meeting notes and Codex Automations to run the workflow around 6:00 a.m. Codex built the recurring automation around my daily flow: read the newest local brief first, check recent meeting notes, prioritize my recurring 10:00 a.m. team meeting, and give me a short brief before the day starts.

The pattern is provider-neutral. You can bring any meeting-note source your agent can read, including an MCP connector, markdown exports, or local notes.

The workflow is simple: define the meetings that matter, point the agent at recent notes and optional local context, then generate a brief with what to remember, what appears to be happening next, personal follow-ups, risks, and a source trail.

## Walkthrough

1. Start with the sample configuration.
2. Run the prompt against only the mock files.
3. Review the generated Daily Compass brief.
4. Copy the example config into a private local note.
5. Add your recurring meetings.
6. Connect your meeting-note source.
7. Optionally add a local daily brief folder or context packs.
8. Turn it into a Codex Automation that runs around 6:00 a.m., or run it manually.

## Why It Is Useful

Recurring meetings create a continuity problem. The important context is scattered across yesterday's notes, meeting summaries, action items, and personal reminders.

Daily Compass gives the agent enough structure to prepare a useful brief without pretending to know more than the sources support.

The automation is the key value: once configured, the brief shows up as part of the morning routine instead of becoming another manual task.

## Privacy Point

The public repo uses mock data only. Real meeting notes, transcripts, private paths, client names, and credentials should stay out of public repos and public examples.
