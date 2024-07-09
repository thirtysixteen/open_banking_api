# OpenBanking::DirectDeposits

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_type_code** | **String** | Bank account type:  * &#x60;Checking&#x60;  * &#x60;Savings&#x60;  * &#x60;Loan&#x60;: Loan account employee choose to direct a portion of their net pay to help pay off a loan  | [optional] |
| **amount** | **Float** | Direct deposit amount | [optional] |
| **account_last_four** | **String** | Last four digits of the deposit account number | [optional] |
| **routing_number** | **String** | Routing number for the deposit account | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::DirectDeposits.new(
  account_type_code: Savings,
  amount: 12.34,
  account_last_four: 3337,
  routing_number: 30207583
)
```

