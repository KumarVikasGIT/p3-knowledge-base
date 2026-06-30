---
slug: upload-photos
category: galleries
title: Uploading photos to a gallery
route: /support/galleries/upload-photos
status: ready
---

# Uploading photos to a gallery

From an open gallery, use the upload screen to add photos. You can drag and drop files or select them manually. Supported formats: JPEG, PNG, HEIC, and RAW.

## What happens during upload

Each photo goes through a few stages, shown per-file: Queued → Preparing → Encrypting → Uploading → Done. The encryption step happens entirely on your device — your photo is scrambled into ciphertext before any of it reaches P3's servers. This is why uploads can take a little longer than on platforms without this step, especially for large batches or slower connections.

Before the upload starts, you'll see an estimate of the total size against your remaining storage, so you're not surprised partway through a large batch.

## If your connection drops or the page reloads

If a page reload interrupts an upload, P3 will tell you which files were affected. Files that finished are marked done and are safe. Files that were interrupted need to be re-added — drag the same files back in and they'll resume from there, without duplicating anything that already completed.

## If storage runs out mid-batch

If you hit your storage limit during an upload, the remaining queued files are cancelled and you'll see a clear "storage full" message with options to free up space or upgrade your plan. Files that already finished uploading before the limit was hit stay safe.

## If you're offline

Uploads pause automatically and resume once you're back online — nothing is lost, the queue just waits.

## If individual files fail

See [Photos won't upload — common causes and fixes](../troubleshooting/8-1-upload-fails.md) and [Some photos uploaded but others didn't](../troubleshooting/8-2-upload-partial-failure.md) for troubleshooting steps.

## Related articles

- [How is gallery storage calculated?](./3-9-gallery-storage-usage.md)
- [What can I do on the free plan?](../getting-started/1-7-free-plan-limits.md)
- [Photos won't upload — common causes and fixes](../troubleshooting/8-1-upload-fails.md)
