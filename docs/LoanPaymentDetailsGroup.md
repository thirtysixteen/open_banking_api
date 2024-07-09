# OpenBanking::LoanPaymentDetailsGroup

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** | An account ID |  |
| **group_number** | **String** | Institution&#39;s ID of the Student Loan Group |  |
| **group_payment_number** | **String** | The payment number given by the institution. This number is typically for manual payments. This is not an ACH payment number. |  |
| **group_payment_address** | **String** | The payment address to which send manual payments should be sent |  |
| **group_future_payoff_amount** | **Float** | The payoff amount for the group | [optional] |
| **group_future_payoff_date** | **Time** | The date to which the \&quot;Future Payoff Amount\&quot; applies | [optional] |
| **group_loan_detail** | [**Array&lt;LoanPaymentDetailsLoan&gt;**](LoanPaymentDetailsLoan.md) |  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::LoanPaymentDetailsGroup.new(
  account_id: 5011648377,
  group_number: 3210-Group A,
  group_payment_number: 00001234895413-A,
  group_payment_address: P.O. Box 123 Sioux Falls, IA 51054,
  group_future_payoff_amount: 7500,
  group_future_payoff_date: 2022-01-01T00:00Z,
  group_loan_detail: null
)
```

