# Meeting Notes MCP Setup

Daily Compass expects a meeting-notes source that can answer questions like:

- What meetings happened recently?
- Which notes match these meeting titles or keywords?
- What action items, decisions, and open questions were captured?
- Can source links or note identifiers be preserved?

The connector can be:

- a meeting-notes MCP server
- exported markdown files
- a local API wrapper
- another agent-readable notes source

## Minimum Useful Capabilities

- Search notes by title, date, and keyword.
- Read note summaries or transcript-derived notes.
- Return enough source information for a source trail.

## Safe Defaults

- Prefer summaries over raw transcripts.
- Avoid long direct quotes.
- Do not paste sensitive meeting content into public prompts, examples, issues, or docs.

