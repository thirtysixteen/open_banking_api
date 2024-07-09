# OpenBanking::CreatedConsumer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A consumer ID. See Create Consumer API for how to create a consumer ID. | [optional] |
| **created_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **customer_id** | **Integer** | A customer ID represented as a number. See Add Customer API for how to create a customer ID. | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CreatedConsumer.new(
  id: 0bf46322c167b562e6cbed9d40e19a4c,
  created_date: 1607450357,
  customer_id: 1005061234
)
```

