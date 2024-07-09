# OpenBanking::MonthlyIncome

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **estimated_monthly_base_pay** | **Float** | Mastercard Open Banking estimated monthly base pay amount for the employment | [optional] |
| **estimated_monthly_overtime_pay** | **Float** | Mastercard Open Banking estimated monthly overtime pay amount for the employment | [optional] |
| **estimated_monthly_bonus_pay** | **Float** | Mastercard Open Banking estimated monthly bonus pay amount for the employment | [optional] |
| **estimated_monthly_other_pay** | **Float** | Mastercard Open Banking estimated monthly other pay amount for the employment | [optional] |
| **estimated_monthly_total_pay** | **Float** | Sum of all Mastercard Open Banking estimated monthly pay amounts |  |
| **estimated_monthly_commission_pay** | **Float** | Mastercard Open Banking estimated monthly commission pay amount for the employment | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::MonthlyIncome.new(
  estimated_monthly_base_pay: 123.45,
  estimated_monthly_overtime_pay: 123.45,
  estimated_monthly_bonus_pay: 123.45,
  estimated_monthly_other_pay: 123.45,
  estimated_monthly_total_pay: 123.45,
  estimated_monthly_commission_pay: 123.45
)
```

