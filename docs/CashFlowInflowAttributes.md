# OpenBanking::CashFlowInflowAttributes

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **average_deposit_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Average value of deposits during periods in the report | [optional] |
| **count_deposits_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndCount&gt;**](ObbDateRangeAndCount.md) | Count of all deposits during periods in the report |  |
| **historic_count_of_deposit_transactions** | **Integer** | Count of ALL deposits over entire known history of the account (may exceed requested length of report) |  |
| **historic_sum_of_deposits** | **Float** | Sum of ALL deposits over entire known history of the account (may exceed requested length of report) | [optional] |
| **maximum_deposit_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Maximum deposit value for different periods in the report |  |
| **minimum_deposit_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Minimum deposit value for different periods in the report |  |
| **sum_deposits_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Sum of all deposits during periods in the report |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowInflowAttributes.new(
  average_deposit_by_month_for_the_report_time_period: null,
  count_deposits_by_month_for_the_report_time_period: null,
  historic_count_of_deposit_transactions: 20,
  historic_sum_of_deposits: 389.22,
  maximum_deposit_by_month_for_the_report_time_period: null,
  minimum_deposit_by_month_for_the_report_time_period: null,
  sum_deposits_by_month_for_the_report_time_period: null
)
```

