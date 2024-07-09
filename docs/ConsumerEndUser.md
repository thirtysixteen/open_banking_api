# OpenBanking::ConsumerEndUser

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The first name of the account holder |  |
| **address** | **String** | Address line 1 |  |
| **city** | **String** | City |  |
| **state** | **String** | State |  |
| **zip** | **String** | A ZIP code |  |
| **phone** | **String** | A phone number (max length 15). |  |
| **email** | **String** | An email address | [optional] |
| **url** | **String** | Reseller end user URL |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ConsumerEndUser.new(
  name: John,
  address: 434 W Ascension Way,
  city: Murray,
  state: UT,
  zip: 84123,
  phone: 1-801-984-4200,
  email: myname@mycompany.com,
  url: testurl.com
)
```

