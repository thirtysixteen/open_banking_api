# OpenBanking::Birthday

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **year** | **Integer** | The birthday 4-digit year | [optional] |
| **month** | **Integer** | The birthday 2-digit month (1 is January) | [optional] |
| **day_of_month** | **Integer** | The birthday 2-digit day-of-month | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Birthday.new(
  year: 1989,
  month: 8,
  day_of_month: 13
)
```

