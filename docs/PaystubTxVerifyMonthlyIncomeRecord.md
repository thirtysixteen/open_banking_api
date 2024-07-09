# OpenBanking::PaystubTxVerifyMonthlyIncomeRecord

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **estimated_monthly_base_pay** | **Float** | The estimated monthly base pay amount for the employment from the paystub, calculated by Finicity | [optional] |
| **estimated_monthly_overtime_pay** | **Float** | The estimated monthly overtime pay amount for the employment from the paystub, calculated by Finicity | [optional] |
| **estimated_monthly_bonus_pay** | **Float** | The estimated monthly bonus pay amount for the employment from the paystub, calculated by Finicity | [optional] |
| **estimated_monthly_commission_pay** | **Float** | The estimated commission bonus pay amount for the employment from the paystub, calculated by Finicity | [optional] |
| **estimated_monthly_other_pay** | **Float** | The estimated monthly other pay amount for the employment from the paystub, calculated by Finicity | [optional] |
| **estimated_monthly_total_pay** | **Float** | The estimated monthly total pay amount for the employment from the paystub, calculated by Finicity | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PaystubTxVerifyMonthlyIncomeRecord.new(
  estimated_monthly_base_pay: 2000,
  estimated_monthly_overtime_pay: 50,
  estimated_monthly_bonus_pay: 20,
  estimated_monthly_commission_pay: 50,
  estimated_monthly_other_pay: 150,
  estimated_monthly_total_pay: 2120
)
```

