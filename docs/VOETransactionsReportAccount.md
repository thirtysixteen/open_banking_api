# OpenBanking::VOETransactionsReportAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The ID of the account | [optional] |
| **number** | **String** | The account number from the institution (all digits except the last four are obfuscated) | [optional] |
| **owner_name** | **String** | The name(s) of the account owner(s). If the owner information is not available, this field will not appear in the report. If the account has multiple owners then all owners will be listed separated by |. | [optional] |
| **owner_address** | **String** | The mailing address of the account owner(s). If the owner information is not available, this field will not appear in the report. If the account has multiple owners then the address of the primary owner will be listed. | [optional] |
| **name** | **String** | The account name from the institution | [optional] |
| **type** | **String** | The list of supported account types * &#x60;checking&#x60; * &#x60;savings&#x60; * &#x60;moneyMarket&#x60; | [optional] |
| **currency** | **String** | A currency code for account | [optional] |
| **aggregation_status_code** | **Integer** | The status of the most recent aggregation attempt | [optional] |
| **income_streams** | [**Array&lt;VOETransactionsReportIncomeStream&gt;**](VOETransactionsReportIncomeStream.md) | A list of income stream records | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::VOETransactionsReportAccount.new(
  id: 1000023996,
  number: 1111,
  owner_name: PATRICK PURCHASER|LORRAINE PURCHASER,
  owner_address: 7195 BELMONT ST. PARLIN, NJ 08859,
  name: Checking,
  type: checking,
  currency: USD,
  aggregation_status_code: 0,
  income_streams: null
)
```

