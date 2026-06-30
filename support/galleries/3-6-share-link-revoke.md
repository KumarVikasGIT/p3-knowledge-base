---
slug: share-link-revoke
category: galleries
title: Revoking or regenerating a share link
route: /support/galleries/share-link-revoke
status: ready
priority: high
note: Must distinguish "regenerate" from "disable sharing" precisely — they have different effects per canonical spec (isPublic=false is a hard server-side revoke; regenerate only invalidates the old token going forward).
---

# Revoking or regenerating a share link

From the Share panel on a gallery you own, you have two related but different actions: **Regenerate link** and **Disable sharing**. They're not interchangeable, so it's worth understanding what each one actually does.

## Regenerate link

This creates a brand new link and invalidates the old one. Anyone trying to open the *old* link afterward will be denied — it no longer works.

The important nuance: regenerating doesn't reach into the browser of someone who *already opened* the old link. If they already loaded the gallery, their device already has what it needs to decrypt that content locally, and a new link on P3's side doesn't undo that. Regeneration stops *future* access through the old link — it isn't a way to retroactively pull back access from someone who's already viewed the gallery. This is explained in more depth in [Is a share link secure?](../encryption/2-4-share-link-security.md).

Use this when you want to stop sharing with people who *haven't yet* opened the link — for example, you sent it to the wrong group and want to cut that off before anyone opens it, or you simply want a fresh link going forward.

## Disable sharing

This turns the gallery back to Private and immediately stops the server from serving the gallery's content to *any* link request — including the current one. It's a more complete stop than regenerating: the server itself refuses to hand out the encrypted gallery data to link-based requests at all, effective immediately, for everyone.

This still carries the same underlying limitation as above: it doesn't undo decryption for someone who already opened the gallery before you disabled sharing. It controls what the server will serve going forward, not what's already been viewed.

## If you need a harder guarantee

If your concern is specifically that someone who already had access needs to be cut off as completely as P3's architecture allows — not just from future link use — the right tool is gallery key rotation, which re-issues the gallery's encryption key for everyone who should keep access. This is a heavier action than regenerating a link. Contact support if you need this, or see [Removing someone from a gallery](./3-7-remove-collaborator.md), which triggers rotation automatically for named collaborators.

## Related articles

- [Is a share link secure?](../encryption/2-4-share-link-security.md)
- [Removing someone from a gallery](./3-7-remove-collaborator.md)
- [Public vs private galleries — what's the difference?](./3-3-gallery-visibility.md)
