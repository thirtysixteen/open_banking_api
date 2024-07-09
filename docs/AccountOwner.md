# OpenBanking::AccountOwner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **owner_name** | **String** | The name of the account owner. Can be multiple account owners in one string. This is how the source data is returned from the institution. |  |
| **owner_address** | **String** | A street address |  |
| **as_of_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AccountOwner.new(
  owner_name: John Smith,
  owner_address: 434 W Ascension Way Suite #200 Murray UT 84123,
  as_of_date: 1607450357
)
```

