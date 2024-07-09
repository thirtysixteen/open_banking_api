# OpenBanking::PaymentHistoryAccountSummaryAccountOwner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The full name of the account owner. Multiple account owners are returned in one string per the source data from the institution. |  |
| **address** | **String** | A street address |  |
| **city** | **String** | City | [optional] |
| **state** | **String** | State | [optional] |
| **zip** | **String** | A ZIP code | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PaymentHistoryAccountSummaryAccountOwner.new(
  name: John Smith, PhD,
  address: 434 W Ascension Way Suite #200 Murray UT 84123,
  city: Murray,
  state: UT,
  zip: 84123
)
```

