---
title: How to save your recovery phrase safely (and what not to do)
published: '2026-06-30'
category: recovery
excerpt: Your recovery phrase is shown to you exactly once. How you store it after that is entirely up
  to you — P3 has no way to help you recover it later if it's lost, so it's worth taking a moment to do...
author: Vikas Kumbhakar
---

# How to save your recovery phrase safely (and what not to do)

Your recovery phrase is shown to you exactly once. How you store it after that is entirely up to you — P3 has no way to help you recover it later if it's lost, so it's worth taking a moment to do this properly.

## Good options

- **Write it on paper** and keep it somewhere secure — a safe, a locked drawer, somewhere you'd keep other important documents.
- **Store it in a password manager** built for handling secrets, such as 1Password, Bitwarden, or similar. These are designed specifically for this kind of sensitive data.
- **Consider splitting physical copies** across two secure locations if you're especially concerned about a single point of failure, like a house fire or theft — though this is optional and most people don't need to go this far.

## What not to do

- **Don't screenshot it.** Screenshots often sync automatically to cloud photo libraries, which defeats the purpose of keeping it private.
- **Don't email it to yourself.** Email accounts get compromised, and email isn't designed for storing secrets like this.
- **Don't save it in a plain, unencrypted note** that syncs to the cloud (like a default notes app without encryption).
- **Don't store it anywhere your photos themselves are kept** — if your phrase is sitting next to the very thing it's protecting, you've reintroduced the risk encryption is meant to remove.

## A reminder on why this matters

P3 never stores a copy of this phrase, by design — that's what makes the encryption real. It also means you genuinely are the last line of defense for your own galleries. See [What are my options if I lose access?](./recovery-options-overview.md) for what your options look like if this phrase is ever lost.

## Consider a backup password too

A backup password, set up separately in Settings, gives you a second independent way back in — worth doing alongside storing your phrase carefully, not instead of it. See [What is a backup password and should I set one?](../account/backup-password.md).

## Related articles

- [What happens during key setup?](../getting-started/key-setup-explained.md)
- [What is a backup password and should I set one?](../account/backup-password.md)
- [What are my options if I lose access?](./recovery-options-overview.md)
