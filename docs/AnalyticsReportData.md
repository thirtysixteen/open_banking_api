# OpenBanking::AnalyticsReportData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **for_cra_purpose** | **Boolean** | Field to indicate if the requested report is for CRA or NONCRA. For small business lending or other similar business use cases, pass the value as “true” for purposes of this field. |  |
| **applicant_is_personal_guarantor** | **Boolean** | Field to indicate if the business owner will personally guarantee the loan. If true, a consumer record will be required. | [optional] |
| **time_interval_types** | **Array&lt;String&gt;** | Requested time interval for attribute values. | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AnalyticsReportData.new(
  for_cra_purpose: true,
  applicant_is_personal_guarantor: true,
  time_interval_types: [&quot;MONTHLY_CALENDAR&quot;]
)
```

