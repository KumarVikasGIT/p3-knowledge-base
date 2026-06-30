---
title: Recovering with a backup password
published: '2026-06-30'
category: recovery
excerpt: If you set up a backup password in advance (see What is a backup password and should I set one?),
  this option appears automatically alongside the recovery phrase option on the recovery screen — you...
author: Vikas Kumbhakar
---

# Recovering with a backup password

If you set up a backup password in advance (see [What is a backup password and should I set one?](../account/5-2-backup-password.md)), this option appears automatically alongside the recovery phrase option on the recovery screen — you don't need to remember where to find it.

## Steps

1. On the recovery screen, choose the backup password option instead of entering a phrase.
2. Enter your backup password.
3. Select **Restore with backup password**. Your device retrieves your encrypted backup from P3, uses your password to decrypt it locally, and compares the result against what's on record for your account.
4. If it matches, your key is restored on this device just as it would be with your recovery phrase.

## If the password is incorrect

You'll see a clear message that the password didn't work, and nothing is changed — try again if you think you mistyped it. Unlike a forgotten account password, there's no email-reset option for a backup password specifically, since P3 never has access to it to reset in the first place.

## If this option doesn't appear

It only shows up if you'd previously set a backup password. If you don't see it, you likely never set one up — see [I lost my recovery phrase and have no backup password](./7-5-lost-mnemonic-no-backup.md) if you're also missing your recovery phrase.

## Related articles

- [What is a backup password and should I set one?](../account/5-2-backup-password.md)
- [What are my options if I lose access?](./7-1-recovery-options-overview.md)
- [Recovering with your recovery phrase](./7-3-recover-with-mnemonic.md)
