# OpenBanking::CadenceDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start_date** | **Integer** | &#x60;postedDate&#x60; of the first deposit transaction | [optional] |
| **stop_date** | **Integer** | &#x60;postedDate&#x60; of the final deposit transaction (omitted if status is active) | [optional] |
| **days** | **Integer** | Number of days between the recurring deposits | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CadenceDetails.new(
  start_date: 1577986990,
  stop_date: 1587986990,
  days: 14
)
```

