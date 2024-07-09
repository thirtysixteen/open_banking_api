# OpenBanking::Transaction

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | A transaction ID |  |
| **amount** | **Float** | The total amount of the transaction. Transactions for deposits are positive values, withdrawals and debits are negative values. |  |
| **account_id** | **Integer** | An account ID represented as a number |  |
| **customer_id** | **Integer** | A customer ID represented as a number. See Add Customer API for how to create a customer ID. |  |
| **status** | **String** | One of \&quot;active\&quot;, \&quot;pending\&quot;, or \&quot;shadow\&quot; (see [Transaction Status](https://developer.mastercard.com/open-banking-us/documentation/products/manage/transaction-data/#transaction-status)) |  |
| **description** | **String** | The description value is from the financial institution (FI), often known as the payee. The value \&quot;No description provided by institution\&quot; is returned when the FI doesn&#39;t provide one |  |
| **memo** | **String** | The institution must provide either a description, a memo, or both. We recommended concatenating the two fields into a single value. | [optional] |
| **type** | **String** | If provided by the institution, the following values may be returned in the field of a record: * \&quot;atm\&quot;  * \&quot;cash\&quot;  * \&quot;check\&quot;  * \&quot;credit\&quot;  * \&quot;debit\&quot;  * \&quot;deposit\&quot;  * \&quot;directDebit\&quot;  * \&quot;directDeposit\&quot;  * \&quot;dividend\&quot;  * \&quot;fee\&quot;  * \&quot;interest\&quot;  * \&quot;other\&quot;  * \&quot;payment\&quot;  * \&quot;pointOfSale\&quot;  * \&quot;repeatPayment\&quot;  * \&quot;serviceCharge\&quot;  * \&quot;transfer\&quot; | [optional] |
| **transaction_date** | **Integer** | A date in Unix epoch time (in seconds). Represents the timestamp of the transaction when it occurred. See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **posted_date** | **Integer** | A date in Unix epoch time (in seconds). Represents the timestamp of the transaction when it was posted or cleared by the institution. This value isn&#39;t required for student loan transaction data. See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **created_date** | **Integer** | A date in Unix epoch time (in seconds). Represents the timestamp of the transaction when it was added to our platform. See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |
| **first_effective_date** | **Integer** | A date in Unix epoch time (in seconds). Represents the first timestamp of the transaction recorded in the &#x60;effectiveDate&#x60; field. See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **effective_date** | **Integer** | A date in Unix epoch time (in seconds). Represents the timestamp of the transaction when it became effective on an account by an institution. See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **option_expire_date** | **Integer** | A date in Unix epoch time (in seconds). Represents the timestamp of the transaction expiration date when it became expires on an account by an institution. See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **check_num** | **String** | The check number of the transaction | [optional] |
| **escrow_amount** | **Float** | The portion of the transaction allocated to escrow | [optional] |
| **fee_amount** | **Float** | The portion of the overall transaction amount applied to fees | [optional] |
| **suspense_amount** | **Float** | Temporarily hold funds if you overpay or underpay your monthly payment | [optional] |
| **interest_amount** | **Float** | The portion of the transaction allocated to interest | [optional] |
| **principal_amount** | **Float** | The portion of the transaction allocated to principal | [optional] |
| **option_strike_price** | **Float** | The strike price of the option contract | [optional] |
| **unit_quantity** | **Integer** | The number of units (individual shares) in the transaction | [optional] |
| **unit_price** | **Float** | Share price for the investment unit: stocks, mutual funds, ETFs | [optional] |
| **categorization** | [**Categorization**](Categorization.md) |  | [optional] |
| **running_balance_amount** | **Float** | The ending balance after the transaction was posted | [optional] |
| **subaccount_security_type** | **String** | The type of sub account the funds came from | [optional] |
| **commission_amount** | **Integer** | Transaction commission | [optional] |
| **ticker** | **String** | Ticker symbol for the investment related to the transaction | [optional] |
| **investment_transaction_type** | **String** | Keywords in the &#x60;description&#x60; and &#x60;memo&#x60; fields were used to translate investment transactions into these types.  Possible values: * \&quot;cancel\&quot;  * \&quot;purchaseToClose\&quot;  * \&quot;purchaseToCover\&quot;  * \&quot;contribution\&quot;  * \&quot;optionExercise\&quot;  * \&quot;optionExpiration\&quot;  * \&quot;fee\&quot;  * \&quot;soldToClose\&quot;  * \&quot;soldToOpen\&quot;  * \&quot;split\&quot;  * \&quot;transfer\&quot;  * \&quot;returnOfCapital\&quot;  * \&quot;income\&quot;  * \&quot;purchased\&quot;  * \&quot;sold\&quot;  * \&quot;dividendReinvest\&quot;  * \&quot;tax\&quot;  * \&quot;dividend\&quot;  * \&quot;reinvestOfIncome\&quot;  * \&quot;interest\&quot;  * \&quot;deposit\&quot;  * \&quot;otherInfo\&quot; | [optional] |
| **taxes_amount** | **Integer** | Taxes applicable to the investment trade | [optional] |
| **currency_symbol** | **String** | If the foreign amount value is present then this is the currency code of that foreign amount | [optional] |
| **income_type** | **String** | Capital gains applied in short, long, or miscellaneous terms for tax purposes | [optional] |
| **split_denominator** | **Float** | Denominator of the stock split for the transaction | [optional] |
| **split_numerator** | **Float** | Numerator of the stock split for the transaction | [optional] |
| **shares_per_contract** | **Float** | Shares per contract of the underlying stock option | [optional] |
| **sub_account_fund** | **String** | The sub account where the funds came from | [optional] |
| **security_id** | **String** | The security ID of the transaction | [optional] |
| **security_id_type** | **String** | The security type. This field is related to the &#x60;securityId&#x60; field. Possible values: * \&quot;CUSIP\&quot;  * \&quot;ISIN\&quot;  * \&quot;SEDOL\&quot;  * \&quot;SICC\&quot;  * \&quot;VALOR\&quot;  * \&quot;WKN\&quot; | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Transaction.new(
  id: 21284820852,
  amount: -828.9,
  account_id: 5011648377,
  customer_id: 1005061234,
  status: active,
  description: Buy Stock,
  memo: UWM HOLDINGS CORPORATION - CLASS A COMMON STOCK,
  type: atm,
  transaction_date: 1607450357,
  posted_date: 1607450357,
  created_date: 1607450357,
  first_effective_date: 1607450357,
  effective_date: 1607450357,
  option_expire_date: 1607450357,
  check_num: 299,
  escrow_amount: 2534,
  fee_amount: 0.51,
  suspense_amount: 0.25,
  interest_amount: 132,
  principal_amount: 32560,
  option_strike_price: 32560,
  unit_quantity: 150,
  unit_price: 5.53,
  categorization: null,
  running_balance_amount: 1000,
  subaccount_security_type: MARGIN,
  commission_amount: 0,
  ticker: UWMC,
  investment_transaction_type: transfer,
  taxes_amount: 0,
  currency_symbol: USD,
  income_type: DIV,
  split_denominator: 152,
  split_numerator: 20,
  shares_per_contract: 100,
  sub_account_fund: MARGIN,
  security_id: 91823B109,
  security_id_type: CUSIP
)
```

