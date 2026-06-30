---
category: delivery
title: Client Delivery
icon: Briefcase
icon_style: Bulk
color_token: --color-accent
route: /support/delivery
order: 4
gated: FLAG_CLIENT_PORTAL — Professional accounts only, full CRM UI requires Pro plan
---

# Client Delivery

The photographer-to-client workflow: adding clients, delivering galleries, and controlling what clients can do.

## Articles

1. [What is the client delivery feature?](./4-1-what-is-client-delivery.md)
2. [Adding a client to your account](./4-2-add-client.md)
3. [Sending a delivery link to a client](./4-3-send-delivery-link.md) — ★ popular
4. [Controlling what a client can download](./4-4-client-download-controls.md)
5. [Can my client re-share the gallery?](./4-5-client-share-permission.md)
6. [What does my client see when they open the link?](./4-6-guest-view-experience.md)
7. [Revoking a client's access to a gallery](./4-7-revoke-client-access.md)

## Notes on accuracy vs the original content plan

A few clarifications surfaced from `p3_canonical_spec_v1_2_final` and `p3_frontend_page_brief` that the articles below reflect precisely:

- **Two separate "revoke" actions exist** and they do different things. Revoking a client's access to one specific gallery (`DELETE /clients/:id/galleries/:galleryId`) only affects that gallery. Revoking the client profile entirely (`DELETE /clients/:id`) removes access to every assigned gallery at once, but — importantly — does **not** delete the client's own P3 account. Article 4.7 covers both and is explicit about which is which.
- **`canShare` is enforced, unlike general link revocation.** When a photographer turns off a client's share permission, any share link tokens that client already generated are invalidated immediately. This is a genuine exception to the usual "can't pull back something already shared" limitation described in Encryption & Privacy — worth calling out in 4.5 so it doesn't read as inconsistent with that earlier disclosure.
- **Delivery status is a three-state badge** the photographer sees per client per gallery: Awaiting registration → Setting up access → Delivered. This is referenced in 4.3 and 4.6 to set accurate expectations for what a photographer will observe while a client gets set up.
- Full CRM functionality (client list, multi-gallery assignment, status tracking) requires the Pro plan. Free and Personal-plan Professional accounts can still send a basic gallery link to a client, but without the dedicated CRM interface. This boundary is cross-linked to Billing & Plans rather than re-explained here.
