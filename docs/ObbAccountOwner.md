# OpenBanking::ObbAccountOwner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address** | **String** | Address of the owner on record for the account |  |
| **name** | **String** | Name of the owner on record for the account |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbAccountOwner.new(
  address: 123 Main St, Portland, OR 12345,
  name: Johnny Appleseed
)
```

