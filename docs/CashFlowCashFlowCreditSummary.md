# OpenBanking::CashFlowCashFlowCreditSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monthly_cash_flow_credit_summaries** | [**Array&lt;CashFlowMonthlyCashFlowCreditSummaries&gt;**](CashFlowMonthlyCashFlowCreditSummaries.md) | List of attributes for each month |  |
| **twelve_month_credit_total** | **Float** | Sum of all credit transactions for each month for all accounts |  |
| **twelve_month_credit_total_less_transfers** | **Float** | Sum of all monthly credit transactions without transfers for all accounts |  |
| **six_month_credit_total** | **Float** | Six month sum of all credit transactions |  |
| **six_month_credit_total_less_transfers** | **Float** | Six month sum of all monthly credit transactions without transfers for all accounts |  |
| **two_month_credit_total** | **Float** | Two month sum of all credit transactions |  |
| **two_month_credit_total_less_transfers** | **Float** | Two month sum of all monthly credit transactions without transfers for all accounts |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowCashFlowCreditSummary.new(
  monthly_cash_flow_credit_summaries: null,
  twelve_month_credit_total: 1200,
  twelve_month_credit_total_less_transfers: 1000,
  six_month_credit_total: 750,
  six_month_credit_total_less_transfers: 500,
  two_month_credit_total: 150,
  two_month_credit_total_less_transfers: 100
)
```

