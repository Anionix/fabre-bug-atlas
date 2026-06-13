# Token-Efficient Closeout Runbook

The rule is: success compressed, failure expanded.

## Success Path

For successful commands, report only:

- command name,
- exit status,
- checked count or summary,
- compact output metrics when available.

Do not paste full successful logs into review comments.

## Failure Path

For failed commands, expand only:

- failing command,
- relevant error excerpt,
- affected file or review object,
- next fix action.

## Batch Progress

Use compact progress updates:

```text
PRs 10-14: merged
PR 15: waiting for review readback
PR 16: fixing blocker
```

## Closeout Evidence

Keep public closeout text short and link to durable artifacts when possible.
Full logs belong in private investigation notes only when they are safe to
store.
