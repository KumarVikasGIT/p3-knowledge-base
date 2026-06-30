---
title: Behaviour when P3 is open in multiple tabs
published: '2026-06-30'
category: troubleshooting
excerpt: P3 is designed to stay consistent if you have it open in several browser tabs at once — most
  of the time, you shouldn't need to think about this at all.
author: Vikas Kumbhakar
migration_note: Corrected from the original content plan's "Web Locks, leader election" framing. The actual
  mechanism per p3_web_architecture.docx is a BroadcastChannel event bus (p3_events) that synchronizes
  login, logout, token refresh, gallery key rotation, and access revocation across all open tabs.
---

# Behaviour when P3 is open in multiple tabs

P3 is designed to stay consistent if you have it open in several browser tabs at once — most of the time, you shouldn't need to think about this at all.

## What stays in sync automatically

- **Logging out** in one tab logs you out in every other open tab immediately, rather than leaving them in a stale logged-in state.
- **Logging in** in one tab updates your other open tabs without requiring them to be reloaded.
- **Removing a collaborator or having your own access revoked** updates instantly across tabs — if you're viewing a gallery in one tab and someone removes your access in another (or from a different device entirely), that tab reflects the change right away rather than continuing to show outdated content.
- **Completing onboarding** in one tab updates other open tabs so they recognize your account as fully set up without needing a manual refresh.

## When you might need to refresh

Most synchronization happens automatically, but if you notice a tab seems to be showing outdated information after a significant change — particularly after being away from that tab for a while — a simple refresh is always a safe way to bring it fully current.

## If tabs seem out of sync and a refresh doesn't fix it

This would be unusual. Try closing and reopening the affected tab entirely rather than just refreshing. If the issue persists, contact support — see [How to contact P3 support](./contact-support.md).

## Related articles

- [I see a warning that someone's key has changed — what do I do?](../galleries/key-change-warning.md)
- ["Something went wrong loading your session"](./bootstrap-error.md)
