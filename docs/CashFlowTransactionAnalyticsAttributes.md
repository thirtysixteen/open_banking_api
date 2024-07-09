# OpenBanking::CashFlowTransactionAnalyticsAttributes

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **activity_deposits_credits_for_the_report_time_period** | [**Array&lt;CashFlowActivityDepositsCredits&gt;**](CashFlowActivityDepositsCredits.md) | List of all deposit transactions posted to the account during the report period |  |
| **activity_withdrawals_debits_for_the_report_time_period** | [**Array&lt;CashFlowActivityWithdrawalsDebits&gt;**](CashFlowActivityWithdrawalsDebits.md) | List of all withdrawal transactions posted to the account during the report period |  |
| **average_transaction_value_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Average value of transactions during periods in the report. Values may be positive or negative |  |
| **historic_weeks_with_zero_transactions** | [**CashFlowNumWeeksZeros**](CashFlowNumWeeksZeros.md) |  | [optional] |
| **last_transaction_date** | [**Array&lt;CashFlowTransactionAnalyticsAttributesLastTransactionDateInner&gt;**](CashFlowTransactionAnalyticsAttributesLastTransactionDateInner.md) | Latest posted transaction(s) to the account. May be more than one if they share the same timestamp | [optional] |
| **net_cash_flow_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Net cash flow for each month during the report period | [optional] |
| **net_cash_flow_for_the_report_time_period** | **Float** | Net cash flow during the report period (may be positive or negative) | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowTransactionAnalyticsAttributes.new(
  activity_deposits_credits_for_the_report_time_period: null,
  activity_withdrawals_debits_for_the_report_time_period: null,
  average_transaction_value_by_month_for_the_report_time_period: null,
  historic_weeks_with_zero_transactions: null,
  last_transaction_date: null,
  net_cash_flow_by_month_for_the_report_time_period: null,
  net_cash_flow_for_the_report_time_period: 1544.94
)
```

