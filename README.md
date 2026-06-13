# ファーブル昆虫記 Bugs 図鑑

A public field guide for recurring review bugs, public evidence, and agent
operations.

This repository turns repeated review failures into reusable patterns. It is
for teams that want pull-request closeout, review replies, and agent handoffs
to become safer and easier over time.

## Three-Line Model

```text
bug atlas      = public recurrence patterns and reusable runbooks
field log      = private observation notes kept outside this public repo
consumer repo  = any project that copies or adapts these patterns
```

## What Belongs Here

- Generic recurrence classes.
- Public-safe review and closeout templates.
- GitHub review-readback recipes with placeholders.
- Redaction and public-evidence guidance.
- Sanitized examples that work without a specific repository.

## What Does Not Belong Here

- Private incident notes.
- Credential-shaped values or secrets.
- Local machine paths, raw environment values, or raw logs.
- Private repository links.
- Repo-specific commands as mandatory steps.

## Start Here

1. Choose a recurrence class in
   [`taxonomy/review-bug-classes.md`](taxonomy/review-bug-classes.md).
2. Follow [`runbooks/bug-triage.md`](runbooks/bug-triage.md) when a review bug
   appears.
3. Use [`runbooks/review-readback.md`](runbooks/review-readback.md) before
   merge or closeout.
4. Check public text with [`runbooks/public-evidence.md`](runbooks/public-evidence.md).
5. Copy a compact reply from [`templates/`](templates/).

## Where To Write Things

| Material | Put it here? | Where it should go |
| --- | --- | --- |
| Generic prevention pattern | Yes | taxonomy or runbook |
| Generic fix-comment wording | Yes | templates |
| Public GitHub readback recipe | Yes | examples or runbooks |
| Repo-specific validation command | Usually no | consumer repo docs |
| Private incident timeline | No | private field log |
| Raw failed command log | No | private investigation note, after redaction |
| Local path or environment value | No | do not store |

## Adoption

Use this repo by copying small pieces, not by making a consuming project depend
on it at runtime. Start with the templates, then add only the runbooks that fit
your repository's review flow. See [`docs/adoption.md`](docs/adoption.md).

## Public Safety

Before opening an issue or PR here, remove local paths, private repository
links, raw environment values, and credential-shaped strings. See
[`docs/redaction.md`](docs/redaction.md).

## License

This project is licensed under the MIT License. See [`LICENSE`](LICENSE).
