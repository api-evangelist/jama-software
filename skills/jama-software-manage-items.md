---
name: manage-items
description: Create, update and delete requirement items in a Jama Connect project.
api: Jama Connect REST API
generated: '2026-10-20'
method: generated
source: openapi/_ae-authored/jama-software-openapi-generated.yml
operations:
- post_items
- patch_items_id
- put_items_id
- delete_items_id
---
1. `post_items` with project, itemType and fields to create an item.
2. `patch_items_id` for a partial update (JSON Patch), or `put_items_id` to replace it.
3. `delete_items_id` removes an item; check your instance's trash/restore behaviour before relying on undo.
No idempotency key is documented: do not blindly retry a POST.
