---
title: Inviting someone to a gallery
published: '2026-06-30'
category: getting-started
excerpt: From an open gallery, use the invite option to add someone by email. They'll receive an invite
  link.
author: Vikas Kumbhakar
---

# Inviting someone to a gallery

From an open gallery, use the invite option to add someone by email. They'll receive an invite link.

## The part that's easy to miss

**You need to be online and active when they accept the invite.**

This isn't a bug — it's a deliberate consequence of how P3's zero-knowledge model works. Granting someone access means securely sharing the gallery's encryption key with them, and that handoff has to happen directly between two active devices. P3's server is never able to see or handle that key itself, so it can't relay it on your behalf while you're offline.

P3 sends a reminder after 48 hours if the invite hasn't been completed, to help reduce the chance you both miss the window.

## If an invite seems stuck

The most common reason is simply that the inviting account wasn't online when the invitee tried to accept. Try:

1. Confirm the inviter is logged in and active in P3 (a browser tab open is enough).
2. Ask the invitee to refresh and try accepting again.
3. If it's been more than 48 hours, send a fresh invite.

If a gallery you were invited to still isn't showing up after that, see [A gallery I was invited to isn't showing up](../troubleshooting/8-7-gallery-not-visible.md).

## Access levels

When you invite someone, you'll choose what they can do — see [Gallery access levels: Viewer, Uploader, Manager](../galleries/3-4-invite-access-levels.md) for what each level permits.

## Related articles

- [Gallery access levels: Viewer, Uploader, Manager](../galleries/3-4-invite-access-levels.md)
- [A gallery I was invited to isn't showing up](../troubleshooting/8-7-gallery-not-visible.md)
- [Removing someone from a gallery](../galleries/3-7-remove-collaborator.md)
