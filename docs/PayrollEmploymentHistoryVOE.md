# OpenBanking::PayrollEmploymentHistoryVOE

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **as_of_date** | **Integer** | The last time the payroll data was updated in the payroll provider&#39;s system |  |
| **employer_name** | **String** | Name of the employer as stated by the employer in the payroll system |  |
| **payroll_source** | **String** | The name of the payroll source where the data was retrieved |  |
| **payroll_provider** | **String** | The name of the provider who provides payroll data to payroll source | [optional] |
| **employee** | [**PayrollEmployeeRecord**](PayrollEmployeeRecord.md) |  |  |
| **employment** | [**PayrollEmploymentRecord**](PayrollEmploymentRecord.md) |  |  |
| **income** | [**PayrollVOEIncomeRecord**](PayrollVOEIncomeRecord.md) |  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PayrollEmploymentHistoryVOE.new(
  as_of_date: 1596175200,
  employer_name: ACME INC,
  payroll_source: finPayroll,
  payroll_provider: Paychex,
  employee: null,
  employment: null,
  income: null
)
```

