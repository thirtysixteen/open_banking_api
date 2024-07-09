# OpenBanking::PayrollReportConstraints

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payroll_data** | [**PayrollData**](PayrollData.md) |  |  |
| **report_custom_fields** | [**Array&lt;ReportCustomField&gt;**](ReportCustomField.md) | The &#x60;reportCustomFields&#x60; parameter is used when experiences are associated with a credit decisioning report.  Designate up to 5 custom fields that you&#39;d like associated with the report when it&#39;s generated. Every custom field consists of three variables: &#x60;label&#x60;, &#x60;value&#x60;, and &#x60;shown&#x60;. The &#x60;shown&#x60; variable is \&quot;true\&quot; or \&quot;false\&quot;. * \&quot;true\&quot;: (default) display the custom field in the PDF report * \&quot;false\&quot;: don&#39;t display the custom field in the PDF report  For an experience that generates multiple reports, the &#x60;reportCustomFields&#x60; parameter gets passed to all reports.  All custom fields display in the Reseller Billing API. | [optional] |
| **pay_statements_from_date** | **Integer** | Limits the pay statement history in the VOIE - Payroll report income record. Pay statements are only included if the payDate of the statement is equal to or greater than the start date requested. Date should be in Unix epoch time (in seconds). See: Handling Epoch Dates and Times. | [optional] |
| **market_segment** | **String** | Use case for requesting the consumer&#39;s data. Current supported enumerations are \&quot;Mortgage\&quot; and \&quot;KYC\&quot;. If your use case doesn&#39;t match one of these please reach out to your technical point of contact. | [optional] |
| **exclude_emp_info** | **Boolean** | Only used on an exception basis for clients that need to exclude EmpInfo data from the VOE-Payroll or VOIE-Payroll report. If true is passed EmpInfo payroll provider&#39;s data will not be searched or returned. | [optional] |
| **purpose** | **String** | FCRA required 2-digit Permissible Purpose Code, specifying the reason for retrieving this report. | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PayrollReportConstraints.new(
  payroll_data: null,
  report_custom_fields: null,
  pay_statements_from_date: 1607450357,
  market_segment: Mortgage,
  exclude_emp_info: false,
  purpose: 31
)
```

