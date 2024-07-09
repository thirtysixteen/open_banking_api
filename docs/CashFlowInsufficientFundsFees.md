# OpenBanking::CashFlowInsufficientFundsFees

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **count_of_transactions_for_the_report_time_period** | **Integer** | Count of all NSF transactions during the report | [optional] |
| **sum_of_transactions_for_the_report_time_period** | **Float** | Sum of all NSF transactions during the report | [optional] |
| **transactions** | [**Array&lt;InsufficientFundsTransaction&gt;**](InsufficientFundsTransaction.md) | Transactions categorized as NSF | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowInsufficientFundsFees.new(
  count_of_transactions_for_the_report_time_period: 1,
  sum_of_transactions_for_the_report_time_period: -1.65,
  transactions: null
)
```

