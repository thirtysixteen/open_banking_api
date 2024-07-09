# OpenBanking::ConsumerInfo

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ssn** | **String** | The consumer&#39;s full SSN without hyphens |  |
| **dob** | **Integer** | The consumer&#39;s date of birth in Unix epoch time (in seconds). See: Handling Epoch Dates and Times. The timestamp should be set at the start of day of birth. | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ConsumerInfo.new(
  ssn: 999999999,
  dob: 1607450357
)
```

