# OpenBanking::AccountOwnerAddress

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **owner_address** | **String** | A street address | [optional] |
| **type** | **String** | The type of address location: * \&quot;Business\&quot; * \&quot;Home\&quot; * \&quot;Mailing\&quot; | [optional] |
| **line1** | **String** | Address line 1 | [optional] |
| **line2** | **String** | Address line 2 | [optional] |
| **line3** | **String** | Address line 3 | [optional] |
| **city** | **String** | City | [optional] |
| **state** | **String** | State | [optional] |
| **postal_code** | **String** | A ZIP code | [optional] |
| **country** | **String** | Country code is Iso3166-1 Alpha-2 code and Alpha 3 standard (max length 3). | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AccountOwnerAddress.new(
  owner_address: 434 W Ascension Way Suite #200 Murray UT 84123,
  type: Home,
  line1: 434 W Ascension Way,
  line2: Suite #200,
  line3: UT 84123,
  city: Murray,
  state: UT,
  postal_code: 84123,
  country: USA
)
```

