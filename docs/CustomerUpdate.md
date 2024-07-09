# OpenBanking::CustomerUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **first_name** | **String** | The first name of the account holder | [optional] |
| **last_name** | **String** | The last name of the account holder | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CustomerUpdate.new(
  first_name: John,
  last_name: Smith
)
```

