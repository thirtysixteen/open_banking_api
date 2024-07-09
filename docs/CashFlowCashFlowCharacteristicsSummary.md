# OpenBanking::CashFlowCashFlowCharacteristicsSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monthly_cash_flow_characteristics_summaries** | [**Array&lt;CashFlowMonthlyCashFlowCharacteristicsSummaries&gt;**](CashFlowMonthlyCashFlowCharacteristicsSummaries.md) | List of attributes for each month | [optional] |
| **average_monthly_net** | **Float** | Average monthly net amount |  |
| **average_monthly_net_less_transfers** | **Float** | Average monthly net less transfers |  |
| **twelve_month_total_net** | **Float** | Sum of all monthly (Total Credits - Total Debits) each month by the account |  |
| **twelve_month_total_net_less_transfers** | **Float** | Sum of all monthly (Total Credits - Total Debits) without transfers by the account |  |
| **six_month_average_total_credits_less_total_debits** | **Float** | 6 Month Average (Total Credits - Total Debits) across all accounts |  |
| **six_month_average_total_credits_less_total_debits_less_transfers** | **Float** | 6 Month Average (Total Credits - Total Debits) - (Without Transfers) across all accounts |  |
| **two_month_average_total_credits_less_total_debits** | **Float** | 2 Month Average (Total Credits - Total Debits) across all accounts |  |
| **two_month_average_total_credits_less_total_debits_less_transfers** | **Float** | 2 Month Average (Total Credits - Total Debits) - (Without Transfers) across all accounts | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowCashFlowCharacteristicsSummary.new(
  monthly_cash_flow_characteristics_summaries: null,
  average_monthly_net: 1250,
  average_monthly_net_less_transfers: 1000,
  twelve_month_total_net: 12500,
  twelve_month_total_net_less_transfers: 12400,
  six_month_average_total_credits_less_total_debits: 55555,
  six_month_average_total_credits_less_total_debits_less_transfers: 55555,
  two_month_average_total_credits_less_total_debits: 55555,
  two_month_average_total_credits_less_total_debits_less_transfers: 55555
)
```

