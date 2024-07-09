# OpenBanking::CustomerAccountPosition

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The ID of the investment position | [optional] |
| **description** | **String** | The description of the holding | [optional] |
| **symbol** | **String** | The investment position&#39;s market ticker symbol | [optional] |
| **units** | **Float** | The number of units of the holding | [optional] |
| **current_price** | **Float** | The current price of the investment holding | [optional] |
| **security_name** | **String** | The security name for the investment holding | [optional] |
| **transaction_type** | **String** | The transaction type of the holding, such as cash, margin, and more | [optional] |
| **market_value** | **Float** | Market value of an investment position at the time of retrieval | [optional] |
| **change_percent** | **Float** | The percent change in value since the previous day | [optional] |
| **daily_change** | **Float** | The value amount change since the previous day | [optional] |
| **cost_basis** | **Float** | The total cost of acquiring the security | [optional] |
| **hold_type** | **String** | The type of the holding | [optional] |
| **inv_security_type** | **String** | The security type for the investment holding | [optional] |
| **status** | **String** | The status of the holding | [optional] |
| **current_price_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **security_type** | **String** | Type of security for the investment position | [optional] |
| **mf_type** | **String** | Type of mutual fund, such as open ended | [optional] |
| **pos_type** | **String** | Fund type assigned by the FI (long or short) | [optional] |
| **total_gl_dollar** | **Float** | Total gain and loss of the position at the time of aggregation in dollars | [optional] |
| **total_gl_percent** | **Float** | Total gain and loss of the position at the time of aggregation in percentage | [optional] |
| **option_strike_price** | **Float** | The strike price of the option contract | [optional] |
| **option_type** | **String** | The type of option contract (PUT or CALL) | [optional] |
| **option_shares_per_contract** | **Float** | The number of shares per option contract | [optional] |
| **option_expire_date** | **Date** | Expiration date of option | [optional] |
| **fi_asset_class** | **String** | Financial Institution (FI) defined asset class (COMMON STOCK, COMNEQTY, EQUITY/STOCK, CMA-ISA, CONVERTIBLE PREFERREDS, CORPORATE BONDS, OTHER MONEY FUNDS, ALLOCATION FUNDS, CMA-TAXABLE, FOREIGNEQUITYADRS, COMMONSTOCK, PREFERRED STOCKS, STABLE VALUE, FOREIGN EQUITY ADRS) | [optional] |
| **asset_class** | **String** | An asset class is a grouping of comparable financial securities. These include equities (stocks), fixed income (bonds), and cash equivalent or money market instruments. (DOMESTICBOND, LARGESTOCK, INTLSTOCK, MONEYMRKT, OTHER) | [optional] |
| **currency_rate** | **Float** | Currency rate, ratio of currency to original currency | [optional] |
| **security_id** | **String** | The security ID of the transaction | [optional] |
| **security_id_type** | **String** | The security type. This field is related to the &#x60;securityId&#x60; field. Possible values: * \&quot;CUSIP\&quot;  * \&quot;ISIN\&quot;  * \&quot;SEDOL\&quot;  * \&quot;SICC\&quot;  * \&quot;VALOR\&quot;  * \&quot;WKN\&quot; | [optional] |
| **cost_basis_per_share** | **Float** | The per share cost of acquiring the security | [optional] |
| **sub_account_type** | **String** | The subaccount&#39;s type, such as cash | [optional] |
| **security_currency** | **String** | Symbol for the currency that the account is being converted into | [optional] |
| **today_gl_dollar** | **Float** | The current day&#39;s gain and loss of the position at the time of aggregation in dollars | [optional] |
| **today_gl_percent** | **Float** | The current day&#39;s gain and loss of the position at the time of aggregation in percentage | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CustomerAccountPosition.new(
  id: 454678080,
  description: DELTA AIR LINES INC,
  symbol: DAL,
  units: 6.537,
  current_price: 41.585,
  security_name: DELTA AIR LINES INC,
  transaction_type: Margin,
  market_value: 271.84,
  change_percent: 170.02,
  daily_change: 180.03,
  cost_basis: 190.01,
  hold_type: INVESTMENT,
  inv_security_type: OTHERINFO,
  status: A,
  current_price_date: 1607450357,
  security_type: Stock,
  mf_type: OPENEND,
  pos_type: Long,
  total_gl_dollar: 162742.9,
  total_gl_percent: 68.89,
  option_strike_price: 50,
  option_type: PUT,
  option_shares_per_contract: 100,
  option_expire_date: null,
  fi_asset_class: COMNEQTY,
  asset_class: INTLSTOCK,
  currency_rate: 1,
  security_id: 25400W102,
  security_id_type: CUSIP,
  cost_basis_per_share: 13.38,
  sub_account_type: CASH,
  security_currency: USD,
  today_gl_dollar: 16272.9,
  today_gl_percent: 18.89
)
```

