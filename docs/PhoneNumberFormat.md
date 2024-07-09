# OpenBanking::PhoneNumberFormat

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **country_code** | **String** | The country code digit representing the phone number for specific country | [optional] |
| **phone_no** | **String** | A phone number ([E.164](https://en.wikipedia.org/wiki/E.164) format) minLength: 7 | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PhoneNumberFormat.new(
  country_code: 1,
  phone_no: 8042221111
)
```

