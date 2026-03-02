---
name: sg-search
description: Search Sourcegraph using natural language or keyword queries.
---

# Sourcegraph Search

Run a Sourcegraph search for the user input.

If the input is natural language, use `nls_search` first.
If the input appears to be a Sourcegraph query, keyword search, or regex pattern, use `keyword_search`.

After searching:

1. Summarize the most relevant matches.
2. Include repositories and files for top results.
3. Suggest 1 to 3 refined follow-up queries when results are broad.

Use any text provided after `/sg-search` as the search query.
