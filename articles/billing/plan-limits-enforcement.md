---
title: What happens if I exceed my plan limits?
published: '2026-06-30'
category: billing
excerpt: P3 is built so that exceeding a limit — whether from active use, a lapsed subscription, or a
  downgrade — never results in sudden, surprising data loss. There's a long, clearly communicated runway...
author: Vikas Kumbhakar
migration_original_priority: high
migration_note: Timeline sourced precisely from p3_canonical_spec_v1_2_final accountStatus state machine
  (active -> over_limit -> grace -> suspended). Numbers (6 months, 30 days) and the "what is never auto-deleted"
  list are load-bearing -- do not round or simplify them, since this is the article most likely to be
  read by an anxious user.
---

# What happens if I exceed my plan limits?

P3 is built so that exceeding a limit — whether from active use, a lapsed subscription, or a downgrade — never results in sudden, surprising data loss. There's a long, clearly communicated runway before anything is actually at risk. Here's the full timeline.

## Stage 1 — Over your limit

This happens immediately when your storage or gallery count exceeds your plan's allowance. New uploads are blocked, and new galleries can't be created if doing so would push you further over. Everything else keeps working as normal: you can view, download, and share existing galleries, and any active client deliveries continue without interruption. You'll get a monthly reminder email during this stage.

This stage lasts up to **6 months** before anything more serious happens.

## Stage 2 — Grace period

If you're still over your limit after 6 months, your account moves into a 30-day grace period. At this point access becomes fully read-only — no uploads, no new galleries, no new client assignments — but everything you already have remains fully accessible. You'll get weekly reminder emails during this window, with a final, unmistakable warning on the last day before the grace period ends.

## Stage 3 — Suspension (only after both stages above)

Only if the grace period also passes without resolution does P3 begin removing content — and even then, it's done deliberately: your oldest galleries are removed first, one at a time, only until your account is back within your current plan's limits. This step is permanent and irreversible once it happens, and P3's email warnings make this unmistakably clear before it does.

## What's never automatically deleted, at any stage

- Galleries that fall within your plan's limit, even after a downgrade
- Your client profiles and their records
- Your P3 account itself

## The bottom line

From the moment you first go over a limit to the point where anything could actually be removed is measured in months, not days, and you'll receive multiple clear warnings throughout — including one final, explicit warning before the last stage begins. If you've recently gone over a limit, there's no need to panic; you have real time to either free up space or upgrade your plan.

## What to do

- [Upgrade your plan](./6-2-upgrade-plan.md) for more storage and galleries
- Delete galleries or photos you no longer need (see [Deleting a gallery](../galleries/3-8-delete-gallery.md))
- If your subscription lapsed and you want to reactivate, see [How to upgrade your plan](./6-2-upgrade-plan.md)

## Related articles

- [I'm seeing a storage warning — what do I do?](../account/5-8-storage-warning.md)
- [My payment failed — what happens?](./6-4-payment-failed.md)
- [How to upgrade your plan](./6-2-upgrade-plan.md)
