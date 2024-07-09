# OpenBanking::LoanPaymentDetailsAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | An account ID |  |
| **account_number** | **String** | Institution&#39;s ID of the Student Loan Account |  |
| **account_payment_number** | **String** | The payment number given by the institution. This number is typically for manual payments. This is not an ACH payment number. |  |
| **account_payment_address** | **String** | The payment address to which send manual payments should be sent |  |
| **account_future_payoff_amount** | **Float** | The payoff amount for the account | [optional] |
| **account_future_payoff_date** | **Time** | The date to which the \&quot;Future Payoff Amount\&quot; applies | [optional] |
| **group_detail** | [**Array&lt;LoanPaymentDetailsGroup&gt;**](LoanPaymentDetailsGroup.md) | Group details | [optional] |
| **loan_detail** | [**Array&lt;LoanPaymentDetailsLoan&gt;**](LoanPaymentDetailsLoan.md) | Loan details | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::LoanPaymentDetailsAccount.new(
  account_id: 5011648377,
  account_number: 9876543210,
  account_payment_number: 00001234895413,
  account_payment_address: P.O. Box 123 Sioux Falls, IA 51054,
  account_future_payoff_amount: 10000,
  account_future_payoff_date: 2022-01-01T00:00Z,
  group_detail: null,
  loan_detail: null
)
```

