---
title: How to set or change your backup password
published: '2026-06-30'
category: account
excerpt: 'From Settings → Security, find the backup password section. You''ll see one of two states: no
  backup set, or backup set.'
author: Vikas Kumbhakar
---

# How to set or change your backup password

From **Settings → Security**, find the backup password section. You'll see one of two states: **no backup set**, or **backup set**.

## Setting it for the first time

Select **Set backup password**, choose a password, and confirm it. P3 will take a moment to process — you'll see a brief "saving" indicator while your device derives a secure encryption key from your password and uses it to encrypt your decryption key before sending the encrypted result to P3. This processing step happens on your device and is deliberately a little slower than a typical password save, by design — it's part of what makes the backup resistant to being cracked even if someone got hold of it.

## Changing an existing backup password

Select **Change backup password** and go through the same steps with a new password. This fully replaces the old backup.

## Removing your backup password

If you'd rather not have a backup password set, select **Remove backup password**. This deletes the encrypted backup from P3's servers — after removing it, your recovery phrase becomes your only way back in if you lose access, so make sure you're confident in how you've stored it before removing this safety net.

## If you see an error during setup

Occasionally, if your account's encryption key has changed since you opened the settings page (for example, you reset your keys in another tab), you may see an error indicating a mismatch. If this happens, refresh the page and try again — it's a safety check to prevent saving a backup against an outdated key, not a sign of anything wrong with your account.

## Related articles

- [What is a backup password and should I set one?](./backup-password.md)
- [Recovering with a backup password](../recovery/recover-with-backup-password.md)
- [What are my options if I lose access?](../recovery/recovery-options-overview.md)
