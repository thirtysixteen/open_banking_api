# OpenBanking::Earnings

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Where available, the employer description of earnings on the paycheck | [optional] |
| **type** | **String** | Categorization of the earnings:  * &#x60;base&#x60;  * &#x60;bonus&#x60;  * &#x60;overtime&#x60;  * &#x60;commission&#x60;  * &#x60;tips&#x60;  * &#x60;other&#x60;  |  |
| **rate** | **Float** | Rate of pay | [optional] |
| **amount** | **Float** | Earnings amount for each earning type |  |
| **amount_ytd** | **Float** | Earnings YTD amount if available | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Earnings.new(
  name: bonusPayAmount,
  type: bonus,
  rate: 19,
  amount: 589,
  amount_ytd: 14301.25
)
```

