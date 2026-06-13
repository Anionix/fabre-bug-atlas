# GitHub Review Thread Readback Example

This example uses placeholders so it can be copied to any GitHub repository.

```sh
gh api graphql -F owner=OWNER -F name=REPO -F number=NUMBER -f query='
query($owner: String!, $name: String!, $number: Int!, $after: String) {
  repository(owner: $owner, name: $name) {
    pullRequest(number: $number) {
      number
      title
      reviewThreads(first: 100, after: $after) {
        pageInfo { hasNextPage endCursor }
        nodes {
          isResolved
          isOutdated
          path
          line
          comments(first: 1) {
            nodes {
              url
              author { login }
              createdAt
            }
          }
        }
      }
    }
  }
}'
```

If pagination is required, repeat the query with the returned cursor and merge
the result sets before reporting counts.
