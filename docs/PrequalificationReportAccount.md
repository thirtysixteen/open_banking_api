# OpenBanking::PrequalificationReportAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The ID of the account | [optional] |
| **number** | **String** | The account number from the institution (all digits except the last four are obfuscated) | [optional] |
| **owner_name** | **String** | The name(s) of the account owner(s). If the owner information is not available, this field will not appear in the report. If the account has multiple owners then all owners will be listed separated by |. | [optional] |
| **owner_address** | **String** | The mailing address of the account owner(s). If the owner information is not available, this field will not appear in the report. If the account has multiple owners then the address of the primary owner will be listed. | [optional] |
| **name** | **String** | The account name from the institution | [optional] |
| **type** | **String** | The list of supported account types. * &#x60;checking&#x60; * &#x60;savings&#x60; * &#x60;moneyMarket&#x60; * &#x60;cd&#x60; * &#x60;investment&#x60; * &#x60;investmentTaxDeferred&#x60; * &#x60;employeeStockPurchasePlan&#x60; * &#x60;ira&#x60; * &#x60;401k&#x60; * &#x60;roth&#x60; * &#x60;403b&#x60; * &#x60;529&#x60; * &#x60;rollover&#x60; * &#x60;ugma&#x60; * &#x60;utma&#x60; * &#x60;keogh&#x60; * &#x60;457&#x60; * &#x60;401a&#x60; * &#x60;brokerageAccount&#x60; * &#x60;educationSavings&#x60; * &#x60;healthSavingsAccount&#x60; * &#x60;nonTaxableBrokerageAccount&#x60; * &#x60;pension&#x60; * &#x60;profitSharingPlan&#x60; * &#x60;roth401k&#x60; * &#x60;sepIRA&#x60; * &#x60;simpleIRA&#x60; * &#x60;thriftSavingsPlan&#x60; * &#x60;variableAnnuity&#x60; | [optional] |
| **currency** | **String** | A currency code for account | [optional] |
| **aggregation_status_code** | **Integer** | The status of the most recent aggregation attempt | [optional] |
| **balance** | **Float** | The cleared balance of the account as-of &#x60;balanceDate&#x60; | [optional] |
| **balance_date** | **Integer** | A timestamp of the balance | [optional] |
| **available_balance** | **Float** | Available balance | [optional] |
| **average_monthly_balance** | **Float** | The average monthly balance of the account | [optional] |
| **tot_number_insufficient_funds_fee_debit_tx_account** | **Integer** | The count for the total number of insufficient funds transactions, based on the &#x60;fromDate&#x60; of the report | [optional] |
| **tot_number_insufficient_funds_fee_debit_tx_over6_months_account** | **Integer** | The total number of  insufficient funds fees for the account over six months | [optional] |
| **tot_number_days_since_most_recent_insufficient_funds_fee_debit_tx_account** | **Integer** | The total number of days since the most recent insufficient funds fee for the account | [optional] |
| **transactions** | [**Array&lt;ReportTransaction&gt;**](ReportTransaction.md) | a list of transaction records | [optional] |
| **asset** | [**PrequalificationReportAssetSummary**](PrequalificationReportAssetSummary.md) |  | [optional] |
| **details** | [**AccountDetails**](AccountDetails.md) |  | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PrequalificationReportAccount.new(
  id: 1000023996,
  number: 1111,
  owner_name: PATRICK PURCHASER|LORRAINE PURCHASER,
  owner_address: 7195 BELMONT ST. PARLIN, NJ 08859,
  name: Checking,
  type: checking,
  currency: USD,
  aggregation_status_code: 0,
  balance: 501.24,
  balance_date: 1588350276,
  available_balance: 1000,
  average_monthly_balance: 501.02,
  tot_number_insufficient_funds_fee_debit_tx_account: 0,
  tot_number_insufficient_funds_fee_debit_tx_over6_months_account: 0,
  tot_number_days_since_most_recent_insufficient_funds_fee_debit_tx_account: 120,
  transactions: null,
  asset: null,
  details: null
)
```

