# Configuration Reference

Daily Compass uses a plain-language markdown configuration.

Start from:

```bash
cp daily-compass.config.example.md daily-compass.local.md
```

Or copy the sections into your preferred private notes app.

## profile

- `Role`: brief role description used to shape output.
- `Time zone`: user's local time zone.
- `Morning delivery time`: target time for the daily brief.
- `Daily or nightly brief reminder time`: expected time for the daily note reminder.

## knowledge_base

- whether local context is required.
- daily brief folder.
- people/contact index.
- durable context packs.
- whether the agent should continue without local context.

## meeting_notes

- provider label, such as Granola or another note taker.
- connector type, such as MCP, markdown export, or local notes.
- source location.
- default lookback window.

## recurring_meetings

Each recurring meeting should define:

- label
- cadence
- usual time
- priority
- purpose
- lookback window
- keywords or title patterns
- output focus
