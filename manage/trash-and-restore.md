---
title: "Trash and Restore"
canonical: "https://dokki.one/pub/docs/trash-and-restore"
source_url: "https://dokki.one/pub/docs/trash-and-restore"
updated_at: "2026-07-10T04:49:53.665+00:00"
generated_by: Dokki
---

# Trash and Restore

Deleting a resource moves it to workspace Trash first. Trash is for recovery from accidental deletion; it is not a long-term archive. Visual guide Collaboration Governance Map Retention window Workspa

Canonical source: [https://dokki.one/pub/docs/trash-and-restore](https://dokki.one/pub/docs/trash-and-restore)

Deleting a resource moves it to workspace Trash first. Trash is for recovery from accidental deletion; it is not a long-term archive.

## Visual guide

[Collaboration Governance Map](../reference/visual-library/collaboration-governance-map.md)

## Retention window

Workspace trash keeps deleted resource roots for 30 days. Each trash item shows when it was deleted and when it expires. A background purge can permanently remove expired trash.

## Trash roots and descendants

Dokki lists only the root resource that was explicitly deleted. If you delete a folder, its descendants move with it, but the trash list shows the folder root instead of every child. Restore the root to bring the subtree back.

## Who can see trashed items

Trash is workspace-scoped. Private trashed resources stay hidden from other members unless they are the creator, a workspace admin, or otherwise have explicit access.

## Who can restore

The creator of the trashed root or a workspace admin can restore it. Descendants cannot be restored directly; Dokki returns an error and asks you to restore the root instead.

## Emptying trash

Workspace admins can empty the trash. Emptying trash permanently deletes every trash root and its content through the permanent delete path. This action is destructive and should be treated as final.

## Archive versus trash

Archiving a workspace makes the workspace inert without deleting every resource. Trash is for deleted resources inside a workspace. Use archive for an inactive project; use trash when a resource was removed and may need recovery.

---

Published from Dokki.
