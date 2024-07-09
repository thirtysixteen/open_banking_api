# OpenBanking::DisputeStatementErrorMessage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **Integer** | An error code for dispute statement. Useful links: [API Errors](https://developer.mastercard.com/open-banking-us/documentation/errors/), [Aggregation Status Codes](https://developer.mastercard.com/open-banking-us/documentation/products/manage/aggregation-status-codes/). |  |
| **status** | **String** | A status code | [optional] |
| **message** | **String** | An error message |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::DisputeStatementErrorMessage.new(
  code: 10406,
  status: 403,
  message: The active dispute statement for this consumer exists.
)
```

