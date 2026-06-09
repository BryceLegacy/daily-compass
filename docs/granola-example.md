# Granola Example

This repo uses Granola MCP as the example meeting-note source.

Daily Compass does not require Granola. The important pattern is:

1. A recurring meeting configuration.
2. A way to search recent meeting notes.
3. A way to read relevant notes.
4. A source trail in the output.

When adapting this to Granola or another note taker:

- keep credentials out of the repo.
- avoid committing raw exports.
- preserve private citations only in private outputs.
- use mock notes in public examples.

## Codex + Granola MCP

In Codex, connect your Granola MCP/connector first. Daily Compass should query recent notes by configured meeting title, date, and keywords.

Use safe defaults:

- prefer summaries over transcript text.
- preserve private citations only in private output.
- fall back to local notes when the connector is unavailable.
- do not copy raw meeting content into public examples.
