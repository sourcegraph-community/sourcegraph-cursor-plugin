# sourcegraph-cursor-plugin

Sourcegraph plugin for Cursor that adds:

- Sourcegraph MCP server connectivity
- Reusable Sourcegraph-focused commands
- A `searching-sourcegraph` skill for agent workflows


## Structure

```text
.
├── .cursor-plugin/plugin.json
├── .mcp.json
├── commands/
│   ├── sourcegraph-deepsearch.md
│   └── sourcegraph-search.md
├── skills/
│   └── searching-sourcegraph/
│       └── SKILL.md
└── README.md
```

## Install In Cursor

1. In Cursor, open plugin installation from Git repository.
2. Use this repository URL.
3. Set environment variables used by `.mcp.json`:
   - `SOURCEGRAPH_ENDPOINT` (for example `https://sourcegraph.com`)

The plugin exposes a Sourcegraph MCP server named `sourcegraph`.

## Configuration Notes

- `SOURCEGRAPH_ENDPOINT` should not include a trailing slash.
- MCP endpoint is `${SOURCEGRAPH_ENDPOINT}/.api/mcp`.
- MCP transport type is `http`.
- This matches Sourcegraph's official Cursor MCP integration docs: `https://sourcegraph.com/docs/api/mcp`.

## Included Commands

- `/sourcegraph-deepsearch` to run Sourcegraph search workflows
- `/sourcegraph-search` to fetch a file and summarize it

## Included Skill

- `searching-sourcegraph` for disciplined Sourcegraph search and navigation workflows
