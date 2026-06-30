---
title: Controlling what a client can download
published: '2026-06-30'
category: delivery
excerpt: When you assign a gallery to a client, you'll set whether they're allowed to download full-resolution
  photos. This is per gallery assignment, so the same client can have downloads enabled on one...
author: Vikas Kumbhakar
migration_note: Must stay consistent with the disclosure already made in encryption/2-4 and galleries/3-6
  — download toggle is a UX control, not an enforced restriction in the E2EE sense.
---

# Controlling what a client can download

When you assign a gallery to a client, you'll set whether they're allowed to download full-resolution photos. This is per gallery assignment, so the same client can have downloads enabled on one gallery and disabled on another.

You can change this setting anytime from the client's profile — toggling it takes effect immediately for that gallery.

## What this controls

With downloads off, your client's gallery view simply won't show a download option — they can view and favourite photos, but the interface won't offer a way to save full files locally.

## What's worth understanding honestly

This is an interface-level control, similar to download settings on a guest share link (see [Is a share link secure?](../encryption/2-4-share-link-security.md)). Anyone viewing a gallery — your client included — has already received the decryption key needed to view it on their device, which is what makes viewing possible without P3's servers reading the content. Turning off the download button removes the convenient in-app way to save files, but it isn't a technical barrier against someone determined to save what's already visible on their screen, the same way it isn't on any platform once content is rendered to a viewer.

In practice, this setting works well for its intended purpose: discouraging casual downloading before a client has paid for or selected their final images, which is the typical reason photographers use it.

## Related articles

- [Is a share link secure?](../encryption/2-4-share-link-security.md)
- [Can my client re-share the gallery?](./4-5-client-share-permission.md)
- [What does my client see when they open the link?](./4-6-guest-view-experience.md)
