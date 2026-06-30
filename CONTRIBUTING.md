# Contributing to P3 Support

Thanks for wanting to improve P3's documentation or help content. This guide covers how content in this repo works and how to suggest a change.

## What you can contribute

- Corrections or clarifications to existing docs and help articles
- New help articles for situations not yet covered
- Bug reports and feature requests (use the [issue templates](.github/ISSUE_TEMPLATE/) for these — see the main [README](./README.md))

## Before you start

Read through `docs/` and `articles/` to get a feel for the tone: plain language, no unexplained jargon, honest about limitations rather than overselling. P3's content is written so a non-technical user can follow it, even in the more technical `docs/` section.

## Content structure

This repo has two content trees:

- **`docs/`** — Technical documentation. How things work, written for people who want the fuller picture.
- **`articles/`** — Help articles. Task-oriented, step-by-step, written for someone trying to get something done right now.

Each category folder (e.g. `docs/encryption/`, `articles/billing/`) contains a `_category.md` file with the category's metadata — don't create a new category without one.

## Frontmatter

Every content file needs this frontmatter at the top:

```yaml
---
title: "How gallery encryption works"
published: 2026-06-19
category: "encryption"
excerpt: "Optional one-line summary."
tags: ["encryption", "security"]
---
```

`title`, `published`, and `category` are required. `category` must match the `slug` field of an existing `_category.md` in the same tree — not the category's display label.

Files missing required frontmatter fields are silently skipped by the site build, so double-check this before opening a PR.

## How to propose a change

1. Fork this repository
2. Make your change in `docs/` or `articles/` following the structure above
3. Open a pull request with a brief description of what changed and why
4. A maintainer will review — for substantial content changes, this may take a few days

For small fixes (typos, broken links), feel free to use GitHub's "Edit this file" button directly from any page on [help.p3.app](https://help.p3.app) — every doc and article page has an "Edit this page" link that takes you straight to the file on GitHub.

## What we won't accept

- Content that describes P3 features or behavior we haven't actually shipped
- Anything containing personal data, credentials, or internal implementation details not already documented here
- Changes to the security or encryption explanations without maintainer review — these need to stay precisely accurate

## Questions

Not sure if something belongs here, or want to discuss an idea before writing it up? Open a [Discussion](../../discussions) or a [Support Request](.github/ISSUE_TEMPLATE/support_request.md) issue first.
