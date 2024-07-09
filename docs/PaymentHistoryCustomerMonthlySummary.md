# OpenBanking::PaymentHistoryCustomerMonthlySummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **month** | **String** | Date of the month |  |
| **average_balance** | **Float** | Average balance for the month |  |
| **closing_balance** | **Float** | Closing balance for the month |  |
| **opening_balance** | **Float** | Opening balance for the month |  |
| **total_deposits** | **Float** | Total of deposit transactions for the month |  |
| **total_withdrawals** | **Float** | Total of withdrawal transactions for the month |  |
| **non_sufficient_funds** | **Float** | Total of NSF transactions for the month |  |
| **insurance_payments** | **Float** | Total of insurance payment transactions for the month |  |
| **tax_payments** | **Float** | Total of tax payment transactions for the month |  |
| **recurring_expense_payments** | **Float** | Total of recurring expense payment transactions for the month |  |
| **missed_recurring_expense_payments** | **Float** | Total of missed recurring expense payment transactions for the month |  |
| **recurring_loan_payments** | **Float** | Total of recurring loan payment transactions for the month |  |
| **missed_recurring_loan_payments** | **Float** | Total of missed recurring loan payment transactions for the month |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PaymentHistoryCustomerMonthlySummary.new(
  month: 2023-06-01,
  average_balance: 123.45,
  closing_balance: 123.45,
  opening_balance: 123.45,
  total_deposits: 123.45,
  total_withdrawals: 123.45,
  non_sufficient_funds: 3,
  insurance_payments: 123.45,
  tax_payments: 123.45,
  recurring_expense_payments: 543.21,
  missed_recurring_expense_payments: 123.45,
  recurring_loan_payments: 543.21,
  missed_recurring_loan_payments: 123.45
)
```

