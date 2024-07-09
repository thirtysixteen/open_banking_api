# OpenBanking::AFBusiness

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of a business |  |
| **address** | [**AFBusinessAddress**](AFBusinessAddress.md) |  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AFBusiness.new(
  name: ABC Tires Inc,
  address: null
)
```

