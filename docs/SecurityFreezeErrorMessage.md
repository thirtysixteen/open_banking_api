# OpenBanking::SecurityFreezeErrorMessage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **Integer** | An error code for security freeze. Useful links: [API Errors](https://developer.mastercard.com/open-banking-us/documentation/errors/), [Aggregation Status Codes](https://developer.mastercard.com/open-banking-us/documentation/products/manage/aggregation-status-codes/). |  |
| **status** | **String** | A status code | [optional] |
| **message** | **String** | An error message |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::SecurityFreezeErrorMessage.new(
  code: 10405,
  status: 403,
  message: The active security freeze for this consumer exists.
)
```

