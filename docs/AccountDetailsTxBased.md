# OpenBanking::AccountDetailsTxBased

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **interest_margin_balance** | **Float** | Only available for investment accounts. Net interest earned after deducting interest paid out. | [optional] |
| **available_cash_balance** | **Float** | Only available for investment accounts. Amount available for cash withdrawal. | [optional] |
| **vested_balance** | **Float** | Only available for investment accounts. Vested amount in account. | [optional] |
| **current_loan_balance** | **Float** | Only available for investment accounts. Current loan balance. | [optional] |
| **available_balance_amount** | **Float** | The available balance for the account | [optional] |
| **margin_balance** | **Float** | Net interest earned after deducting interest paid out | [optional] |
| **current_balance** | **Float** | Current balance | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AccountDetailsTxBased.new(
  interest_margin_balance: -50000,
  available_cash_balance: 1500,
  vested_balance: 300000,
  current_loan_balance: 0,
  available_balance_amount: 1000,
  margin_balance: 100.0,
  current_balance: 1000.0
)
```

