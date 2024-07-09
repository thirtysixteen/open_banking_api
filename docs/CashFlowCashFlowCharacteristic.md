# OpenBanking::CashFlowCashFlowCharacteristic

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **monthly_cash_flow_characteristics** | [**Array&lt;CashFlowMonthlyCashFlowCharacteristics&gt;**](CashFlowMonthlyCashFlowCharacteristics.md) | List of attributes for each month |  |
| **average_monthly_net** | **Float** | Average (Total Credits - Total Debits) for the account |  |
| **average_monthly_net_less_transfers** | **Float** | Average (Total Credits - Total Debits) without transfers for the account |  |
| **twelve_month_total_net** | **Float** | Sum of all monthly (Total Credits - Total Debits) each month for the account | [optional] |
| **twelve_month_total_net_less_transfers** | **Float** | Sum of all monthly (Total Credits - Total Debits) without transfers for the account | [optional] |
| **six_month_average_total_credits_less_total_debits** | **Float** | 6 Month Average (Total Credits - Total Debits) | [optional] |
| **six_month_average_total_credits_less_total_debits_less_transfers** | **Float** | 6 Month Average (Total Credits - Total Debits) - (Without Transfers) | [optional] |
| **two_month_average_total_credits_less_total_debits** | **Float** | 2 Month Average (Total Credits - Total Debits) | [optional] |
| **two_month_average_total_credits_less_total_debits_less_transfers** | **Float** | 2 Month Average (Total Credits - Total Debits) - (Without Transfers) | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowCashFlowCharacteristic.new(
  monthly_cash_flow_characteristics: null,
  average_monthly_net: 2350,
  average_monthly_net_less_transfers: 1000,
  twelve_month_total_net: 12500,
  twelve_month_total_net_less_transfers: 12400,
  six_month_average_total_credits_less_total_debits: 55555,
  six_month_average_total_credits_less_total_debits_less_transfers: 55555,
  two_month_average_total_credits_less_total_debits: 55555,
  two_month_average_total_credits_less_total_debits_less_transfers: 55555
)
```

