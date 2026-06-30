---
title: Photos are loading slowly or not at all
published: '2026-06-30'
category: troubleshooting
excerpt: This is usually one of a few distinct issues, depending on whether it's slow or fully stuck.
author: Vikas Kumbhakar
---

# Photos are loading slowly or not at all

This is usually one of a few distinct issues, depending on whether it's slow or fully stuck.

## Slow loading

The first time you open a gallery on a given device, P3 has to download and decrypt each photo locally — there's no way around this first pass, since decryption only happens on your device, never on P3's servers. After that first load, P3 caches the decrypted images locally, so reopening the same gallery later is typically much faster. A large gallery (hundreds of photos) will understandably take longer on first open, especially on a slower connection.

## Stuck or not loading at all

If photos aren't loading even after waiting, check:

- **Your connection.** A dropped connection mid-load will show as stalled rather than failed outright in some cases.
- **Whether you're seeing a specific error**, like a broken-image icon rather than just a blank space — if so, see [Photos show a decryption error or broken image](./8-3-decryption-error.md), which is a more specific issue with its own fix.
- **Whether the gallery is mid-rotation** — see [Removing someone from a gallery](../galleries/3-7-remove-collaborator.md) for why this temporarily affects a gallery.

## If only some photos are slow

This is normal for large galleries — P3 prioritizes loading what's visible on your screen first rather than the entire gallery at once, so scrolling further down can trigger new loading for photos that haven't been reached yet.

## If nothing helps

Try refreshing the page first. If the issue persists across multiple galleries or sessions, contact support — see [How to contact P3 support](./8-12-contact-support.md).

## Related articles

- [Photos show a decryption error or broken image](./8-3-decryption-error.md)
- [What works when I'm offline?](./8-10-offline-behaviour.md)
- [Browser storage is full — what do I do?](./8-11-storage-quota-error.md)
