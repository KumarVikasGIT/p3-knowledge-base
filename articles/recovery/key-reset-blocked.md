---
title: Why is my key reset blocked?
published: '2026-06-30'
category: recovery
excerpt: 'If you''re trying to perform a key reset and it won''t proceed, the most likely reason is that
  one of your galleries is in the middle of a different security process: a key rotation, which happens...'
author: Vikas Kumbhakar
---

# Why is my key reset blocked?

If you're trying to perform a key reset and it won't proceed, the most likely reason is that one of your galleries is in the middle of a different security process: a key rotation, which happens automatically whenever you remove someone from a gallery.

## Why this blocks a reset

Rotation and reset are both processes that touch your encryption keys, and running them at the same time on the same account isn't safe — it could leave a gallery in an inconsistent state. Rather than risk that, P3 simply waits until the in-progress rotation finishes before allowing a reset to start.

## What to do

This isn't something you need to actively fix — it resolves on its own. Gallery rotations are typically quick, usually finishing within seconds to at most a few minutes for very large galleries. Wait a short while and try the key reset again.

If you removed a collaborator from a gallery recently, that's almost certainly the cause — see [Removing someone from a gallery](../galleries/3-7-remove-collaborator.md) for what's happening behind the scenes during that process.

## If it's still blocked after a while

If you've waited and the reset still won't go through, contact support — see [How to contact P3 support](../troubleshooting/8-12-contact-support.md) — since at that point it's worth having someone look at the specific gallery involved.

## Related articles

- [Removing someone from a gallery](../galleries/3-7-remove-collaborator.md)
- [What is a key reset and what does it permanently delete?](./7-6-key-reset-explained.md)
