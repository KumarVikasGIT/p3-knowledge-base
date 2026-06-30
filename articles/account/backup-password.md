---
title: What is a backup password and should I set one?
published: '2026-06-30'
category: account
excerpt: Your recovery phrase is the primary way to regain access to your photos if you ever lose your
  device or clear your browser data. A backup password is a second, independent way to do the same thing
  —...
author: Vikas Kumbhakar
---

# What is a backup password and should I set one?

Your recovery phrase is the primary way to regain access to your photos if you ever lose your device or clear your browser data. A backup password is a second, independent way to do the same thing — recommended, though not required.

## Why have a second option

The recovery phrase is powerful precisely because P3 never stores it — but that also means if you lose the phrase itself, there's no fallback within P3 to retrieve it. A backup password gives you a second path that doesn't depend on still having that phrase written down somewhere.

## How it works, in plain terms

When you set a backup password, your device uses it to encrypt your decryption key and sends that *encrypted* copy to P3 for safekeeping. P3 stores the encrypted version — it cannot decrypt it, since the backup password itself is never sent to P3's servers. Only your device, using the password you typed, can turn that stored backup back into a usable key.

This means your backup password needs to be something you'll remember (or store securely, like in a password manager) — if you forget it, the backup is just as inaccessible as if it didn't exist.

## Should you set one?

Yes, generally — it costs you nothing day to day and gives you a real second chance if your recovery phrase is ever lost. The main reason not to is if you're confident in how you've stored your phrase and prefer not to add another password to manage. Either way, it's optional and can be set up anytime from Settings, not just during onboarding.

## How to set it up

See [How to set or change your backup password](./set-backup-password.md).

## Related articles

- [How to set or change your backup password](./set-backup-password.md)
- [What are my options if I lose access?](../recovery/recovery-options-overview.md)
- [Recovering with a backup password](../recovery/recover-with-backup-password.md)
