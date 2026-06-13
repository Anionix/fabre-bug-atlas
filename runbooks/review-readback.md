# Review Readback Runbook

Use compact readback first. Expand comment bodies only for new, unanswered, or
blocking comments.

## Pull Request List

```sh
gh pr list --repo OWNER/REPO --state open \
  --json number,baseRefName,headRefName,mergeStateStatus,isDraft,updatedAt
```

Report PR number, base/head, merge state, draft state, and whether the state
changed since the prior readback.

## Review Thread Pagination

Always paginate review threads before counting unresolved comments.

```sh
gh api graphql -F owner=OWNER -F name=REPO -F number=NUMBER -f query='
query($owner: String!, $name: String!, $number: Int!, $after: String) {
  repository(owner: $owner, name: $name) {
    pullRequest(number: $number) {
      reviewThreads(first: 100, after: $after) {
        pageInfo { hasNextPage endCursor }
        nodes {
          isResolved
          isOutdated
          comments(last: 1) {
            nodes { author { login } createdAt url }
          }
        }
      }
    }
  }
}'
```

If `hasNextPage` is true, repeat with the returned cursor and combine the
nodes before counting.

## Merge Readiness

Use this compact shape:

```text
PR <number>: <merge state>
current unresolved review threads: <count>
outdated unresolved review threads: <count>
checks: <summary>
next action: <merge / wait / fix>
```

When review bugs have been arriving after replies, perform two delayed
readbacks before merge.
