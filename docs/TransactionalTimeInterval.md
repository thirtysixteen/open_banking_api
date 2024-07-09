# OpenBanking::TransactionalTimeInterval

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **periods** | [**Array&lt;TransactionalPeriod&gt;**](TransactionalPeriod.md) | Periods of the specified time interval type, describing the attribute calculations |  |
| **time_interval_type** | **String** | Possible values for strategies in which attributes may be aggregated and reported across varying time intervals. Allowed Values - MONTHLY_CALENDAR - MONTHLY_ROLLING_30 | [default to &#39;MONTHLY_CALENDAR&#39;] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::TransactionalTimeInterval.new(
  periods: null,
  time_interval_type: MONTHLY_CALENDAR
)
```

