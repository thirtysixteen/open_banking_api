# OpenBanking::ReportTransaction

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | A transaction ID |  |
| **amount** | **Float** | The total amount of the transaction. Transactions for deposits are positive values, withdrawals and debits are negative values. | [optional] |
| **posted_date** | **Integer** | A timestamp showing when the transaction was posted or cleared by the institution |  |
| **description** | **String** | The description of the transaction, as provided by the institution (often known as &#x60;payee&#x60;). In the event that this field is left blank by the institution, Finicity will pass a value of \&quot;No description provided by institution\&quot;. All other values are provided by the institution. |  |
| **memo** | **String** | The memo field of the transaction, as provided by the institution. The institution must provide either a description, a memo, or both. It is recommended to concatenate the two fields into a single value. | [optional] |
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

instance = OpenBanking::ReportTransaction.new(
  id: 21284820852,
  amount: 100,
  posted_date: 1571313600,
  description: ATM CHECK DEPOSIT mm/dd,
  memo: Some St Somewhere City State,
  normalized_payee: T-Mobile,
  institution_transaction_id: 0000000000,
  category: Income,
  type: debit,
  security_type: Stock,
  symbol: DAL,
  commission: 0
)
```

