---
name: trace-requirements
description: Find Jama Connect items and walk their upstream and downstream relationships to build a traceability view.
api: Jama Connect REST API
generated: '2026-10-20'
method: generated
source: openapi/_ae-authored/jama-software-openapi-generated.yml
operations:
- get_items
- get_items_id_upstreamrelationships
- get_items_id_downstreamrelationships
- get_relationships
---
1. `get_items` with `project` (and optionally `itemType`) to list items; page with `startAt` / `maxResults` (max 50).
2. For each item, call `get_items_id_upstreamrelationships` and `get_items_id_downstreamrelationships`.
3. Use `get_relationships` to read relationships across a project in bulk.
Auth: HTTP Basic or OAuth 2.0 client credentials (token at https://{tenant}.jamacloud.com/rest/oauth/token). Base URL is per tenant.
Note: the contract is generated from the public docs (rest.jamasoftware.com), not published by Jama.
