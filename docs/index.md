# Mock BNB Chain Docs

This documentation site is used to test the AI docsite update GitHub App.

It documents the public behavior of the mock source repository:

- Source repo: [koredeBNB/mock-bsc-app](https://github.com/koredeBNB/mock-bsc-app)
- Main documented API: `get_validator_status` and `get_gas_fee_status`

## Demo Goal

When a pull request is merged in the mock source app, the GitHub App should:

1. receive a GitHub webhook,
2. inspect the merged source diff,
3. identify affected documentation in this MkDocs repo,
4. update the relevant Markdown page,
5. open a pull request for human review.
