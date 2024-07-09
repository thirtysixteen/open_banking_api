# OpenBanking::CashFlowOutflowAttributes

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **average_withdrawal_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Average value of withdrawals during periods in the report | [optional] |
| **count_withdrawals_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndCount&gt;**](ObbDateRangeAndCount.md) | Count of all withdrawals during periods in the report |  |
| **historic_count_of_withdrawal_transactions** | **Integer** | Count of ALL withdrawals over entire known history of the account (may exceed requested length of report) |  |
| **historic_sum_of_withdrawals** | **Float** | Sum of ALL withdrawals over entire known history of the account (may exceed requested length of report) | [optional] |
| **maximum_withdrawal_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Maximum withdrawal value for different periods in the report |  |
| **minimum_withdrawal_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Minimum withdrawal value for different periods in the report |  |
| **sum_withdrawals_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Sum of all withdrawals during periods in the report |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowOutflowAttributes.new(
  average_withdrawal_by_month_for_the_report_time_period: null,
  count_withdrawals_by_month_for_the_report_time_period: null,
  historic_count_of_withdrawal_transactions: 20,
  historic_sum_of_withdrawals: 925.66,
  maximum_withdrawal_by_month_for_the_report_time_period: null,
  minimum_withdrawal_by_month_for_the_report_time_period: null,
  sum_withdrawals_by_month_for_the_report_time_period: null
)
```

