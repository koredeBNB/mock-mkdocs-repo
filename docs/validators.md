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
- `reward_rate`: the validator reward rate.

Example response:

```json
{
  "validator_id": "validator-1",
  "status": "active",
  "commission_rate": 0.05,
  "reward_rate": 0.12
}
```

## Documentation Update Test

For the end-to-end demo, change the source API in `mock-bsc-app`, merge the change into `main`, and confirm the GitHub App opens a pull request against this documentation repo.