# Adoption Guide

Use this atlas as a copy-and-adapt source, not as a runtime dependency.

## Recommended Path

1. Copy the fix-comment and PR closeout templates.
2. Pick the recurrence classes that match your review flow.
3. Add a local public-evidence rule in your consumer repository.
4. Add a review-readback checklist to your merge process.
5. Keep private field notes outside the public consumer repository.

## Consumer Repo Boundary

The consumer repository should be self-contained. If a lesson from this atlas
becomes important to a consumer repository, copy the exact sanitized text into
that repository through normal review. Do not rely on a mutable external page
as closeout evidence.

## Minimal Files To Copy

- `templates/fix-comment.md`
- `templates/pr-closeout.md`
- `runbooks/public-evidence.md`
- `runbooks/review-readback.md`
- `taxonomy/review-bug-classes.md`

## Optional Files

- `templates/merge-stack-readback.md`
- `templates/issue-closeout.md`
- `runbooks/token-efficient-closeout.md`
- `examples/github-review-thread-readback.md`
