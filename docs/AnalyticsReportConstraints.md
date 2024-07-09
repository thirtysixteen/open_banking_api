# OpenBanking::AnalyticsReportConstraints

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **analytics_report_data** | [**AnalyticsReportData**](AnalyticsReportData.md) |  | [optional] |
| **account_ids** | **String** | A whitespace-separated list of account IDs to be included in the report (all accounts will be included if not set) | [optional] |
| **report_custom_fields** | [**Array&lt;ReportCustomField&gt;**](ReportCustomField.md) | The &#x60;reportCustomFields&#x60; parameter is used when experiences are associated with a credit decisioning report.  Designate up to 5 custom fields that you&#39;d like associated with the report when it&#39;s generated. Every custom field consists of three variables: &#x60;label&#x60;, &#x60;value&#x60;, and &#x60;shown&#x60;. The &#x60;shown&#x60; variable is \&quot;true\&quot; or \&quot;false\&quot;. * \&quot;true\&quot;: (default) display the custom field in the PDF report * \&quot;false\&quot;: don&#39;t display the custom field in the PDF report  For an experience that generates multiple reports, the &#x60;reportCustomFields&#x60; parameter gets passed to all reports.  All custom fields display in the Reseller Billing API. | [optional] |
| **from_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AnalyticsReportConstraints.new(
  analytics_report_data: null,
  account_ids: 5011648377 5011648378 5011648379,
  report_custom_fields: null,
  from_date: 1607450357
)
```

