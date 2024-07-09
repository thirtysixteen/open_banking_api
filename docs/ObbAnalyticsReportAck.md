# OpenBanking::ObbAnalyticsReportAck

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_ids** | **Array&lt;Integer&gt;** | List of account IDs included in the report |  |
| **business_id** | **Integer** | Business ID associated with the requested customer | [optional] |
| **created_date** | **String** | Created date of balance analytics request |  |
| **customer_id** | **Integer** | A customer ID represented as a number. See Add Customer API for how to create a customer ID. |  |
| **report_id** | **String** | A report ID |  |
| **report_pin** | **String** | PIN that may be used to access the report |  |
| **requester_name** | **String** | Name of requester | [optional] |
| **title** | **String** | Title of the report |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbAnalyticsReportAck.new(
  account_ids: null,
  business_id: 1005061234,
  created_date: 2023-05-17T06:48:22-07:00,
  customer_id: 1005061234,
  report_id: u4hstnnak45g,
  report_pin: qert,
  requester_name: Mortgage ABC LLC,
  title: Finicity Asset Ready Report (CRA)
)
```

