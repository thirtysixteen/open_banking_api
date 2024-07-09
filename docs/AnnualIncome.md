# OpenBanking::AnnualIncome

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **String** | The year for the amounts given in YTD totals for an employer |  |
| **gross_pay_amount_ytd** | **Float** | Year to date (YTD) gross pay amount for the indicated year |  |
| **net_pay_amount_ytd** | **Float** | Year to date (YTD) net pay amount for the indicated year | [optional] |
| **base_pay_amount_ytd** | **Float** | Year to date (YTD) base pay amount for the year indicated | [optional] |
| **overtime_pay_amount_ytd** | **Float** | Year to date (YTD) overtime pay amount for the year indicated | [optional] |
| **other_pay_amount_ytd** | **Float** | Year to date (YTD) other pay amount for the indicated year. Other pay is pay that is not categorized into one of the other categories. | [optional] |
| **commission_pay_amount_ytd** | **Float** | Year to date (YTD) commission pay amount for the indicated year | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AnnualIncome.new(
  year: 2022,
  gross_pay_amount_ytd: 123.45,
  net_pay_amount_ytd: 123.45,
  base_pay_amount_ytd: 123.45,
  overtime_pay_amount_ytd: 123.45,
  other_pay_amount_ytd: 123.45,
  commission_pay_amount_ytd: 123.45
)
```

