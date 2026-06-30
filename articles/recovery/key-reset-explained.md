---
title: What is a key reset and what does it permanently delete?
published: '2026-06-30'
category: recovery
excerpt: A key reset is the way back into P3 when you've lost your recovery phrase and have no backup
  password. It's a significant, irreversible action — worth understanding fully before you start.
author: Vikas Kumbhakar
migration_original_priority: high
migration_note: Reflects resolved category conflict — phrase confirmation only, no OTP step, per p3_frontend_spec_brief.md
  and Decision D3.
---

# What is a key reset and what does it permanently delete?

A key reset is the way back into P3 when you've lost your recovery phrase and have no backup password. It's a significant, irreversible action — worth understanding fully before you start.

## What it is, in plain terms

A key reset generates a completely new recovery phrase and a fresh encryption key for your account, replacing the old one entirely. Because the old key is what protected your existing galleries, and that key is gone for good, those galleries go with it. This is the fundamental trade-off: getting back into P3 with a working key means leaving behind what the old key protected.

## What you'll see before it happens

You'll be shown a clear list of exactly what's about to be destroyed — every gallery you own, by name, with its photo count — along with a note that any collaborators on those galleries will also lose access. There's no way to miss this warning; it's shown explicitly before you can proceed.

To confirm, you'll need to type an exact phrase rather than just clicking a button — this is a deliberate extra step, since something this permanent shouldn't be triggerable by accident.

## What's permanently deleted

- Every gallery you own, along with all its photos
- Access for every collaborator and client on those galleries
- Your existing backup password, if you had one set (it was tied to the old key)

## What survives

- Your P3 account itself — email, username, account type, plan
- Galleries where you're a collaborator, not the owner (though you'll need to be re-invited to actually access them again, since the old key that could decrypt them is gone)
- Your client profiles, if you're on a Professional account — these are CRM records and aren't tied to your encryption key

## After the reset

You'll go through key setup again, just like when you first created your account — a brand new recovery phrase is generated, and this time, it's worth taking [How to save your recovery phrase safely](./save-mnemonic-safely.md) seriously from the start.

## This is not the same as deleting your account

A key reset destroys your galleries but keeps your P3 account intact. Deleting your account entirely is a different, separate action — see [Deleting your account](../account/delete-account.md) if that's actually what you're looking for, which is a bigger step than most people in this situation need.

## Related articles

- [I lost my recovery phrase and have no backup password](./lost-mnemonic-no-backup.md)
- [Why is my key reset blocked?](./key-reset-blocked.md)
- [Deleting your account](../account/delete-account.md)
