---
title: Can my client re-share the gallery?
published: '2026-06-30'
category: delivery
excerpt: By default, no — your client can view and (if you've allowed it) download a gallery, but they
  cannot generate their own share link to pass along to others. This is controlled by a re-sharing...
author: Vikas Kumbhakar
migration_note: 'Important: canShare=false IS enforced and revokes tokens the client already generated
  — unlike the general share-link revocation case in encryption/2-4 and galleries/3-6. This is a genuine
  exception, not an inconsistency, and should be presented as such.'
---

# Can my client re-share the gallery?

By default, no — your client can view and (if you've allowed it) download a gallery, but they cannot generate their own share link to pass along to others. This is controlled by a re-sharing permission you set per gallery assignment, off by default.

## Turning re-sharing on

If you enable it, your client gains the ability to create their own share link from the gallery, which they can then send to anyone — this only works if the gallery itself is also set to link-only visibility (see [Public vs private galleries](../galleries/gallery-visibility.md)).

This is useful in some delivery scenarios — for example, a couple wanting to pass their wedding gallery to family members directly — but it's worth thinking through before turning on, since once your client shares that link further, the same disclosure in [Is a share link secure?](../../docs/encryption/share-link-security.md) applies: anyone who opens it gains real access on their own device.

## One thing that works differently here

Unlike general share-link revocation, **turning re-sharing off again is genuinely effective going forward, including for links your client already created.** If you disable this permission after your client has already generated their own share link, that link stops working immediately — this is enforced server-side specifically for client-generated links, not just a UX hint.

The one limitation that still applies: this doesn't undo access for anyone who already opened the link before you turned re-sharing off. It stops new and continued access through that link; it can't reach into a device that's already decrypted the gallery.

## Related articles

- [Is a share link secure?](../../docs/encryption/share-link-security.md)
- [Controlling what a client can download](./client-download-controls.md)
- [Revoking a client's access to a gallery](./revoke-client-access.md)
