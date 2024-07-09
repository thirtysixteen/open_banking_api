# OpenBanking::CashFlowTransactionAnalyticsAttributesLastTransactionDateInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date** | **String** | Date the deposit transaction was posted |  |
| **deposits_credits** | **Float** | Amount of transaction if deposit, otherwise null | [optional] |
| **withdrawals_debits** | **Float** | Amount of transaction if withdrawal, otherwise null | [optional] |
| **zero_amount_transaction** | **Float** | Amount of transaction if zero, otherwise null | [optional] |
| **transaction_description** | **String** | Description of transaction | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowTransactionAnalyticsAttributesLastTransactionDateInner.new(
  date: 2020-03-25,
  deposits_credits: 500,
  withdrawals_debits: 500,
  zero_amount_transaction: 0,
  transaction_description: VENMO            CASHOUT
)
```

