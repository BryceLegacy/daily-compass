# Daily Compass Configuration

Copy this file to `daily-compass.local.md` or paste it into Codex, Claude, or another agent. Keep your private version out of public repos.

## Profile

- Role: Product lead
- Time zone: America/Chicago
- Morning delivery time: 08:00
- Daily or nightly brief reminder time: 17:00
- Preferred brief length: readable in under two minutes
- Preferred source style: short source trail, no raw transcript dumps

## Meeting Notes Source

- Provider I use: Granola
- Other supported pattern: any meeting-note tool exposed through MCP, markdown exports, or an agent-readable notes source
- Preferred lookback: 2-3 business days for daily meetings, 7 days for weekly planning
- If meeting notes are unavailable: continue with local notes and clearly mark the brief as limited

## Local Knowledge Base

- Required: no
- Daily briefs folder: `samples/daily-briefs/`
- People/contact index: `samples/people/contacts.example.yaml`
- Context packs folder: `samples/context-packs/`
- If the local knowledge base is unavailable: continue with meeting notes and clearly mark the missing context

For your private setup, replace the sample paths with your own local folders. Do not commit private paths, real notes, transcripts, emails, or credentials.

## Recurring Meetings

### Daily Team Sync

- Cadence: weekdays
- Usual time: 10:00
- Priority: high
- Purpose: coordinate active work, blockers, and follow-ups
- Keywords/title patterns: daily, team sync, coordination
- Lookback: 2 business days
- Output focus: what changed, open loops, personal follow-ups, risks

### Weekly Planning

- Cadence: weekly
- Usual time: Monday 14:00
- Priority: medium
- Purpose: review priorities, decisions, owners, and next milestones
- Keywords/title patterns: planning, priorities, roadmap
- Lookback: 7 days
- Output focus: decisions needed, workstream status, dependencies

## Reminders

- Morning Daily Compass brief: enabled
- Daily or nightly note reminder: enabled
- Follow-up reminder: optional
- Reminder style: short, action-oriented, no raw meeting content

## Privacy Rules

- Prefer summaries over raw transcripts.
- Do not paste private meeting notes into public issues, posts, examples, or docs.
- Cite sources safely.
- Label inferred follow-ups as inferred.
- Do not invent owners, deadlines, approvals, or decisions.
