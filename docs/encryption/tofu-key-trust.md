---
title: What is a key fingerprint and why does P3 show it?
published: '2026-06-30'
category: encryption
excerpt: 'A key fingerprint is a short, unique code derived from someone''s personal encryption key. You
  might see one on a collaborator''s profile or during an invite. It exists to answer one specific question:'
author: Vikas Kumbhakar
---

# What is a key fingerprint and why does P3 show it?

A key fingerprint is a short, unique code derived from someone's personal encryption key. You might see one on a collaborator's profile or during an invite. It exists to answer one specific question: *am I really sharing this gallery with the person I think I am?*

## Why this matters

When you invite someone to a gallery, your device fetches their public key from P3's server to encrypt the gallery key for them. P3 takes real steps to protect this process — but it's still worth understanding the underlying question any encrypted system has to answer: how do you know the key the server gave you actually belongs to the right person, and not something substituted along the way?

P3 handles this in two layers.

## Layer 1 — automatic, always on

The first time your device sees someone's public key, it remembers it. If that key ever changes unexpectedly on a later interaction, your device will show a clear warning rather than silently proceeding. This means any unexpected change is something you'll actually see, not something that happens invisibly.

This protection is automatic — you don't need to do anything to benefit from it. See [I see a warning that someone's key has changed — what do I do?](../galleries/3-10-key-change-warning.md) if you encounter it.

## Layer 2 — optional, for extra assurance

If you want to be certain about someone's identity *before* you've ever interacted with them — what's sometimes called verifying on "first contact" — you can compare key fingerprints out of band. That means checking the fingerprint shown in P3 against the same fingerprint shown on the other person's device, through a separate channel (in person, over a phone call, etc.) rather than trusting it sight unseen within the app.

This step is optional. Most users won't need it for everyday sharing with people they already know. It's most useful for high-stakes situations — for example, a professional photographer confirming a new client's identity before sending a sensitive delivery.

## The honest limit

This system — automatic change-detection plus optional fingerprint verification — is the same general approach used by other major encrypted messaging platforms. It's a strong, well-understood model, but it's worth being clear that no automated check can fully replace a real, independent verification you do yourself for very first contact with someone. P3 surfaces the tools; using the optional layer is up to you.

## Related articles

- [I see a warning that someone's key has changed — what do I do?](../galleries/3-10-key-change-warning.md)
- [How do encryption keys work in P3?](./2-3-how-keys-work.md)
- [Inviting someone to a gallery](../getting-started/1-6-invite-collaborator.md)
