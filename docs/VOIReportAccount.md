# OpenBanking::VOIReportAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The ID of the account | [optional] |
| **number** | **String** | The account number from the institution (all digits except the last four are obfuscated) | [optional] |
| **owner_name** | **String** | The name(s) of the account owner(s). If the owner information is not available, this field will not appear in the report. If the account has multiple owners then all owners will be listed separated by |. | [optional] |
| **owner_address** | **String** | The mailing address of the account owner(s). If the owner information is not available, this field will not appear in the report. If the account has multiple owners then the address of the primary owner will be listed. | [optional] |
| **name** | **String** | The account name from the institution | [optional] |
| **type** | **String** | The list of supported account types. * &#x60;checking&#x60; * &#x60;savings&#x60; * &#x60;moneyMarket&#x60; | [optional] |
| **currency** | **String** | A currency code for account | [optional] |
| **aggregation_status_code** | **Integer** | The status of the most recent aggregation attempt | [optional] |
| **income_streams** | [**Array&lt;VOIReportIncomeStream&gt;**](VOIReportIncomeStream.md) | A list of income stream records | [optional] |
| **balance** | **Float** | The cleared balance of the account as-of &#x60;balanceDate&#x60; | [optional] |
| **average_monthly_balance** | **Float** | The average monthly balance of this account | [optional] |
| **transactions** | [**Array&lt;ReportTransaction&gt;**](ReportTransaction.md) | a list of transaction records | [optional] |
| **available_balance** | **Float** | The available balance for the account | [optional] |
| **current_balance** | **Float** | Current balance of the account | [optional] |
| **beginning_balance** | **Float** | Beginning balance of account per the time period in the report | [optional] |
| **oldest_transaction_date** | **Integer** | The oldest transaction date of this account. | [optional] |
| **misc_deposits** | [**Array&lt;ReportTransaction&gt;**](ReportTransaction.md) | A list of miscellaneous deposits | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::VOIReportAccount.new(
  id: 1000023996,
  number: 1111,
  owner_name: PATRICK PURCHASER|LORRAINE PURCHASER,
  owner_address: 7195 BELMONT ST. PARLIN, NJ 08859,
  name: Checking,
  type: checking,
  currency: USD,
  aggregation_status_code: 0,
  income_streams: null,
  balance: 714.16,
  average_monthly_balance: 720.75,
  transactions: null,
  available_balance: 714.16,
  current_balance: 714.16,
  beginning_balance: 714.77,
  oldest_transaction_date: 1588350276,
  misc_deposits: null
)
```

