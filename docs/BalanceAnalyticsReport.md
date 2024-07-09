# OpenBanking::BalanceAnalyticsReport

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_results** | [**Array&lt;BalanceAnalyticsAccountResult&gt;**](BalanceAnalyticsAccountResult.md) | Balance results per account | [optional] |
| **business_id** | **Integer** | Business ID | [optional] |
| **business_summary** | [**BalanceAnalyticsBusinessSummary**](BalanceAnalyticsBusinessSummary.md) |  | [optional] |
| **customer_id** | **Integer** | A customer ID represented as a number. See Add Customer API for how to create a customer ID. |  |
| **report_header** | [**ObbReportHeader**](ObbReportHeader.md) |  |  |
| **requester_name** | **String** | Name of requester | [optional] |
| **title** | **String** | Title of the report |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::BalanceAnalyticsReport.new(
  account_results: null,
  business_id: 4444,
  business_summary: null,
  customer_id: 1005061234,
  report_header: null,
  requester_name: Mortgage ABC LLC,
  title: Finicity Asset Ready Report (CRA)
)
```

