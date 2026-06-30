---
title: Removing someone from a gallery
published: '2026-06-30'
category: galleries
excerpt: 'From the collaborators panel on a gallery you own, select Remove next to the person you want
  to remove, then confirm. You''ll see a clear warning before confirming: they''ll lose access, and going...'
author: Vikas Kumbhakar
migration_original_priority: high
migration_note: Corrected from the original content plan. Removal is not instantaneous and silent — it
  triggers a mandatory key rotation that makes the entire gallery temporarily read-only for all remaining
  members. See p3_roles_permissions_spec and GALLERY_ROTATION_JOB in p3_backend_architecture_v1_1.
---

# Removing someone from a gallery

From the collaborators panel on a gallery you own, select **Remove** next to the person you want to remove, then confirm. You'll see a clear warning before confirming: they'll lose access, and going forward, photos can't be added or removed from the gallery until the process below finishes.

## What actually happens when you remove someone

Removing a collaborator isn't just deleting them from a list — it triggers **key rotation**, which is how P3 makes the gallery's encryption key unreadable to the person who was removed, going forward. This is a required step, not optional cleanup: it happens automatically every time someone is removed.

While rotation is running, you'll see a banner on the gallery: **"Gallery is temporarily read-only while access is being updated."** During this window:

- Uploading and deleting photos is blocked, for everyone, including you
- Viewing and downloading existing photos continues to work normally for everyone who still has access
- This typically takes just a few seconds for most galleries

Once rotation finishes, the banner disappears and the gallery returns to normal.

## A second removal during rotation

Only one rotation can run on a gallery at a time. If you try to remove another person while a rotation is already in progress, you'll be asked to wait until the current one finishes before starting the next.

## What removal does and doesn't protect

Removal and rotation stop the removed person from being able to fetch the gallery's encryption key again going forward — they can no longer decrypt new content shared after their removal.

What it cannot do: undo access to photos they already downloaded to their own device before being removed. Once someone has decrypted and saved a photo locally, removing them from the gallery doesn't reach into their device and take it back. This is the same underlying limitation described in [Is a share link secure?](../encryption/2-4-share-link-security.md) — it's a structural property of end-to-end encryption, not something specific to how removal was implemented. The removal flow states this plainly before you confirm, rather than implying a guarantee P3 can't make.

## Related articles

- [Is a share link secure?](../encryption/2-4-share-link-security.md)
- [Gallery access levels: Viewer, Editor, Owner](./3-4-invite-access-levels.md)
- [I see a warning that someone's key has changed — what do I do?](./3-10-key-change-warning.md)
