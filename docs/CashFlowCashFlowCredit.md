# OpenBanking::CashFlowCashFlowCredit

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monthly_cash_flow_credits** | [**Array&lt;CashFlowMonthlyCashFlowCredits&gt;**](CashFlowMonthlyCashFlowCredits.md) | List of attributes for each month |  |
| **twelve_month_credit_total** | **Float** | Sum of all credit transactions for each month by account | [optional] |
| **twelve_month_credit_total_less_transfers** | **Float** | Sum of all monthly credit transactions without transfers for the account | [optional] |
| **six_month_credit_total** | **Float** | Sum of six month credit transactions | [optional] |
| **six_month_credit_total_less_transfers** | **Float** | Sum of six month credit transactions without transfers | [optional] |
| **two_month_credit_total** | **Float** | Sum of two month credit transactions | [optional] |
| **two_month_credit_total_less_transfers** | **Float** | Sum of two month credit transactions without transfers | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowCashFlowCredit.new(
  monthly_cash_flow_credits: null,
  twelve_month_credit_total: 1200,
  twelve_month_credit_total_less_transfers: 1000,
  six_month_credit_total: 750,
  six_month_credit_total_less_transfers: 500,
  two_month_credit_total: 150,
  two_month_credit_total_less_transfers: 100
)
```

