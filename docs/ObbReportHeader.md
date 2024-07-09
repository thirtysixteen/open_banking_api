# OpenBanking::ObbReportHeader

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_address** | **String** | Business address line 1 | [optional] |
| **business_city** | **String** | Business address city | [optional] |
| **business_name** | **String** | Name of the business | [optional] |
| **business_state** | **String** | Business address state | [optional] |
| **business_zip** | **String** | Business address zip | [optional] |
| **reference_number** | **String** | Partner-provided reference number | [optional] |
| **report_date** | **String** | Date the report was requested |  |
| **report_id** | **String** | Generated unique report ID |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbReportHeader.new(
  business_address: 123 Main St,
  business_city: Portland,
  business_name: B&amp;G Construction,
  business_state: OR,
  business_zip: 12345,
  reference_number: 32asdfaasd0823,
  report_date: 2022-03-16T21:28:38-07:00,
  report_id: 8ff8b4b2-706f-45c3-8d66-857bdb516214
)
```

