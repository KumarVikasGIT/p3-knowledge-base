---
title: What happens during key setup?
published: '2026-06-30'
category: getting-started
excerpt: This is the most important screen in onboarding, so it's worth explaining plainly — without the
  cryptography jargon.
author: Vikas Kumbhakar
migration_original_priority: high
---

# What happens during key setup?

This is the most important screen in onboarding, so it's worth explaining plainly — without the cryptography jargon.

## What you'll see

During key setup, P3 generates a unique **recovery phrase** for your account — a sequence of ordinary words. This phrase is what makes your photos yours and only yours.

P3 uses this phrase to mathematically generate your personal encryption key. And here's the important part: **P3 never stores the phrase itself.** It's shown to you exactly once, on this screen, and then it's gone from P3's systems entirely.

## Why P3 can't just email you a new one

This isn't an oversight — it's what makes the encryption real.

A system that could reset your phrase for you on demand would also be a system that could be compelled, hacked, or tricked into accessing your photos. By never storing it, P3 removes that possibility entirely. The trade-off is that **you** become the only safeguard for your own phrase.

If you lose this phrase and haven't set a backup password, there is no "forgot phrase" email reset. See [What are my options if I lose access?](../recovery/7-1-recovery-options-overview.md) for the full picture of what's recoverable and what isn't.

## Before you continue

Write the phrase down somewhere safe. Specifically:

- Don't screenshot it
- Don't email it to yourself
- Don't save it in a plain note synced to the cloud
- Do write it on paper, or store it in a password manager built for secrets

See [How to save your recovery phrase safely](../recovery/7-8-save-mnemonic-safely.md) for detailed guidance.

## Consider a backup password too

P3 offers an optional **backup password** as a secondary recovery path, independent of the phrase. It's not required, but it's worth setting up — see [What is a backup password and should I set one?](../account/5-2-backup-password.md)

## Related articles

- [What are my options if I lose access?](../recovery/7-1-recovery-options-overview.md)
- [How to save your recovery phrase safely](../recovery/7-8-save-mnemonic-safely.md)
- [What is a backup password and should I set one?](../account/5-2-backup-password.md)
- [How do encryption keys work in P3?](../encryption/2-3-how-keys-work.md)
