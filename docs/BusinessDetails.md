# OpenBanking::BusinessDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of a business |  |
| **address** | [**AFBusinessAddress**](AFBusinessAddress.md) |  |  |
| **business_id** | **String** | Unique identifier of the business | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::BusinessDetails.new(
  name: ABC Tires Inc,
  address: null,
  business_id: 1112
)
```

