# OpenBanking::ObbErrorMessage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **error_code** | **Integer** | Error code |  |
| **message** | **String** | Detailed reason about the source of the error |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbErrorMessage.new(
  error_code: 404,
  message: Customer Id does not exist
)
```

