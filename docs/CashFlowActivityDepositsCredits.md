# OpenBanking::CashFlowActivityDepositsCredits

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date** | **String** | Date the deposit transaction was posted |  |
| **deposits_credits** | **Float** | Amount of the deposit |  |
| **transaction_description** | **String** | Description of transaction | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowActivityDepositsCredits.new(
  date: 2020-03-25,
  deposits_credits: 500,
  transaction_description: VENMO            CASHOUT
)
```

