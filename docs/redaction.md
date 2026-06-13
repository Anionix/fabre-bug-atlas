# Redaction Guide

Use this guide before promoting a private observation into public runbooks,
templates, or examples.

## Keep

- Public pull request or issue numbers.
- Public URLs.
- Generic root cause.
- Recurrence class.
- Prevention rule.
- Public-safe command names.

## Remove

- Local absolute paths.
- Home-relative paths.
- Raw environment values.
- Credential-shaped strings.
- Private repository URLs.
- Raw command logs.
- Personal names that are not necessary for the lesson.

## Rewrite Table

| Private wording | Public wording |
| --- | --- |
| A local build path was exposed. | A machine-specific path was exposed. |
| A token-shaped value appeared in a PR body. | Credential-shaped values must be scanned before publishing. |
| A private review thread was missed. | Review-thread pagination and delayed readback were incomplete. |
| A repo-specific validator missed a generated artifact. | Artifact freshness validation did not cover generated output. |

## Promotion Checklist

- [ ] The lesson works for more than one repository.
- [ ] The text contains no private URL.
- [ ] The text contains no local path or environment value.
- [ ] The text uses placeholders where a repo-specific value would appear.
- [ ] The text explains the prevention rule, not only the incident.
