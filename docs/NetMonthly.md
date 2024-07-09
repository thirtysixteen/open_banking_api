# OpenBanking::NetMonthly

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **month** | **Integer** | Timestamp for the first day of this month |  |
| **net** | **Float** | Total income during the given month, across all income streams |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::NetMonthly.new(
  month: 1522562400,
  net: 2004.77
)
```

