---
title: Why can't P3 reset my password and restore my photos?
published: '2026-06-30'
category: encryption
excerpt: 'Short answer: your account password and your photo decryption key are two completely different
  things, and only one of them can be reset by email.'
author: Vikas Kumbhakar
migration_original_priority: high
migration_note: Likely highest-traffic article at launch per content inventory. Should appear in popular
  articles list and be cross-linked from any forgot-password UI.
---

# Why can't P3 reset my password and restore my photos?

Short answer: your **account password** and your **photo decryption key** are two completely different things, and only one of them can be reset by email.

## What an email reset can do

P3 can reset your account password the normal way — click "forgot password," verify your email, set a new one. This gets you back into your account and dashboard.

## What an email reset cannot do

It cannot restore access to your encrypted galleries. Your photo decryption key isn't generated from your password — it's generated from your recovery phrase, the one shown to you once during key setup. P3 never stores that phrase, on purpose.

So even after a successful password reset, if you don't have your recovery phrase (or a backup password you set up in advance), your galleries will still show as inaccessible. This isn't a separate bug from the password reset working — it's the expected, by-design outcome of the two systems being intentionally kept apart.

## Why P3 built it this way

If P3 *could* email you a way to recover your photo decryption key, that would mean P3 itself holds enough information to decrypt your photos — which would defeat the entire point of end-to-end encryption. A system where "forgot your photos? we'll email you a reset link" works is a system where P3 (or anyone who compromised P3) could read your content. P3 deliberately doesn't have that capability.

## What actually gets you back in

You have two real recovery paths, and they need to have been set up *before* you lose access:

1. **Your recovery phrase** — entered at `/recover`, re-derives your key directly.
2. **A backup password** — if you set one in Settings → Security in advance, it provides a second way back in, independent of the phrase.

If you have neither, your galleries are not recoverable. See the full breakdown in [What are my options if I lose access?](../../articles/recovery/recovery-options-overview.md) — it's worth reading even if you're not currently locked out, so you know what to set up now.

## Related articles

- [What are my options if I lose access?](../../articles/recovery/recovery-options-overview.md)
- [What is a backup password and should I set one?](../../articles/account/backup-password.md)
- [I forgot my account password](../../articles/recovery/forgot-password.md)
- [What happens during key setup?](../../articles/getting-started/key-setup-explained.md)
