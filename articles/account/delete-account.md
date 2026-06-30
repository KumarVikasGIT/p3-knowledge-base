---
title: Deleting your account
published: '2026-06-30'
category: account
excerpt: From Settings → Account, the danger zone at the bottom will include a Delete account option.
  You'll be asked to type an exact confirmation phrase before the deletion proceeds — this is a deliberate...
author: Vikas Kumbhakar
migration_original_status: FORWARD-LOOKING — describes a planned flow (Rework H), not yet live in MVP
migration_original_priority: high
migration_note: 'Per resolved spec conflict (see category README): this article documents the Rework H
  design from p3_backend_rework_v2.md (status PENDING sign-off at time of writing) — phrase confirmation,
  no OTP, 30-day soft-delete recovery window. As of writing, p3_settings_spec.md confirms NO endpoint
  exists yet; the in-app button currently routes to support instead of performing deletion. This article
  should be held back from publishing, or published with a clear "coming soon" framing, until Rework H
  actually ships. Support should treat deletion requests as manual/support-handled until then.'
---

# Deleting your account

> ⚠️ **Status note:** This describes how account deletion is designed to work once it ships. As of now, the in-app delete option routes you to contact support directly rather than completing deletion automatically — see the note at the bottom of this article for what to do today.

From **Settings → Account**, the danger zone at the bottom will include a **Delete account** option. You'll be asked to type an exact confirmation phrase before the deletion proceeds — this is a deliberate extra step, since the action is close to permanent.

## What deleting your account does

- Permanently deletes every gallery you own, along with their photos and encrypted data
- Cancels any active subscription
- Removes your stored backup password, if you'd set one
- Notifies your collaborators that galleries they had access to are gone

## A 30-day window before it's truly final

Unlike some destructive actions in P3, account deletion is designed with a 30-day recovery window: your account is scheduled for deletion rather than wiped instantly. If you log back in during that window, you'll have the option to cancel the scheduled deletion and keep your account as it was. After 30 days with no action, deletion completes permanently and cannot be reversed.

## This is different from a key reset

It's worth being clear about the distinction, since the two flows sound similar but do very different things. [What is a key reset and what does it permanently delete?](../recovery/key-reset-explained.md) destroys your encryption keys and every gallery you own, but **your P3 account itself survives** — you keep your email, username, and plan, and set up new keys to start fresh. Account deletion, by contrast, removes the account entirely. If you're trying to recover from a lost recovery phrase, you almost always want key reset, not account deletion — deleting your account is a much bigger step than what's needed to simply regain access.

## If you want to delete your account today

This feature isn't available as a fully automated in-app flow yet. Contact support — see [How to contact P3 support](../troubleshooting/contact-support.md) — and a member of the team will help process your deletion request manually in the meantime.

## Related articles

- [What is a key reset and what does it permanently delete?](../recovery/key-reset-explained.md)
- [How to contact P3 support](../troubleshooting/contact-support.md)
- [Deleting a gallery](../galleries/delete-gallery.md)
