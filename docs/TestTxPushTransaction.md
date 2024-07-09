# OpenBanking::TestTxPushTransaction

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Float** | The amount of the transaction |  |
| **description** | **String** | The description of the transaction |  |
| **status** | **String** | \&quot;active\&quot; or \&quot;pending\&quot; (optional) | [optional][default to &#39;active&#39;] |
| **posted_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **transaction_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::TestTxPushTransaction.new(
  amount: -4.25,
  description: a testing transaction description,
  status: pending,
  posted_date: 1607450357,
  transaction_date: 1607450357
)
```

