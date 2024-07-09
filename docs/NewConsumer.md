# OpenBanking::NewConsumer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **first_name** | **String** | The first name of the account holder |  |
| **last_name** | **String** | The last name of the account holder |  |
| **address** | **String** | A street address |  |
| **city** | **String** | City |  |
| **state** | **String** | State |  |
| **zip** | **String** | A ZIP code |  |
| **phone** | **String** | A phone number (max length 15). |  |
| **ssn** | **String** | A full SSN with or without hyphens |  |
| **birthday** | [**Birthday**](Birthday.md) |  |  |
| **email** | **String** | An email address | [optional] |
| **suffix** | **String** | A generational or academic suffix | [optional] |
| **end_user** | [**ConsumerEndUser**](ConsumerEndUser.md) |  | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::NewConsumer.new(
  first_name: John,
  last_name: Smith,
  address: 434 W Ascension Way Suite #200 Murray UT 84123,
  city: Murray,
  state: UT,
  zip: 84123,
  phone: 1-801-984-4200,
  ssn: 999-99-9999,
  birthday: null,
  email: myname@mycompany.com,
  suffix: PhD,
  end_user: null
)
```

