# OpenBanking::ThirdPartyAccessPeriod

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Multiple types will be supported. Presently below types are supported. * \&quot;timeframe\&quot;: Specifies a timeframe bounded by a startTime and endTime.   The startTime is the time at which the access was granted and the access key generated,   and the endTime is the time at which the access was revoked. Times are represented in ISO 8601 format(\&quot;2022-03-10T06:06:20Z\&quot;) |  |
| **start_time** | **Time** | A date-time with time zone |  |
| **end_time** | **Time** | A date-time with time zone |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ThirdPartyAccessPeriod.new(
  type: timeframe,
  start_time: 2022-03-10T06:06:20.042584549Z,
  end_time: 2022-03-10T06:06:20.042584549Z
)
```

