# ファーブル昆虫記 Bugs 図鑑

A generic field guide for review bugs, public evidence, and agent operations.

This repository is the public core. It contains reusable runbooks, templates,
and taxonomy entries that can be applied to any repository with pull requests,
review comments, and local validation evidence.

## What This Is

- A review-bug atlas for recurring PR failure patterns.
- A public-evidence guide for keeping review text safe to publish.
- A compact closeout workflow for successful validation and failed checks.
- A set of templates that agents and humans can copy across repositories.

## What This Is Not

- Not a private incident log.
- Not a credential store.
- Not tied to a specific repository, framework, provider, CI system, or agent.
- Not a replacement for live review-thread readback.

## Start Here

1. Read [`taxonomy/review-bug-classes.md`](taxonomy/review-bug-classes.md).
2. Use [`runbooks/bug-triage.md`](runbooks/bug-triage.md) when a review bug appears.
3. Use [`runbooks/review-readback.md`](runbooks/review-readback.md) before merge or closeout.
4. Use [`runbooks/public-evidence.md`](runbooks/public-evidence.md) before publishing PR bodies or comments.
5. Use [`templates/`](templates/) for compact public-safe replies.

## Public / Private Boundary

Public guidance may name public pull requests, public issues, public commands,
and sanitized recurrence classes. Do not publish local absolute paths,
environment values, credential-shaped strings, private repository links, or raw
internal logs.

Private observations should be stored in a separate private field-log
repository and promoted here only after redaction.
