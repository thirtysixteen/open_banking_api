# OpenBanking::InsufficientFundsTransaction

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Float** | Amount of the NSF transaction |  |
| **description** | **String** | Description of the transaction | [optional] |
| **memo** | **String** | Transaction memo | [optional] |
| **posted_date** | **String** | Posted date of the NSF transaction |  |
| **transaction_id** | **Integer** | Finicity transaction ID |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::InsufficientFundsTransaction.new(
  amount: -1.65,
  description: OVERDRAFT FEE,
  memo: NSF,
  posted_date: 2022-12-19,
  transaction_id: 23092384290
)
```

