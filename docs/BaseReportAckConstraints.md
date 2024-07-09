# OpenBanking::BaseReportAckConstraints

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **analytics_report_data** | [**AnalyticsReportData**](AnalyticsReportData.md) |  | [optional] |
| **account_ids** | **Array&lt;String&gt;** | An array of account IDs to be included in the report (all accounts will be included if not set) | [optional] |
| **report_custom_fields** | [**Array&lt;ReportCustomField&gt;**](ReportCustomField.md) | The &#x60;reportCustomFields&#x60; parameter is used when experiences are associated with a credit decisioning report.  Designate up to 5 custom fields that you&#39;d like associated with the report when it&#39;s generated. Every custom field consists of three variables: &#x60;label&#x60;, &#x60;value&#x60;, and &#x60;shown&#x60;. The &#x60;shown&#x60; variable is \&quot;true\&quot; or \&quot;false\&quot;. * \&quot;true\&quot;: (default) display the custom field in the PDF report * \&quot;false\&quot;: don&#39;t display the custom field in the PDF report  For an experience that generates multiple reports, the &#x60;reportCustomFields&#x60; parameter gets passed to all reports.  All custom fields display in the Reseller Billing API. | [optional] |
| **from_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **show_nsf** | **Boolean** | Include the non-sufficient funds (NSF) summary JSON and the NSF summary PDF section in the report. Data included: * Account  * Total number of NSF funds  * Days since the most recent NFS funds fee | [optional] |
| **income_stream_confidence_minimum** | **Integer** | Include income streams in the report, based on the income stream&#39;s confidence score. For example, Use the value 50 to include only income streams with a confidence score of 50 or higher. | [optional] |
| **voie_with_interview_data** | [**VOIEWithInterviewData**](VOIEWithInterviewData.md) |  |  |
| **voie_with_statement_data** | [**VOIEWithStatementData**](VOIEWithStatementData.md) |  |  |
| **statement_report_data** | [**StatementData**](StatementData.md) |  |  |
| **to_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **include_pending** | **Boolean** | If pending transactions must be included | [optional][default to false] |
| **voai_pdf_deposit_view** | **Boolean** | Provide an alternate PDF view of deposit transactions group by income stream in PDF. | [optional] |
| **payroll_data** | [**PayrollDataOut**](PayrollDataOut.md) |  |  |
| **pay_statements_from_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **report_id** | **String** | A report ID | [optional] |
| **paystatement_report** | [**PayStatementData**](PayStatementData.md) |  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::BaseReportAckConstraints.new(
  analytics_report_data: null,
  account_ids: [5011648377, 5011648378, 5011648379],
  report_custom_fields: null,
  from_date: 1607450357,
  show_nsf: false,
  income_stream_confidence_minimum: 50,
  voie_with_interview_data: null,
  voie_with_statement_data: null,
  statement_report_data: null,
  to_date: 1607450357,
  include_pending: true,
  voai_pdf_deposit_view: true,
  payroll_data: null,
  pay_statements_from_date: 1607450357,
  report_id: u4hstnnak45g,
  paystatement_report: null
)
```

