---
title: My payment failed — what happens?
published: '2026-06-30'
category: billing
excerpt: If a renewal payment doesn't go through, here's what actually happens — and importantly, what
  doesn't.
author: Vikas Kumbhakar
migration_original_priority: high
migration_note: Must not overstate consequences of a single failed payment. past_due retains full access
  per canonical spec Rule 30 — only exhausted retries (unpaid) change access.
---

# My payment failed — what happens?

If a renewal payment doesn't go through, here's what actually happens — and importantly, what doesn't.

## Right after a failed payment

You'll get an email letting you know the charge didn't succeed, and Razorpay automatically begins retrying the payment over the following days. During this entire retry period, **your account keeps full access to everything on your current plan** — nothing is restricted, paused, or downgraded just because one payment attempt failed. This is deliberate: a single declined card, an expired card you haven't updated yet, or a temporary bank issue shouldn't interrupt your access while there's still a reasonable chance the payment goes through on retry.

## If all retries fail

If every retry attempt is exhausted without a successful charge, your subscription moves to an unpaid state, and at that point your account behaves as if the subscription ended — it follows the same path described in [What happens if I exceed my plan limits?](./6-8-plan-limits-enforcement.md) if you're over the Free plan's limits, since you're effectively back on Free at that point.

## What to do if you get a failed-payment notice

The simplest fix is usually updating your payment method before the retry window runs out — outdated card details are the most common cause. Once a valid payment succeeds, whether through Razorpay's automatic retry or after you've updated your card, your account resumes normally without any further action needed.

## If you keep seeing this and aren't sure why

Reach out to support — see [How to contact P3 support](../troubleshooting/8-12-contact-support.md) — with your account email and we can look into what's happening with the payment specifically.

## Related articles

- [What happens if I exceed my plan limits?](./6-8-plan-limits-enforcement.md)
- [How to upgrade your plan](./6-2-upgrade-plan.md)
- [How do I get an invoice or receipt?](./6-7-invoice-receipt.md)
