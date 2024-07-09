# OpenBanking::PayrollData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ssn** | **String** | The consumer&#39;s full SSN without hyphens |  |
| **dob** | **Integer** | The consumer&#39;s date of birth in Unix epoch time (in seconds). See: Handling Epoch Dates and Times. The timestamp should be set at the start of day of birth. |  |
| **report_id** | **String** | The report ID of the original payroll report for refresh use cases. If used, only the employment records from the original report will be included in the refreshed report response. | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PayrollData.new(
  ssn: 999999999,
  dob: 1607450357,
  report_id: u4hstnnak45g-voiepayroll
)
```

