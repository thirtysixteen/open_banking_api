# OpenBanking::ObbCurrentReportRequestDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **report_begin_date** | **String** | Date from when the requested data is available | [optional] |
| **report_end_date** | **String** | Date to which the requested data is available | [optional] |
| **report_request_date** | **String** | The date and time the report was requested |  |
| **requested_days_for_report** | **Integer** | Number of days requested for the report |  |
| **requested_report_begin_date** | **String** | Date the report would have begun on if enough data was available for which the partner requested |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbCurrentReportRequestDetails.new(
  report_begin_date: 2022-03-01,
  report_end_date: 2022-03-30,
  report_request_date: 2022-03-30T14:47:19-07:00,
  requested_days_for_report: 90,
  requested_report_begin_date: 2022-01-01
)
```

