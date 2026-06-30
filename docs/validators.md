# Validators

The mock BSC app exposes a small validator status API.

## `get_validator_status`

Use `get_validator_status` to read a validator status payload.

```python
from mock_bsc_app.validators import get_validator_status

status = get_validator_status("validator-1")
```

The function returns a dictionary with these fields:

- `validator_id`: the validator identifier passed by the caller.
- `status`: the validator status. The current demo value is `active`.
- `commission_rate`: the validator commission rate.
- `voting_power`: the validator's current voting power.
- `delegator_count`: the number of delegators currently attached to the validator.
- `uptime_percent`: the validator uptime percentage.
- `jailed_bnb`: whether the validator is currently jailed.
- `slashable`: whether the validator is currently slashable.
- `reward_rate`: the validator reward rate.

Example response:

```json
{
  "validator_id": "validator-1",
  "status": "active",
  "commission_rate": 0.05,
  "voting_power": 1000,
  "delegator_count": 25,
  "uptime_percent": 99.9,
  "jailed_bnb": false,
  "slashable": false,
  "reward_rate": 0.12
}
```

## Try it: interactive playground

Run the API and inspect the response without leaving the docs.

<iframe
  src="https://bnb-chain.github.io/techops-docsite-interactive-playground/?validator=validator-1"
  width="100%"
  height="720"
  style="border: 1px solid #ddd; border-radius: 8px;"
  loading="lazy"
></iframe>

<p>
  <a href="https://bnb-chain.github.io/techops-docsite-interactive-playground/" target="_blank">
    Open the playground in a new tab
  </a>
</p>

## Documentation Update Test

For the end-to-end demo, change the source API in `mock-bsc-app`, merge the change into `main`, and confirm the GitHub App opens a pull request against this documentation repo.
