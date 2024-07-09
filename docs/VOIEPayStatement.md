# OpenBanking::VOIEPayStatement

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pay_period** | **String** | The pay period of the pay statement | [optional] |
| **billable** | **Boolean** | Designates whether the pay statement is billable | [optional] |
| **asset_id** | **String** | The asset ID of the stored pay statement | [optional] |
| **pay_date** | **Integer** | The listed pay date for the pay statement | [optional] |
| **start_date** | **Integer** | The beginning of the pay period | [optional] |
| **end_date** | **Integer** | The end of the pay period | [optional] |
| **net_pay_current** | **Float** | The total pay after deductions for the employee for the current pay period | [optional] |
| **net_pay_ytd** | **Float** | The total accumulation of pay after deductions for the employee for the current pay year | [optional] |
| **gross_pay_current** | **Float** | The total pay before deductions for the employee for the current pay period | [optional] |
| **gross_pay_ytd** | **Float** | The total accumulation of pay before deductions for the employee for the current pay year | [optional] |
| **payroll_provider** | **String** | The company that provides the pay stub. | [optional] |
| **match_type** | **String** | The statement match category. Possible values:    * \&quot;NET_PAY_MATCH\&quot;     * \&quot;SPLIT_INTERVIEW_AMOUNT_SUM_TO_NET_PAY_MATCH\&quot;     * \&quot;SPLIT_DIRECT_DEPOSIT_SUM_TO_NET_PAY_MATCH\&quot;     * \&quot;SPLIT_LESS_THAN_NET_PAY_SUM_TO_NET_PAY_MATCH\&quot;     * \&quot;PARTIAL\&quot;     * \&quot;TRANSACTION_DATE_RANGE_INVALID\&quot;     * \&quot;NO_MATCH\&quot; | [optional] |
| **employer** | [**Employer**](Employer.md) |  | [optional] |
| **employee** | [**Employee**](Employee.md) |  | [optional] |
| **pay_stat** | [**Array&lt;PayStat&gt;**](PayStat.md) | Information pertaining to the earnings on the pay statement | [optional] |
| **deductions** | [**Array&lt;Deduction&gt;**](Deduction.md) | Information pertaining to deductions on the pay statement | [optional] |
| **direct_deposits** | [**Array&lt;DirectDeposit&gt;**](DirectDeposit.md) | Information pertaining to direct deposits on the pay statement | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::VOIEPayStatement.new(
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
  match_type: PARTIAL,
  employer: null,
  employee: null,
  pay_stat: null,
  deductions: null,
  direct_deposits: null
)
```

