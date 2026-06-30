---
title: Changing your account password
published: '2026-06-30'
category: account
excerpt: From Settings → Security, select Send reset email. P3 will email you a link to set a new password.
author: Vikas Kumbhakar
migration_note: Resolved per spec conflict — MVP uses email-based reset only, no in-session change-password
  form. See category README.
---

# Changing your account password

From **Settings → Security**, select **Send reset email**. P3 will email you a link to set a new password.

This works a little differently from changing a password while logged into many other apps — instead of entering your current and new password directly on the settings page, P3 sends you through the same reset flow you'd use if you'd forgotten your password entirely. Follow the link in the email, and you'll be prompted to set your new password there.

## Why this works the way it does right now

A fully in-session "enter current password, set new password" form is planned but isn't part of the current flow — until it ships, the email-based reset is the supported path, and it works reliably even though it takes an extra step.

## A reminder on what this does and doesn't affect

Changing your account password only affects how you log in — it has no effect on your photo decryption key, which is derived separately from your recovery phrase. See [Why can't P3 reset my password and restore my photos?](../../docs/encryption/no-password-reset-by-email.md) if that distinction isn't clear, since it's a common point of confusion.

## Related articles

- [I forgot my account password](../recovery/forgot-password.md)
- [Why can't P3 reset my password and restore my photos?](../../docs/encryption/no-password-reset-by-email.md)
- [What is a backup password and should I set one?](./backup-password.md)
