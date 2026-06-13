# Review Bug Classes

Use these classes to make review findings searchable across repositories.

| Class | Meaning | Typical enforcing layer |
| --- | --- | --- |
| `artifact-validation-gap` | Generated or checked-in artifacts can drift while validation still passes. | artifact checker, schema test, freshness test |
| `public-evidence-boundary` | PR text, review replies, or validation evidence can leak local or sensitive details. | public-evidence checker, template, runbook |
| `schema-contract-drift` | Code, schema, docs, or examples disagree about the accepted shape or vocabulary. | schema test, parser, docs guard |
| `process-signal-contract` | Wrappers mishandle child exit status, signals, process groups, or cleanup. | process tests, platform gates |
| `docs-overclaim` | Documentation promises behavior that current implementation does not provide. | docs guard, wording review |
| `fixture-pairing-or-baseline` | Candidate and baseline evidence are not compared over the same required pairs. | fixture checker, paired baseline test |
| `review-readback-operations` | Merge or closeout proceeds with incomplete review-thread, pagination, or reply state. | readback runbook, delayed checks |

## Classification Rule

Classify the bug by the smallest layer that should have prevented recurrence,
not by where the reviewer happened to comment.
