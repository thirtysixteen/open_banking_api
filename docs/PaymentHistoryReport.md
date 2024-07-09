# OpenBanking::PaymentHistoryReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **title** | **String** | Title of the report |  |
| **customer_id** | **Integer** | A customer ID represented as a number. See Add Customer API for how to create a customer ID. |  |
| **account_ids** | **Array&lt;Integer&gt;** | List of account IDs included in the report | [optional] |
| **business_id** | **Integer** | Business ID | [optional] |
| **requester_name** | **String** | Name of requester | [optional] |
| **report_header** | [**ObbReportHeader**](ObbReportHeader.md) | Customer and report metadata |  |
| **analytics** | [**PaymentHistoryAnalytics**](PaymentHistoryAnalytics.md) |  | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PaymentHistoryReport.new(
  title: Finicity Asset Ready Report (CRA),
  customer_id: 1005061234,
  account_ids: null,
  business_id: 4444,
  requester_name: Mortgage ABC LLC,
  report_header: null,
  analytics: null
)
```

