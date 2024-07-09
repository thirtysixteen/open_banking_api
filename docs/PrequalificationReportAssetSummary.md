# OpenBanking::PrequalificationReportAssetSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | The asset type: \&quot;checking\&quot;, \&quot;savings\&quot;, \&quot;moneyMarket\&quot;, \&quot;cd\&quot;, \&quot;investment\&quot; | [optional] |
| **available_balance** | **Float** | The available balance for the account | [optional] |
| **current_balance** | **Float** | The current balance of the account |  |
| **two_month_average** | **Float** | The two month average daily balance of the account |  |
| **six_month_average** | **Float** | The six month average daily balance of the account | [optional] |
| **beginning_balance** | **Float** | The beginning balance of the account per the time period of the report |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PrequalificationReportAssetSummary.new(
  type: checking,
  available_balance: 1000,
  current_balance: 1000,
  two_month_average: -1865.96,
  six_month_average: -7616.01,
  beginning_balance: -17795.6
)
```

