# Gas Fees

The mock BSC app exposes a gas fee status API.

## `get_gas_fee_status`

Use `get_gas_fee_status` to read current gas fee information.

```python
from mock_bsc_app.gas_fees import get_gas_fee_status

status = get_gas_fee_status("bnb-smart-chain")
```

The function returns a dictionary with these fields:

- `network`: the network identifier passed by the caller.
- `base_fee_gwei`: the base fee in gwei.
- `priority_fee_gwei`: the priority fee in gwei.
- `estimated_total_fee_gwei`: the estimated total fee in gwei.
- `congestion_level`: the current network congestion level.
- `sample_block`: a sample block number.
- `fee_trend`: the direction the fee is moving (e.g. `"rising"`).

Example response:

```json
{
  "network": "bnb-smart-chain",
  "base_fee_gwei": 3.5,
  "priority_fee_gwei": 1.1,
  "estimated_total_fee_gwei": 4.6,
  "congestion_level": "medium",
  "sample_block": 39126000,
  "fee_trend": "rising"
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
