# Contributing

Thanks for improving the atlas.

## Contribution Rules

- Keep guidance generic unless a file is explicitly marked as an example.
- Prefer short runbook changes over long incident narratives.
- Add a recurrence class only when it can help more than one repository.
- Do not include local paths, raw environment values, credentials, or private
  repository links.
- Use placeholders such as `OWNER/REPO`, `NUMBER`, and `<targeted validation>`.

## Good Contributions

- A clearer template.
- A new public-safe checklist.
- A generic review-readback query.
- A sanitized example of a recurring review bug.
- A stronger redaction rule.

## Not Accepted

- Private incident timelines.
- Secret-bearing logs.
- Repo-specific closeout evidence.
- Tooling that calls a live service without a clear local/offline boundary.

## Review Standard

Before requesting review, check:

- the text is useful outside your source repository,
- placeholders are generic,
- public-evidence guidance is followed,
- success logs are summarized and failed logs are excerpted only when needed.
