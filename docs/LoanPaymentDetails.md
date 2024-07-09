# OpenBanking::LoanPaymentDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **loan_number** | **String** | The number of the specific loan under the account. |  |
| **loan_payment_number** | **String** | The payment number given by the institution. This number is typically for manual payments. This is not an ACH payment number. |  |
| **loan_payment_address** | **String** | The payment address to send manual payments to |  |
| **account_detail** | [**LoanPaymentDetailsAccount**](LoanPaymentDetailsAccount.md) |  | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::LoanPaymentDetails.new(
  loan_number: 123456789,
  loan_payment_number: 5231123456789,
  loan_payment_address: Heartland ECSI       PO Box 718       Wexford PA 15090,
  account_detail: null
)
```

