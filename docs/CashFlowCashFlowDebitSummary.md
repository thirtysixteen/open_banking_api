# OpenBanking::CashFlowCashFlowDebitSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monthly_cash_flow_debit_summaries** | [**Array&lt;CashFlowMonthlyCashFlowDebitSummaries&gt;**](CashFlowMonthlyCashFlowDebitSummaries.md) | List of attributes for each month |  |
| **twelve_month_debit_total** | **Float** | Sum of all monthly debit transactions for each month by account |  |
| **twelve_month_debit_total_less_transfers** | **Float** | Sum of all monthly debit transactions without transfers for the account |  |
| **six_month_debit_total** | **Float** | Six month sum of all debit transactions by account |  |
| **six_month_debit_total_less_transfers** | **Float** | Six month sum of all debit transactions without transfers for the account |  |
| **two_month_debit_total** | **Float** | Two month sum of all debit transactions by account |  |
| **two_month_debit_total_less_transfers** | **Float** | Two month sum of all debit transactions without transfers for the account |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowCashFlowDebitSummary.new(
  monthly_cash_flow_debit_summaries: null,
  twelve_month_debit_total: -1200,
  twelve_month_debit_total_less_transfers: -1000,
  six_month_debit_total: -750,
  six_month_debit_total_less_transfers: -500,
  two_month_debit_total: -150,
  two_month_debit_total_less_transfers: -100
)
```

