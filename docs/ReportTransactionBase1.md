# OpenBanking::ReportTransactionBase1

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | A transaction ID |  |
| **amount** | **Float** | The total amount of the transaction. Transactions for deposits are positive values, withdrawals and debits are negative values. | [optional] |
| **posted_date** | **Integer** | A timestamp showing when the transaction was posted or cleared by the institution |  |
| **description** | **String** | The description of the transaction, as provided by the institution (often known as &#x60;payee&#x60;). In the event that this field is left blank by the institution, Finicity will pass a value of \&quot;No description provided by institution\&quot;. All other values are provided by the institution. |  |
| **memo** | **String** | The memo field of the transaction, as provided by the institution. The institution must provide either a description, a memo, or both. It is recommended to concatenate the two fields into a single value. | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ReportTransactionBase1.new(
  id: 21284820852,
  amount: 100,
  posted_date: 1571313600,
  description: ATM CHECK DEPOSIT mm/dd,
  memo: Some St Somewhere City State
)
```

