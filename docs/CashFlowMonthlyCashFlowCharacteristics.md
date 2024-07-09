# OpenBanking::CashFlowMonthlyCashFlowCharacteristics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **month** | **Integer** | One instance for each complete calendar month in the report |  |
| **total_credits_less_total_debits** | **Float** | Total Credits - Total Debits by month |  |
| **total_credits_less_total_debits_less_transfers** | **Float** | Total Credits - Total Debits by month (Without Transfers) |  |
| **average_transaction_amount** | **Float** | Average transaction amount by month |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowMonthlyCashFlowCharacteristics.new(
  month: 1512111600,
  total_credits_less_total_debits: 15000,
  total_credits_less_total_debits_less_transfers: 11000,
  average_transaction_amount: 10
)
```

