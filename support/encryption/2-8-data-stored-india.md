---
slug: data-stored-india
category: encryption
title: Where is my data stored and is it covered by Indian law?
route: /support/encryption/data-stored-india
status: DRAFT — legal claims pending review
note: >
  Per memory context, legal pages (privacy policy, terms) are still pending Indian legal review
  and unconfirmed business decisions (governing-law jurisdiction scope, DPDP Act 2023 posture).
  This article should not make compliance claims ahead of that review. Written to describe
  architecture factually and defer specific legal-status claims to the reviewed Privacy Policy.
---

# Where is my data stored and is it covered by Indian law?

> ⚠️ **Note on this article's status.** The specific legal claims below (data protection law applicability, jurisdiction) require sign-off from qualified legal review before publishing — this is a known open item, not an oversight. The architecture description (what's stored, where, and in what form) is accurate and can ship independently of the legal review.

## What's stored, and where

Your encrypted photo data is stored using cloud object storage, with account and gallery metadata held in P3's database. The specific storage region should be confirmed here once finalized — this affects which data protection regime applies and shouldn't be asserted without that confirmation.

## What "encrypted" means for this question

Because photo content is end-to-end encrypted before it leaves your device (see [What does "end-to-end encrypted" actually mean for my photos?](./2-1-what-is-e2ee.md)), what's physically stored on P3's servers — regardless of region — is ciphertext that P3 itself cannot read. Account metadata (email, gallery names, billing information) is stored in readable form, since P3 needs it to operate the service.

## Legal and compliance status

P3 is operated by a India-based sole proprietorship. The specific compliance posture under India's Digital Personal Data Protection Act (DPDP) 2023 and IT Rules 2021, along with the governing law for disputes, is being finalized as part of P3's legal page review. This article will be updated with specifics once that review is complete — see the full [Privacy Policy](/privacy) for the authoritative, legally-reviewed statement once published.

## Related articles

- [What does "end-to-end encrypted" actually mean for my photos?](./2-1-what-is-e2ee.md)
- [What can P3 see and what can't it see?](./2-2-what-p3-cannot-see.md)
- [What happens to my photos if P3 is hacked?](./2-5-p3-breach-scenario.md)
