# OpenBanking::ACHDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **routing_number** | **String** | The routing number of the financial institution for specific customer account |  |
| **real_account_number** | **String** | The account number for initiating ACH transfers for this account |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ACHDetails.new(
  routing_number: 123456789,
  real_account_number: 002345678901
)
```

