---
title: Photos show a decryption error or broken image
published: '2026-06-30'
category: troubleshooting
excerpt: P3 is built to never silently fail on a photo that won't decrypt — you'll always see a clear
  placeholder rather than a blank gap or a photo that looks corrupted, so this is a visible, intentional...
author: Vikas Kumbhakar
---

# Photos show a decryption error or broken image

P3 is built to never silently fail on a photo that won't decrypt — you'll always see a clear placeholder rather than a blank gap or a photo that looks corrupted, so this is a visible, intentional error state rather than something going unnoticed.

## What P3 already tries automatically

If a photo fails to decrypt, your device's first assumption is that its locally cached copy of the gallery's encryption key might simply be out of date — for example, if someone was recently removed from the gallery, which automatically rotates the key for everyone remaining. P3 automatically fetches a fresh copy of the key and retries once before showing you an error at all. Most cases that look like a decryption problem resolve invisibly at this step, and you'll just see the photo load normally a moment later.

## If the error persists after that retry

A few possible causes:

- **You're mid-rotation.** If a collaborator was just removed from this gallery, the gallery may briefly be read-only while keys finish updating — see [Removing someone from a gallery](../galleries/remove-collaborator.md). This typically resolves within seconds.
- **Your local data is stale or corrupted.** Try refreshing the page. If that doesn't help, logging out and back in restores your key cleanly from your account.
- **You're on a new device or your browser data was cleared**, and recovery hasn't been completed yet — see [Logging in on a new device](../recovery/new-device-login.md).

## What this is not a sign of

A decryption error on its own doesn't mean your photo is lost or corrupted on P3's servers — the encrypted data is almost always intact; it's the local key material on your specific device that's out of sync. This is recoverable in the vast majority of cases.

## If nothing resolves it

Contact support — see [How to contact P3 support](./contact-support.md) — and mention which gallery and roughly when this started, since that helps narrow down the cause quickly.

## Related articles

- [I see a warning that someone's key has changed — what do I do?](../galleries/key-change-warning.md)
- [Removing someone from a gallery](../galleries/remove-collaborator.md)
- [Logging in on a new device](../recovery/new-device-login.md)
