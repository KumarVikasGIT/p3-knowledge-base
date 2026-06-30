---
title: How do encryption keys work in P3?
published: '2026-06-30'
category: encryption
excerpt: There are three things involved, and they each play a different role. No cryptography background
  needed to follow this — just the plain-language version of what each one does.
author: Vikas Kumbhakar
---

# How do encryption keys work in P3?

There are three things involved, and they each play a different role. No cryptography background needed to follow this — just the plain-language version of what each one does.

## Your recovery phrase

A sequence of ordinary words shown to you once, during key setup. This is the root of everything else — every key you have is generated from this phrase. P3 never stores it. See [What happens during key setup?](../getting-started/1-4-key-setup-explained.md) for the full explanation of why.

## Your personal key

From your recovery phrase, your device mathematically generates a personal key pair — one private half that stays only on your device(s) (re-derivable any time from your phrase), and one public half that P3's server does store, because other people need it to share galleries with you.

Think of the public half like a mailbox address: people use it to send things to you, but it doesn't let anyone open your mail. Only your private half — derived from your phrase — can do that.

## The gallery key

Each gallery has its own unique key, generated when the gallery is created. This is the key that actually encrypts and decrypts the photos inside that gallery.

When you invite someone to a gallery, P3 doesn't send them the gallery key directly — it wraps (encrypts) the gallery key using their personal public key, so only they can unwrap it with their own private key. This wrapped copy is what gets stored, one per invited person, per gallery.

## Putting it together

1. Your recovery phrase generates your personal key pair, once, during setup.
2. Each gallery gets its own gallery key when it's created.
3. Inviting someone wraps a copy of that gallery key specifically for them, using their public key.
4. Only people with a valid wrapped copy — unwrapped using their own private key, derived from their own phrase — can decrypt that gallery's photos.

This is why losing your recovery phrase is serious: it's the one piece that regenerates your private key. Without it, there's no way to unwrap any gallery key meant for you. See [What are my options if I lose access?](../recovery/7-1-recovery-options-overview.md)

## Related articles

- [What happens during key setup?](../getting-started/1-4-key-setup-explained.md)
- [What is a key fingerprint and why does P3 show it?](./2-6-tofu-key-trust.md)
- [What are my options if I lose access?](../recovery/7-1-recovery-options-overview.md)
