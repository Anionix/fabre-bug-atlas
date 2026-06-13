# Public Evidence Runbook

Public evidence is text that will be visible in a PR body, review reply, issue
closeout, release note, or public artifact.

## Allowed

- Public commands.
- Public issue and pull request URLs.
- Abstract local categories such as `local cache` or `local scratch target`.
- Compact validation summaries.
- Sanitized recurrence classes.

## Do Not Publish

- Local absolute paths.
- Home-relative paths.
- Local file URI paths.
- Raw environment variable values.
- Custom build target paths.
- Credential-shaped strings.
- Raw logs that contain machine-specific paths or private data.
- Private repository URLs in public repositories.

## Before Publishing

1. Save the exact public text that will be posted.
2. Scan that saved text with the repository's public-evidence checker or an
   equivalent local leak scan.
3. Scan the patch separately before claiming the patch is clean.
4. Replace machine-specific details with abstract categories.
5. Do not paste rejected raw values into the fix comment.

## Template Wording

```text
Public evidence:
- body leak scan: clean
- patch leak scan: clean
- local details abstracted as local cache or local scratch target
```
