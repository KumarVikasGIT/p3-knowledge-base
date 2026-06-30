---
title: I see a warning that someone's key has changed — what do I do?
published: '2026-06-30'
category: galleries
excerpt: This warning appears when P3 notices that a collaborator's encryption key is different from the
  one your device remembered from before. It's a security feature working as intended, not an error —
  P3...
author: Vikas Kumbhakar
---

# I see a warning that someone's key has changed — what do I do?

This warning appears when P3 notices that a collaborator's encryption key is different from the one your device remembered from before. It's a security feature working as intended, not an error — P3 deliberately blocks the action and shows you this rather than silently proceeding, so it's worth pausing here rather than dismissing it.

## Why this happens — the harmless reason

By far the most common cause is that the person genuinely reset their own keys — for example, because they lost their recovery phrase and had to start fresh (see [What is a key reset and what does it permanently delete?](../recovery/7-6-key-reset-explained.md)). A legitimate reset is recorded by P3's servers, but your device still flags it for your awareness, because it can't fully distinguish a deliberate reset from a more concerning scenario on its own.

## Why this matters — the scenario it protects against

In rarer, more serious cases, an unexpected key change could indicate someone is attempting to intercept a share by substituting their own key in place of the real recipient's. This is exactly the kind of silent, hard-to-detect issue this warning is designed to surface. See [What is a key fingerprint and why does P3 show it?](../encryption/2-6-tofu-key-trust.md) for the fuller explanation of why this check exists.

## What to do

1. **If you're expecting it** — for example, you know the person recently had to reset their account — it's reasonable to proceed.
2. **If you're not sure**, reach out to the person directly, outside of P3 (a text, a call, in person), and confirm with them that they did reset their keys.
3. **If you can't confirm it**, don't proceed. You can remove them from the gallery instead — see [Removing someone from a gallery](./3-7-remove-collaborator.md) — and re-invite them once you've verified what happened.

There's no urgency to act the moment you see this — it's safe to pause and verify before deciding.

## Related articles

- [What is a key fingerprint and why does P3 show it?](../encryption/2-6-tofu-key-trust.md)
- [What is a key reset and what does it permanently delete?](../recovery/7-6-key-reset-explained.md)
- [Removing someone from a gallery](./3-7-remove-collaborator.md)
