# Daily Compass Onboarding Prompt

Use this prompt inside Codex when a user says something like:

```text
Help me get started adding this workflow automation.
```

## Goal

Guide the user through setup conversationally. Do not jump straight to asking for private data. Start with a sample automation demo so the user can see how Daily Compass arrives in chat.

## Startup Flow

1. Briefly explain what will happen:
   - you will create a sample Daily Compass demo first.
   - the demo will use only files from this repo.
   - no private meeting notes, transcripts, credentials, or local paths are needed yet.
   - after the demo, you will ask for the details needed to turn the sample into the user's real workflow.

2. Use the real Codex automation builder/tool to create a near-term sample demo automation. Do not merely describe the setup if the automation tool is available.
   - Name: `Daily Compass Demo`
   - Timing: schedule it for the soonest practical time based on the current time and what Codex Automations supports. If Codex requires a minimum lead time, use the earliest allowed time and tell the user.
   - Destination: current chat/thread if supported, so the user can see how the brief arrives.
   - Source data: sample files only.
   - Purpose: deliver one sample Daily Compass brief using `prompts/daily-compass.md`, `daily-compass.config.example.md`, and `samples/`.

   If Codex cannot schedule a near-term demo automation in the current environment, run the sample brief immediately in chat using the sample files, explain the limitation, and still continue the setup interview.

3. Tell the user what you created and where to look:
   - confirm it should appear in the Codex Automations tab.
   - explain that the first output is a sample run.
   - explain that it is intentionally not connected to private notes yet.

4. When the sample demo brief has run, start the setup interview. If Codex cannot automatically continue after the demo delivery, tell the user to reply `continue setup` after they see the sample brief.

## Sample Demo Automation Task

The demo automation should run Daily Compass in sample mode:

```text
Run a Daily Compass sample brief.

Use prompts/daily-compass.md as the operating prompt.
Use daily-compass.config.example.md as the configuration.
Use only files under samples/ as source data.

Clearly label the output as a sample run.

Produce:

1. today's meeting map
2. what to remember
3. what appears to be happening next
4. my follow-ups
5. risks / watchouts
6. source trail

Do not use private notes, private paths, raw transcripts, credentials, or external meeting-note connectors for this sample run.
```

## Setup Interview After Demo

After the sample output is delivered, ask for the minimum details needed to configure the real workflow:

1. Morning delivery time:
   - Default: 6:00 a.m.
   - Ask whether they want to keep that time.

2. Recurring meetings:
   - meeting name
   - cadence
   - usual time
   - purpose
   - keywords/title patterns
   - lookback window
   - what they want the brief to focus on

3. Meeting-note source:
   - Granola MCP
   - another meeting-notes MCP connector
   - markdown exports
   - local notes
   - sample-only for now

4. Optional local context:
   - daily or nightly brief folder
   - people/contact index
   - context packs
   - none for now

5. Reminders:
   - morning Daily Compass brief
   - daily or nightly note reminder
   - follow-up reminder

6. Privacy guardrails:
   - no raw transcript dumps
   - no credentials
   - no private paths in public repos
   - private source citations only in private output

## Real Automation Setup

After the user answers, create or update the recurring `Daily Compass` Codex Automation.

Until the user provides private configuration, keep the recurring automation in sample mode.

When private configuration exists, the recurring automation should:

- use `daily-compass.local.md` if present.
- read the newest configured daily or nightly brief first.
- check configured meeting notes.
- prioritize the user's configured recurring meetings.
- produce the short Daily Compass brief.
- cite sources safely.
- label unavailable sources clearly.

## Communication Style

Keep the user oriented. At each step, say what you are doing and why.

Use short status updates:

- "I'll start with a sample demo so you can see the brief format before connecting private notes."
- "This demo uses only mock files from the repo."
- "Next I'll ask for your meeting schedule and note source so we can turn the sample into your real workflow."
- "I won't ask you to paste raw transcripts or credentials."
