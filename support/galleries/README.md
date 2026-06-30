---
category: galleries
title: Galleries & Sharing
icon: GalleryAdd
icon_style: Bulk
color_token: --color-accent
route: /support/galleries
order: 3
---

# Galleries & Sharing

Creating galleries, managing access levels, sharing with collaborators, and understanding what happens when access changes.

## Articles

1. [How to create a gallery](./3-1-create-gallery.md)
2. [Uploading photos to a gallery](./3-2-upload-photos.md)
3. [Public vs private galleries — what's the difference?](./3-3-gallery-visibility.md)
4. [Gallery access levels: Viewer, Editor, Owner](./3-4-invite-access-levels.md)
5. [Creating and sharing a gallery link](./3-5-share-link-create.md)
6. [Revoking or regenerating a share link](./3-6-share-link-revoke.md)
7. [Removing someone from a gallery](./3-7-remove-collaborator.md)
8. [Deleting a gallery](./3-8-delete-gallery.md)
9. [How is gallery storage calculated?](./3-9-gallery-storage-usage.md)
10. [I see a warning that someone's key has changed — what do I do?](./3-10-key-change-warning.md)

## Correction from the original content plan

The initial article outline for 3.7 (removing a collaborator) assumed access ends immediately once removed, full stop. Checking against `p3_roles_permissions_spec` and `p3_backend_architecture_v1_1` (GALLERY_ROTATION_JOB) surfaced a more involved and more accurate mechanism:

- Removing a collaborator triggers a **mandatory key rotation** — no exceptions.
- The gallery becomes **fully read-only** (uploads and deletes blocked, HTTP 423) for the **entire gallery**, for **all remaining members**, while rotation runs. View and download continue working for everyone who still has access.
- Only **one rotation can run per gallery at a time** — a second revocation attempted mid-rotation is rejected (409) until the first completes.
- Rotation re-wraps the gallery key for remaining members going forward. It does not and cannot reach photos the removed person already downloaded to their own device before removal — consistent with the same E2EE limitation already disclosed in the Encryption & Privacy category (download/revocation as UX hints, not retroactive enforcement).

Article 3.7 reflects this corrected, more complete picture rather than the simpler original framing. Also note: gallery **deletion** (3.8) and account **key reset** use two different confirmation patterns from the canonical spec — deletion requires typing the gallery name, key reset requires the exact phrase `delete my galleries`. These should not be conflated in copy or screenshots.
