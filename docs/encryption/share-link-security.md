---
title: Is a share link secure?
published: '2026-06-30'
category: encryption
excerpt: 'Yes, with an important nuance worth understanding: a P3 share link is secure against people
  who don''t have the link, but it works differently from a typical "share with view-only access" toggle
  you...'
author: Vikas Kumbhakar
migration_original_priority: high
migration_note: Must not overstate revocation guarantees. See canonical spec R6 — download-disable and
  link revocation are UX hints, not enforced controls.
---

# Is a share link secure?

Yes, with an important nuance worth understanding: a P3 share link is secure against people who don't have the link, but it works differently from a typical "share with view-only access" toggle you might be used to elsewhere.

## How a share link works

A P3 share link contains the gallery's decryption key, embedded directly in the link itself (not visible as plain text — it's in a part of the URL that browsers don't send to any server). This is what lets someone view the gallery without needing a P3 account: their browser uses the key in the link to decrypt the gallery, entirely on their own device.

P3's server never sees this key. It only serves the encrypted gallery data — the actual unlocking happens client-side, using the key from the link.

## What this means for revocation

Here's the part to understand clearly, because it's a genuine trade-off, not a missing feature: **once someone has a share link, P3 cannot remotely "unshare" that specific link.**

If you regenerate your gallery's share link, the *old* link stops working for anyone who hasn't already opened it. But if someone already opened the old link, their device already extracted and can still use the decryption key — regenerating the link doesn't reach into their browser and take that key back.

The same applies to "download disabled" settings: they prevent the *interface* from showing a download button, but anyone who can view a gallery already has the key needed to save it through other means. This is true of any end-to-end encrypted system — once content is decrypted and visible, there's no way to retroactively control what someone does with it.

## What P3 does protect against

- Anyone who has never received the link cannot access the gallery — there's no way to guess or brute-force the key.
- P3's own servers cannot decrypt or view the gallery contents, even under legal compulsion, because they never hold the key.
- Strict security headers prevent the link's key from leaking to third-party scripts, ad trackers, or browser history in normal use.

## What to do if you've shared a link too widely

If you're concerned a link has reached someone you didn't intend, the only real remedy is **gallery key rotation** — generating an entirely new key and re-wrapping access for everyone who should still have it. This is a heavier operation than simply regenerating a link. See [Revoking or regenerating a share link](../galleries/3-6-share-link-revoke.md) for what's currently available, and talk to support if you need a full rotation.

## Related articles

- [Revoking or regenerating a share link](../galleries/3-6-share-link-revoke.md)
- [Can my client re-share the gallery?](../delivery/4-5-client-share-permission.md)
- [What does "end-to-end encrypted" actually mean for my photos?](./2-1-what-is-e2ee.md)
