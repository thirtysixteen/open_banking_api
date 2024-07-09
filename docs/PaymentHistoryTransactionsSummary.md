# OpenBanking::PaymentHistoryTransactionsSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total_non_sufficient_funds** | **Float** | Total of NSF transactions |  |
| **average_monthly_non_sufficient_funds** | **Float** | Monthly average of NSF transactions |  |
| **total_deposits** | **Float** | Total of deposit transactions |  |
| **average_monthly_deposits** | **Float** | Monthly average of deposit transactions |  |
| **total_withdrawals** | **Float** | Total of withdrawals transactions |  |
| **average_monthly_withdrawals** | **Float** | Monthly average of withdrawal transactions |  |
| **begin_date** | **String** | ISO-8601 date of earliest transaction |  |
| **end_date** | **String** | ISO-8601 date of latest transaction |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PaymentHistoryTransactionsSummary.new(
  total_non_sufficient_funds: null,
  average_monthly_non_sufficient_funds: null,
  total_deposits: null,
  average_monthly_deposits: null,
  total_withdrawals: null,
  average_monthly_withdrawals: null,
  begin_date: null,
  end_date: null
)
```

