---
title: Photos won't upload — common causes and fixes
published: '2026-06-30'
category: troubleshooting
excerpt: Start by checking what message you're actually seeing, since the cause and fix are usually specific
  to it.
author: Vikas Kumbhakar
pinned: true
---

# Photos won't upload — common causes and fixes

Start by checking what message you're actually seeing, since the cause and fix are usually specific to it.

## "Storage full" or upload blocked immediately

You've hit your plan's storage limit. Uploads are blocked until you free up space or upgrade. See [How is gallery storage calculated?](../galleries/gallery-storage-usage.md) and [How to upgrade your plan](../billing/upgrade-plan.md).

## Upload starts but stalls or fails partway

Usually a connectivity issue. P3 automatically retries failed uploads several times with increasing delays between attempts before giving up — so a brief network drop often resolves on its own without you doing anything. If it's still stuck after a few minutes, check your connection and try again manually.

## "This file already exists" or it seems to skip silently

This isn't an error — P3 detects when a file has already been uploaded (even across retries) and skips re-uploading it rather than creating a duplicate. If a photo you expected to see is missing, check the gallery; it's likely already there.

## Gallery shows "temporarily read-only"

Uploads are blocked while a gallery is mid-rotation — this happens automatically right after someone is removed from the gallery. It resolves on its own, usually within seconds. See [Removing someone from a gallery](../galleries/remove-collaborator.md) for why this happens.

## Nothing happens at all when you try to upload

Check that you have permission to upload to this gallery — only the Owner and Editors can upload; Viewers cannot. See [Gallery access levels](../galleries/invite-access-levels.md) to confirm your role.

## If none of this matches what you're seeing

See [Some photos uploaded but others didn't](./upload-partial-failure.md) if it's a partial-batch issue specifically, or [How to contact P3 support](./contact-support.md) with details on what you're seeing.

## Related articles

- [Some photos uploaded but others didn't](./upload-partial-failure.md)
- [How is gallery storage calculated?](../galleries/gallery-storage-usage.md)
- [Uploading photos to a gallery](../galleries/upload-photos.md)
