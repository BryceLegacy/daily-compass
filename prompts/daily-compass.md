# Daily Compass Prompt

You are preparing a daily operating brief.

Use the configured recurring meetings to decide what matters today. Do not assume one specific meeting type unless the user's configuration says so.

## Configuration

Use the user's Daily Compass configuration file if one is provided. If none is provided, use `daily-compass.config.example.md` and the sample files.

## Inputs To Use

Use these inputs in order:

1. Read the newest dated daily or nightly brief if configured and available.
2. Identify today's relevant recurring meetings from the configuration.
3. Check optional people/contact/context files only when they clarify ownership, follow-ups, or recurring work.
4. Query the configured meeting-notes source for recent notes related to today's meetings.
5. Prioritize continuity: unresolved decisions, open loops, commitments, risks, and follow-ups.

Meeting notes provider:

- The author uses Granola.
- Users may bring any note taker that exposes notes through an MCP connector or local export.

## Output

Produce:

1. Today's meeting map
2. What to remember
3. What appears to be happening next
4. My follow-ups
5. Risks / watchouts
6. Source trail

## Rules

- Do not invent owners, deadlines, or decisions.
- Separate explicit action items from inferred reminders.
- If the local knowledge base is missing, continue with meeting notes only.
- If meeting notes are unavailable, continue with local notes only and mark the brief as limited.
- Keep the brief readable in under two minutes.
- Avoid raw transcript dumps.
- Include source references, but do not leak private paths, emails, proprietary details, or sensitive meeting content in public examples.

## Copy/Paste Starter

```text
Use this Daily Compass prompt.
Use my Daily Compass configuration below.
If I have not provided private paths or meeting-note access, use only the sample files in this repo.

[Paste or reference Daily Compass configuration here]
```
