---
title: Revoking a client's access to a gallery
published: '2026-06-30'
category: delivery
excerpt: There are two different things you might mean by "revoke," and P3 treats them as separate actions
  — worth knowing which one you actually want before you click.
author: Vikas Kumbhakar
migration_note: 'Corrected from the original content plan, which framed this around "regenerating the
  share token." The actual mechanism is two distinct actions: per-gallery revoke and full client-profile
  revoke. Neither deletes the client''s own P3 account. See p3_canonical_spec_v1_2_final §4.8 (DELETE
  /clients/:id, DELETE /clients/:id/galleries/:galleryId).'
---

# Revoking a client's access to a gallery

There are two different things you might mean by "revoke," and P3 treats them as separate actions — worth knowing which one you actually want before you click.

## Revoking access to one specific gallery

From the client's profile, on the **Galleries** tab, select **Revoke access** next to the gallery in question, then confirm. This removes their access to that one gallery only — any other galleries you've assigned them stay exactly as they were.

## Revoking the client entirely

From the client's profile, select **Revoke client**. This removes their access to *every* gallery you've assigned them, all at once, and marks the client profile itself as revoked.

One thing worth being clear about: **this does not delete your client's own P3 account.** If they registered a P3 account to view your gallery, that account is theirs and continues to exist independently — revoking only removes the specific access you'd granted them to your galleries through this client relationship.

## What revocation actually does

Both actions stop your client from being able to access the affected gallery or galleries going forward through their normal client access. As with other access changes in P3, this works going forward — it can't undo viewing or downloading that already happened before you revoked access. See [Is a share link secure?](../encryption/2-4-share-link-security.md) for the fuller explanation of why that's a structural property of end-to-end encryption rather than a gap specific to client delivery.

If your client had also generated their own share link (because you'd enabled re-sharing), be aware that revoking their direct access doesn't automatically revoke a link they may have already shared further — if re-sharing was on, consider also reviewing [Can my client re-share the gallery?](./4-5-client-share-permission.md) to turn that permission off specifically, which does invalidate their generated links.

## Related articles

- [Can my client re-share the gallery?](./4-5-client-share-permission.md)
- [Is a share link secure?](../encryption/2-4-share-link-security.md)
- [Adding a client to your account](./4-2-add-client.md)
