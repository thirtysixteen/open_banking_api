# OpenBanking::CashFlowActivityWithdrawalsDebits

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date** | **String** | Date the withdrawal transaction was posted |  |
| **transaction_description** | **String** | Description of transaction | [optional] |
| **withdrawals_debits** | **Float** | Amount of the withdrawal |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowActivityWithdrawalsDebits.new(
  date: 2020-03-25,
  transaction_description: Payment to Chase card ending in,
  withdrawals_debits: 15.69
)
```

