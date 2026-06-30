---
slug: send-delivery-link
category: delivery
title: Sending a delivery link to a client
route: /support/delivery/send-delivery-link
status: ready
popular: true
---

# Sending a delivery link to a client

From a client's profile, select **Assign gallery**, choose the gallery you want to deliver, and set the permissions for this delivery — whether the client can download photos, and whether they can re-share the gallery themselves. You can change these later.

Once assigned, use **Invite Client** to send the delivery email. It's branded and includes a personalised link to the gallery — your client doesn't need a P3 account to open it, though one will be created automatically behind the scenes once they do.

## Tracking delivery status

On your client's profile, each assigned gallery shows a status badge so you know exactly where things stand:

- **Awaiting registration** — your client hasn't created a P3 account yet. Nothing more to do on your end; this resolves automatically once they do.
- **Setting up access** — they've registered, and P3 is finishing the handoff that grants them their decryption key.
- **Delivered** — full access granted. Your client can open the gallery.

This process is automatic — once your client registers, the rest happens without any further action needed from you.

## A note on timing, like collaborator invites

Similar to inviting a regular collaborator, granting a client's key access requires your account to be active at some point after they register, since P3's zero-knowledge model means the server can't hand over an encryption key on your behalf. In practice this is rarely an issue since the badge states above are designed to make it clear if access is still pending, but if a client tells you they registered and still can't see anything after some time, opening P3 yourself (even just having a tab active) usually resolves it.

## Related articles

- [What does my client see when they open the link?](./4-6-guest-view-experience.md)
- [Controlling what a client can download](./4-4-client-download-controls.md)
- [Inviting someone to a gallery](../getting-started/1-6-invite-collaborator.md)
