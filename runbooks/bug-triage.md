# Bug Triage Runbook

Use this when a reviewer finds a bug or an agent notices repeated failures.

## Steps

1. Read the latest review-thread state, including outdated and unresolved
   status.
2. Classify the bug using `taxonomy/review-bug-classes.md`.
3. Identify the smallest enforcing layer that prevents recurrence.
4. Fix that layer before broad refactors.
5. Add a regression test or guard that would have failed before the fix.
6. Run targeted validation plus the repository's standard validation lane.
7. Scan the PR body, patch, and fix comment for public-evidence safety.
8. Reply to the review thread with a compact summary and validation list.
9. Re-read review-thread state after the reply.
10. Wait for two delayed readbacks before merge or closeout when review bugs
    have been arriving asynchronously.

## Smallest Enforcing Layer

| If the bug is... | Prefer fixing... |
| --- | --- |
| unclear contract | docs and templates |
| clear but unguarded contract | tests or schema |
| accepted malformed input | parser or checker |
| generated artifact drift | freshness check |
| process cleanup or exit handling | runtime wrapper contract |
| public text leak | public-evidence checker or template |

## Closeout Rule

Do not close an issue only because a fix comment was posted. Close only after
the fix is merged, validation evidence is available, and live readback shows no
current unresolved blocker for the closed scope.
