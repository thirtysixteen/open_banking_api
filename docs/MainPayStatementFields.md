# OpenBanking::MainPayStatementFields

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pay_date** | **Integer** | Pay date for the pay period |  |
| **start_date** | **Integer** | Start date for the pay period | [optional] |
| **end_date** | **Integer** | End date for the pay period | [optional] |
| **pay_period_hours** | **Float** | Sum of all hours worked each week for the pay period | [optional] |
| **pay_frequency** | **String** | The current pay frequency, or how often a regular pay check is distributed:  * &#x60;Daily&#x60;  * &#x60;Weekly&#x60;  * &#x60;Bi-Weekly&#x60;  * &#x60;Semi-Monthly&#x60;  * &#x60;Monthly&#x60;  * &#x60;Quarterly&#x60;  * &#x60;Semi-Annual&#x60;  * &#x60;Annual&#x60;  * &#x60;Every 2.6 wks&#x60;  * &#x60;Every 4 wks&#x60;  * &#x60;Every 5.2 wks&#x60;  * &#x60;Other&#x60;  | [optional] |
| **pay_type** | **String** | Current pay type:  * &#x60;Salary&#x60;  * &#x60;Hourly&#x60;  * &#x60;Daily&#x60;  | [optional] |
| **gross_pay_amount** | **Float** | Gross pay amount for the pay period |  |
| **gross_pay_amount_ytd** | **Float** | Year to date (YTD) gross pay amount at the time of payment | [optional] |
| **net_pay_amount** | **Float** | Net pay amount for a pay period | [optional] |
| **net_pay_amount_ytd** | **Float** | Year to date (YTD) net pay amount at the time of payment | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::MainPayStatementFields.new(
  pay_date: 1607450357,
  start_date: 1607450357,
  end_date: 1607450357,
  pay_period_hours: 39.75,
  pay_frequency: Weekly,
  pay_type: Hourly,
  gross_pay_amount: 755.25,
  gross_pay_amount_ytd: 4256,
  net_pay_amount: 608.77,
  net_pay_amount_ytd: 2345.99
)
```

