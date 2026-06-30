---
title: Browser storage is full — what do I do?
published: '2026-06-30'
category: troubleshooting
excerpt: This is a different thing from your P3 plan's storage limit — this is about space your browser
  has set aside on your specific device for caching P3's locally decrypted photos, separate from anything...
author: Vikas Kumbhakar
migration_note: Distinct from plan storage (billing/account categories) — this is the browser's own local
  cache quota on the device, unrelated to your P3 plan limit.
---

# Browser storage is full — what do I do?

This is a different thing from your P3 plan's storage limit — this is about space your browser has set aside on your specific device for caching P3's locally decrypted photos, separate from anything related to your account or subscription.

## What's actually happening

To make galleries load quickly on repeat visits, P3 caches decrypted photos locally in your browser. Browsers cap how much any single site can store this way, and if you're a heavy user with many large galleries viewed on one device, you can occasionally bump into that local cap.

## P3's own protection against this

P3 monitors this in the background and manages older cached content automatically — when local space gets tight, less recently viewed full-resolution images are cleared first (smaller thumbnails are kept longer, since they take up much less room) to free up room without you needing to do anything. You'll typically only see a warning if this automatic management isn't keeping up with how much you're actively browsing.

## If you see a warning anyway

- **Close unused tabs**, especially other browser tabs with large amounts of cached data from other sites, which compete for the same local storage budget.
- **Clear your browser's site data for P3 specifically** (not your whole browser history) — this is safe and doesn't affect your account or your photos on P3's servers, since everything important lives there, not in your browser cache. You'll just need to re-download and re-decrypt galleries the next time you view them.

## What this doesn't affect

This has no impact on your actual photos or your P3 account — everything is safely stored on P3's servers in encrypted form regardless of what's cached locally on any one device. Clearing local cache, even entirely, is always safe to do.

## Related articles

- [I'm seeing a storage warning — what do I do?](../account/5-8-storage-warning.md)
- [Photos are loading slowly or not at all](./8-4-photos-not-loading.md)
