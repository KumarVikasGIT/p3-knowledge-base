---
category: encryption
title: Encryption & Privacy
icon: Lock1
icon_style: Bulk
color_token: --color-accent
route: /support/encryption
order: 2
---

# Encryption & Privacy

How end-to-end encryption works, what P3 can and can't see, and the honest limits of what E2EE protects.

## Articles

1. [What does "end-to-end encrypted" actually mean for my photos?](./2-1-what-is-e2ee.md) — ★ popular
2. [What can P3 see and what can't it see?](./2-2-what-p3-cannot-see.md)
3. [How do encryption keys work in P3?](./2-3-how-keys-work.md)
4. [Is a share link secure?](./2-4-share-link-security.md)
5. [What happens to my photos if P3 is hacked?](./2-5-p3-breach-scenario.md)
6. [What is a key fingerprint and why does P3 show it?](./2-6-tofu-key-trust.md)
7. [Why can't P3 reset my password and restore my photos?](./2-7-no-password-reset-by-email.md)
8. [Where is my data stored and is it covered by Indian law?](./2-8-data-stored-india.md)

## Editorial standard for this category

Every claim in this category is a security claim. Nothing here should say more than the canonical spec actually guarantees. Two load-bearing constraints from `p3_canonical_spec_v1_4` (R6, §1.6) govern several articles:

- **Download-disable and "view-only" sharing are UX hints, not enforced security controls.** Anyone who can view a gallery holds the decryption key and can save the content locally. Articles 2.4 and the cross-linked 3.6 (Galleries & Sharing) must state this plainly, not imply otherwise.
- **Regenerating a share link does not retroactively revoke access already granted.** It stops the *old token* from working, but anyone who already has the Gallery Key (extracted from a previously shared link, or invited as a collaborator) keeps the ability to decrypt that content. True revocation requires key rotation, which is a separate, heavier operation.

These are disclosed in the spec itself as deliberate, acknowledged trade-offs of the E2EE model — not bugs. The knowledge base should disclose them the same way: clearly, without alarm, and without erasing the nuance to make P3 sound simpler than it is.
