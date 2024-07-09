# OpenBanking::NewAddress

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address_line1** | **String** | Address line 1 | [optional] |
| **address_line2** | **String** | Address line 2 | [optional] |
| **city** | **String** | City | [optional] |
| **state** | **String** | State | [optional] |
| **country** | **String** | Two-letter ISO 3166-1 alpha-2 country code | [optional] |
| **postal_code** | **String** | A ZIP code | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::NewAddress.new(
  address_line1: 434 W Ascension Way,
  address_line2: Suite #200,
  city: Murray,
  state: UT,
  country: US,
  postal_code: 84123
)
```

