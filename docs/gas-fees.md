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
- `congestion_level`: the network congestion level.
- `sample_block`: the sample block number.

Example response:

```json
{
  "network": "bnb-smart-chain",
  "base_fee_gwei": 3.2,
  "priority_fee_gwei": 0.8,
  "estimated_total_fee_gwei": 4.0,
  "congestion_level": "low",
  "sample_block": 39124801
}
```
