# OpenBanking::LoanPaymentDetailsLoan

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | An account ID |  |
| **loan_number** | **String** | Institution&#39;s ID of the Student Loan |  |
| **loan_payment_number** | **String** | The payment number given by the institution. This number is typically for manual payments. This is not an ACH payment number. |  |
| **loan_payment_address** | **String** | The payment address to which send manual payments should be sent |  |
| **loan_future_payoff_amount** | **Float** | The payoff amount for the loan | [optional] |
| **loan_future_payoff_date** | **Time** | The date to which the \&quot;Future Payoff Amount\&quot; applies | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::LoanPaymentDetailsLoan.new(
  account_id: 5011648377,
  loan_number: 3210-Group A-1,
  loan_payment_number: 00001234895413-A-1,
  loan_payment_address: P.O. Box 123 Sioux Falls, IA 51054,
  loan_future_payoff_amount: 5000,
  loan_future_payoff_date: 2022-01-01T00:00Z
)
```

