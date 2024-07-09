# OpenBanking::DirectDeposit

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **fi_name** | **String** | The name of the institution | [optional] |
| **account_type_code** | **String** | Bank account type:  * &#x60;Checking&#x60;  * &#x60;Savings&#x60;  * &#x60;Loan&#x60;: Loan account employee choose to direct a portion of their net pay to help pay off a loan  | [optional] |
| **account_type_name** | **String** | The name of the Account | [optional] |
| **description** | **String** | Description of deposit | [optional] |
| **amount** | **Float** | Direct deposit amount | [optional] |
| **account_last_four** | **String** | Last four digits of the deposit account number | [optional] |
| **routing_number** | **String** | Routing number for the deposit account | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::DirectDeposit.new(
  fi_name: FinBank,
  account_type_code: Savings,
  account_type_name: Checking,
  description: Payroll,
  amount: 12.34,
  account_last_four: 3337,
  routing_number: 30207583
)
```

