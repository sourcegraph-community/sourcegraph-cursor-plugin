---
name: searching-sourcegraph
description: Use when the user needs to search or navigate code with Sourcegraph MCP tools.
---

# Searching Sourcegraph

You have access to Sourcegraph search and code navigation tools through MCP.

## Tools

- `nls_search({ query })`: semantic search for natural-language exploration.
- `keyword_search({ query })`: keyword or regex search using Sourcegraph query syntax.
- `read_file({ repo, path, startLine?, endLine?, revision? })`: fetch file contents.
- `list_repos({ query, limit?, after?, before? })`: discover relevant repositories.
- `list_files({ repo, path?, revision? })`: list files and directories.
- `go_to_definition({ repo, path, symbol, revision? })`: locate symbol definitions.
- `find_references({ repo, path, symbol, revision? })`: find symbol usage.
- `commit_search({ repos, messageTerms?, authors?, contentTerms?, files?, after?, before? })`: search commit history.
- `diff_search({ pattern, repos, added?, removed?, author?, after?, before? })`: search code diffs.
- `compare_revisions({ repo, base, head, first?, after? })`: compare two revisions.
- `get_contributor_repos({ author, limit?, minCommits? })`: discover contributor activity by repo.
- `deepsearch({ question })`: run Sourcegraph Deep Search for complex, multi-step questions.
- `deepsearch_read({ identifier })`: read a Deep Search conversation by URL or token.

## Workflow

1. Start with a constrained search (`repo:`, `file:`, `lang:`, `type:` when possible).
2. If results are broad, add constraints and rerun.
3. Read promising files with `read_file` to confirm behavior.
4. Iterate queries based on findings.

Prefer `nls_search` for exploration and `keyword_search` for precision.

## Query Tips

- Use `repo:^github\\.com/org/repo$` for exact repository matching.
- Use `file:\\.(go|ts|py)$` to constrain by extension.
- Use `type:symbol` for definitions and `type:file` for content matches.
