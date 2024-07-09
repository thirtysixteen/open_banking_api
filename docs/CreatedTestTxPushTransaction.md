# OpenBanking::CreatedTestTxPushTransaction

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | A transaction ID |  |
| **created_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CreatedTestTxPushTransaction.new(
  id: 21284820852,
  created_date: 1607450357
)
```

