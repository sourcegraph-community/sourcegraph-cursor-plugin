---
name: sourcegraph-search
description: Run a Sourcegraph search for the user's question using the Sourcegraph MCP tools.
---

# Sourcegraph Search

Use Sourcegraph MCP tools to answer the user's question through direct search.

## Command behavior

1. Parse the question and extract exact symbols, error text, or keywords.
2. Prefer `keyword_search` when exact terms are available.
3. Use `nls_search` for concept-level requests.
4. Scope search with `repo:` and `file:` filters when context is known.
5. Return concise results with likely best matches and next follow-up searches.
