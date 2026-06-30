---
title: Some photos uploaded but others didn't
published: '2026-06-30'
category: troubleshooting
excerpt: This is common with large batches and isn't usually a sign of a deeper problem — large uploads
  are made up of many individual file uploads, and it's normal for one or two to need a retry while the...
author: Vikas Kumbhakar
---

# Some photos uploaded but others didn't

This is common with large batches and isn't usually a sign of a deeper problem — large uploads are made up of many individual file uploads, and it's normal for one or two to need a retry while the rest succeed.

## What's safe

Any photo marked as done in the upload screen is fully uploaded and safe — it's already in the gallery. You don't need to re-add or worry about those.

## What needs attention

Files marked as failed or interrupted need to be re-added. If your page reloaded or your browser closed mid-upload, P3 will tell you which files were affected when you return — simply drag the same files back in. P3 recognizes files it's already fully received and won't duplicate them, so it's safe to re-add the whole original batch if you're not sure exactly which ones went through.

## Why this happens

The most common causes are a temporary network drop during a large batch, or closing the browser tab before everything finished. P3's upload queue is built to survive both of these — it persists locally and resumes automatically where it can, but a file that was actively transferring at the exact moment of an interruption may need that one manual re-add.

## If it keeps happening repeatedly

If you're seeing this consistently, even on a stable connection, it's worth checking your connection speed against the size of your batch — many large RAW files over a slow connection can occasionally need more retries than usual. If it persists, contact support — see [How to contact P3 support](./contact-support.md).

## Related articles

- [Photos won't upload — common causes and fixes](./upload-fails.md)
- [Uploading photos to a gallery](../galleries/upload-photos.md)
