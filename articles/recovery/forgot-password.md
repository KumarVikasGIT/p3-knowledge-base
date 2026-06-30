---
title: I forgot my account password
published: '2026-06-30'
category: recovery
excerpt: From the login screen, select Forgot password? and enter your account email. You'll receive a
  reset link by email — follow it to set a new password.
author: Vikas Kumbhakar
---

# I forgot my account password

From the login screen, select **Forgot password?** and enter your account email. You'll receive a reset link by email — follow it to set a new password.

## What this does and doesn't fix

This restores your ability to log in. It does not, on its own, restore access to your encrypted photos — your password and your photo decryption key are entirely separate systems by design. See [Why can't P3 reset my password and restore my photos?](../../docs/encryption/no-password-reset-by-email.md) if that distinction isn't clear yet.

## After resetting your password

Once you're logged in again, P3 checks whether this device already has your decryption key stored locally:

- **If it does** (you're on the same device you normally use, and your browser data wasn't cleared), your galleries should appear normally — nothing further needed.
- **If it doesn't** (new device, reinstalled app, or cleared browser storage), you'll be guided to a recovery screen to restore your key using your recovery phrase or backup password. See [What are my options if I lose access?](./recovery-options-overview.md) for that next step.

## Related articles

- [What are my options if I lose access?](./recovery-options-overview.md)
- [Why can't P3 reset my password and restore my photos?](../../docs/encryption/no-password-reset-by-email.md)
- [Logging in on a new device](./new-device-login.md)
