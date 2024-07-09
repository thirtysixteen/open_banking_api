# OpenBanking::AFBusinessAddress

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address_line1** | **String** | Address line 1 | [optional] |
| **address_line2** | **String** | Address line 2 | [optional] |
| **city** | **String** | City | [optional] |
| **state** | **String** | State | [optional] |
| **country** | **String** | Country code is Iso3166-1 Alpha-2 code and Alpha 3 standard (max length 3). | [optional] |
| **postal_code** | **String** | A ZIP code | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AFBusinessAddress.new(
  address_line1: 434 W Ascension Way,
  address_line2: Suite #200,
  city: Murray,
  state: UT,
  country: USA,
  postal_code: 84123
)
```

