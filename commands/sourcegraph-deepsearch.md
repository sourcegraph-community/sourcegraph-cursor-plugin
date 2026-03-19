---
name: sourcegraph-deepsearch
description: Run Sourcegraph Deep Search for the user question, then read and summarize the deep search result.
---

# Sourcegraph Deep Search

Use Sourcegraph Deep Search when the user asks "how/why" questions or needs cross-file/system understanding.

## Command behavior

1. Start a deep search for the user prompt using `deepsearch`.
2. Read the deep search response using `deepsearch_read`.
3. Identify key files, functions, and call paths mentioned.
4. Summarize findings in plain language with actionable follow-up steps.
5. If needed, read key files for precision before final response.
