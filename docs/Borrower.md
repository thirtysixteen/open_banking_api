# OpenBanking::Borrower

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID. See Add Customer API for how to create a customer ID. |  |
| **consumer_id** | **String** | A consumer ID. See Create Consumer API for how to create a consumer ID. |  |
| **type** | **String** | \&quot;primary\&quot; or \&quot;jointBorrower\&quot; |  |
| **optional_consumer_info** | [**ConsumerInfo**](ConsumerInfo.md) |  | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Borrower.new(
  customer_id: 1005061234,
  consumer_id: 0bf46322c167b562e6cbed9d40e19a4c,
  type: primary,
  optional_consumer_info: null
)
```

