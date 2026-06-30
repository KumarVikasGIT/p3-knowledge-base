---
slug: p3-breach-scenario
category: encryption
title: What happens to my photos if P3 is hacked?
route: /support/encryption/p3-breach-scenario
status: ready
---

# What happens to my photos if P3 is hacked?

If an attacker gained access to P3's servers or databases, here's the honest breakdown of what they would and wouldn't get.

## What they would get

Encrypted data — the ciphertext form of your photos, plus the metadata described in [What can P3 see and what can't it see?](./2-2-what-p3-cannot-see.md): account emails, gallery names, photo counts, and similar information.

## What they would not get

The actual content of your photos. Because P3's servers never hold your decryption keys, encrypted photo data is meaningless without them — there's no key sitting alongside it on the server that an attacker could also steal to unlock it.

This is the core promise of end-to-end encryption: the server is never a single point of failure for your content, because it never had the ability to read that content in the first place, breach or no breach.

## What this doesn't protect against

It's worth being precise about the boundaries of this protection, rather than letting the claim run further than it should:

- **Your own device security.** If your device itself is compromised — malware, someone with physical access while you're logged in — your photos are exposed the same way they would be on any platform, because at that point they're already decrypted on your screen.
- **Account-level access.** A breach of your P3 account password alone doesn't expose photo content (your password and your decryption key are separate, as covered in [What happens during key setup?](../getting-started/1-4-key-setup-explained.md)), but it could expose account metadata or let someone impersonate you for new actions.
- **Already-shared links.** As explained in [Is a share link secure?](./2-4-share-link-security.md), anyone who already has a valid share link already has the key for that gallery — a server breach doesn't change that, but it also wasn't something a server breach could have caused either.

## Related articles

- [What can P3 see and what can't it see?](./2-2-what-p3-cannot-see.md)
- [Is a share link secure?](./2-4-share-link-security.md)
- [Where is my data stored and is it covered by Indian law?](./2-8-data-stored-india.md)
