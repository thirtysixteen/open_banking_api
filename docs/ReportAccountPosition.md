# OpenBanking::ReportAccountPosition

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Float** | The id of the investment position | [optional] |
| **currency** | **String** | What currency the account operates in | [optional] |
| **symbol** | **String** | The investment position’s market ticker symbol | [optional] |
| **security_name** | **String** | The security name for the investment holding | [optional] |
| **units** | **Float** | The number of units of the holding | [optional] |
| **market_value** | **Float** | Market value of an investment position at the time of retrieval | [optional] |
| **current_price** | **Float** | The current price of the investment holding | [optional] |
| **security_type** | **Float** | Type of security of the investment position | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ReportAccountPosition.new(
  id: 637054,
  currency: USD,
  symbol: MCD,
  security_name: Common Stock,
  units: 5,
  market_value: 1403.55,
  current_price: 280.71,
  security_type: null
)
```

