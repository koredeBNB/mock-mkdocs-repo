# Block Sync

The mock BSC app exposes a block synchronization status API.

## `get_block_sync_status`

Use `get_block_sync_status` to read the current block synchronization status.

```python
from mock_bsc_app.block_sync import get_block_sync_status

status = get_block_sync_status("bnb-smart-chain")
```

The function returns a dictionary with these fields:

- `network`: the network identifier passed by the caller.
- `latest_block`: the most recent block number seen by the node.
- `safe_block`: the latest block considered safe.
- `finalized_block`: the latest finalized block number.
- `sync_lag_blocks`: the number of blocks the node is behind the chain tip.
- `is_syncing`: whether the node is currently syncing.

Example response:

```json
{
  "network": "bnb-smart-chain",
  "latest_block": 39126000,
  "safe_block": 39125920,
  "finalized_block": 39125810,
  "sync_lag_blocks": 80,
  "is_syncing": false
}
```

## Try it: interactive playground

Run the API and inspect the response without leaving the docs.

<iframe
  src="https://koredebnb.github.io/techops-docsite-interactive-playground/?network=bnb-smart-chain"
  width="100%"
  height="720"
  style="border: 1px solid #ddd; border-radius: 8px;"
  loading="lazy"
></iframe>

<p>
  <a href="https://koredebnb.github.io/techops-docsite-interactive-playground/" target="_blank">
    Open the playground in a new tab
  </a>
</p>

## Documentation Update Test

For the end-to-end demo, change the source API in `mock-bsc-app`, merge the change into `main`, and confirm the GitHub App opens a pull request against this documentation repo.
