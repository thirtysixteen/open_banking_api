# OpenBanking::InstitutionAddress

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **city** | **String** | City | [optional] |
| **state** | **String** | State | [optional] |
| **country** | **String** | Country code is Iso3166-1 Alpha-2 code and Alpha 3 standard (max length 3). | [optional] |
| **postal_code** | **String** | A ZIP code | [optional] |
| **address_line1** | **String** | Address line 1 | [optional] |
| **address_line2** | **String** | Address line 2 | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::InstitutionAddress.new(
  city: Murray,
  state: UT,
  country: USA,
  postal_code: 84123,
  address_line1: 434 W Ascension Way,
  address_line2: Suite #200
)
```

