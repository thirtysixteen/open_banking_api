# OpenBanking::InitiatedMicroDeposit

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | An account ID | [optional] |
| **status** | **String** | Micro entries successful initiation status | [optional] |
| **deposit_count** | **Integer** | Count of micro entries | [optional] |
| **status_description** | **String** | Micro entries successful initiation description | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::InitiatedMicroDeposit.new(
  account_id: 5011648377,
  status: Pending,
  deposit_count: 2,
  status_description: Micro entries successfully initiated
)
```

