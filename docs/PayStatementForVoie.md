# OpenBanking::PayStatementForVoie

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pay_period** | **String** | The pay period of the pay statement | [optional] |
| **billable** | **Boolean** | This will display true if the pay statement is billable. If a pay statement has been digitized previously, this will display as false as it will not be billable. |  |
| **asset_id** | **String** | The asset ID of the stored pay statement |  |
| **pay_date** | **Integer** | The listed pay date for the pay statement | [optional] |
| **start_date** | **Integer** | The beginning of the pay period | [optional] |
| **end_date** | **Integer** | The end of the pay period | [optional] |
| **net_pay_current** | **Float** | The total pay after deductions for the employee for the current pay period | [optional] |
| **net_pay_ytd** | **Float** | The total accumulation of pay after deductions for the employee for the current pay year | [optional] |
| **gross_pay_current** | **Float** | The total pay before deductions for the employee for the current pay period | [optional] |
| **gross_pay_ytd** | **Float** | The total accumulation of pay before deductions for the employee for the current pay year | [optional] |
| **payroll_provider** | **String** | The payroll provider extracted from the pay statement | [optional] |
| **employer** | [**Employer**](Employer.md) |  |  |
| **employee** | [**Employee**](Employee.md) |  |  |
| **pay_stat** | [**Array&lt;PayStat&gt;**](PayStat.md) | Information pertaining to the earnings on the pay statement |  |
| **direct_deposits** | [**Array&lt;DirectDeposit&gt;**](DirectDeposit.md) | Information pertaining to the direct deposits on the pay statement | [optional] |
| **institutions** | **Array&lt;String&gt;** | Not populated for the voieWithStatement style of paystub report. For the VOIE - Paystub (with TXVerify) reports this would include details of the financial institution accounts and income streams with matching transactions to the pay statement. |  |
| **error_code** | **Integer** | Error code for the asset | [optional] |
| **error_message** | **String** | Error message for the asset | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PayStatementForVoie.new(
  pay_period: LastPayPeriod,
  billable: true,
  asset_id: 6f8fb0a0-e882-4f57-b672-cf53f1397581,
  pay_date: 1559241000,
  start_date: 1557513000,
  end_date: 1558722600,
  net_pay_current: 1802.22,
  net_pay_ytd: 36000,
  gross_pay_current: 24200,
  gross_pay_ytd: 72600,
  payroll_provider: Finicity,
  employer: null,
  employee: null,
  pay_stat: null,
  direct_deposits: null,
  institutions: [],
  error_code: 0,
  error_message: Some error message
)
```

