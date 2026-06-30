---
title: What can P3 see and what can't it see?
published: '2026-06-30'
category: encryption
excerpt: 'This is the clearest way to think about it: P3 can see the shape of your activity, but never
  the content of your photos.'
author: Vikas Kumbhakar
---

# What can P3 see and what can't it see?

This is the clearest way to think about it: P3 can see the *shape* of your activity, but never the *content* of your photos.

## What P3 cannot see, under any circumstances

- The actual image content of your photos
- The contents of any photo, at any resolution, including thumbnails
- Your encryption key — it's derived from your recovery phrase on your device and never transmitted to P3 in usable form

This isn't a policy choice P3 could quietly reverse — it's how the system is built. P3's servers receive and store encrypted bytes. There is no key on the server side that could unlock them.

## What P3 can see

- Account information: your email, username, account type
- Gallery metadata: gallery names, how many photos are in a gallery, when it was created, when photos were uploaded
- Storage usage: how much encrypted data you've stored, for plan limit enforcement
- Who you've invited to a gallery and what access level they have
- Billing and subscription information

This metadata is necessary for the app to function — showing you your gallery list, enforcing storage limits, sending you invite notifications. None of it requires reading photo content.

## Why this split exists

A fully "zero-knowledge" system that hid even gallery names or photo counts from the server would make basic features — like showing you a dashboard, or warning you when you're near a storage limit — effectively impossible to build. P3 draws the line at content: anything P3 needs to know to operate the service is visible; anything that constitutes the actual private content you're sharing is not.

## Related articles

- [What does "end-to-end encrypted" actually mean for my photos?](./what-is-e2ee.md)
- [Where is my data stored and is it covered by Indian law?](./data-stored-india.md)
- [What happens to my photos if P3 is hacked?](./p3-breach-scenario.md)
