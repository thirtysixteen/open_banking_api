# OpenBanking::ReportTransactionBase2

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **normalized_payee** | **String** | A normalized payee, derived from the transaction&#39;s &#x60;description&#x60; and &#x60;memo&#x60; fields | [optional] |
| **institution_transaction_id** | **String** | The unique identifier given by the FI for each transaction | [optional] |
| **category** | **String** | One of the values from Categories (assigned based on the payee name) | [optional] |
| **type** | **String** | One of the values from transaction types | [optional] |
| **security_type** | **String** | The type of investment security (VOA only) | [optional] |
| **symbol** | **String** | Investment symbol (VOA only) | [optional] |
| **commission** | **Float** | A commission amount | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ReportTransactionBase2.new(
  normalized_payee: T-Mobile,
  institution_transaction_id: 0000000000,
  category: Income,
  type: debit,
  security_type: Stock,
  symbol: DAL,
  commission: 0
)
```

