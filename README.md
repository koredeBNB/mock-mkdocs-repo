# Mock MkDocs Repo

Small MkDocs documentation repository used to test the AI docsite update GitHub App.

This repo stands in for the BNB Chain docsite. It documents the public API behavior of [`koredeBNB/mock-bsc-app`](https://github.com/koredeBNB/mock-bsc-app).

## Local Development

Install MkDocs:

```bash
python3 -m pip install -r requirements.txt
```

Run the local dev server:

```bash
mkdocs serve
```

Validate the static site:

```bash
mkdocs build --strict
```

## Demo Flow

1. Merge a source change in `mock-bsc-app`.
2. The GitHub App receives the merged PR webhook.
3. The AI worker updates the relevant page in this repo.
4. The worker opens a documentation pull request for review.
