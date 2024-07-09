# OpenBanking::DirectPayStatements

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payroll_pay_history_id** | **String** | An ID for the income and employment details for the given pay period |  |
| **last_pay_period_indicator** | **Boolean** | Most recent available pay check |  |
| **main_pay_statement_fields** | [**MainPayStatementFields**](MainPayStatementFields.md) |  |  |
| **earnings** | [**Array&lt;Earnings&gt;**](Earnings.md) | Categorization of pay, for the pay period |  |
| **deductions** | [**Array&lt;Deductions&gt;**](Deductions.md) | Deductions from the pay check | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::DirectPayStatements.new(
  payroll_pay_history_id: qsrt2hmjnf,
  last_pay_period_indicator: true,
  main_pay_statement_fields: null,
  earnings: null,
  deductions: null
)
```

