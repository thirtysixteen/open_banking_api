# OpenBanking::PayrollVOIEIncomeRecord

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pay_frequency** | **String** | The current pay frequency or how often a regular pay check is:  * &#x60;Daily&#x60;  * &#x60;Weekly&#x60;  * &#x60;Bi-Weekly&#x60;  * &#x60;Semi-Monthly&#x60;  * &#x60;Monthly&#x60;  * &#x60;Quarterly&#x60;  * &#x60;Semi-Annual&#x60;  * &#x60;Annual&#x60;  * &#x60;Every 2.6 wks&#x60;  * &#x60;Every 4 wks&#x60;  * &#x60;Every 5.2 wks&#x60;  * &#x60;Other&#x60;  * &#x60;Unknown&#x60;  | [optional] |
| **pay_type** | **String** | The current pay type:  * &#x60;Salary&#x60;  * &#x60;Hourly&#x60;  * &#x60;Daily&#x60;  | [optional] |
| **base_pay_rate** | **Float** | The current base or regular pay rate. Please use in conjunction with the &#x60;basePayRateUnit&#x60; field. | [optional] |
| **base_pay_rate_unit** | **String** | Unit for the base pay rate:  * &#x60;Hourly&#x60;  * &#x60;Daily&#x60;  * &#x60;Weekly&#x60;  * &#x60;Bi-Weekly&#x60;  * &#x60;Semi-Monthly&#x60;  * &#x60;Monthly&#x60;  * &#x60;Quarterly&#x60;  * &#x60;Semi-Annual&#x60;  * &#x60;Annual&#x60;  * &#x60;Every 2.6 wks&#x60;  * &#x60;Every 5.2 wks&#x60;  * &#x60;Other&#x60;  | [optional] |
| **oldest_pay_statement_available** | **String** | The date of the oldest direct pay statement available from the payroll source, as measured by the oldest &#x60;payDate&#x60; from all the pay statements delivered. | [optional] |
| **annual_income** | [**Array&lt;AnnualIncome&gt;**](AnnualIncome.md) | The annual pay for the current year, through prior year 2 (as available)  This is a mandatory field only for VOIE-payroll report type. | [optional] |
| **monthly_income** | [**MonthlyIncome**](MonthlyIncome.md) |  | [optional] |
| **direct_pay_statements** | [**Array&lt;DirectPayStatements&gt;**](DirectPayStatements.md) | An array of payment histories for each available paycheck | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PayrollVOIEIncomeRecord.new(
  pay_frequency: Weekly,
  pay_type: Daily,
  base_pay_rate: 1234.56,
  base_pay_rate_unit: Annual,
  oldest_pay_statement_available: 1527832900,
  annual_income: null,
  monthly_income: null,
  direct_pay_statements: null
)
```

