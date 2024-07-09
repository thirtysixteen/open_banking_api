# OpenBanking::NewBusiness

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The legal name of the business |  |
| **personally_liable** | **Boolean** | Indicates whether a business owner is personally liable for a loan |  |
| **address** | [**NewAddress**](NewAddress.md) |  |  |
| **phone_number** | [**PhoneNumberFormat**](PhoneNumberFormat.md) |  |  |
| **url** | **String** | A URL for the business website | [optional] |
| **email** | **String** | An email address | [optional] |
| **type** | **String** | The business type eg LLC, Corp, S Corp, C Corp, B Corp, Sole Propriertorship, Nonprofit, etc. | [optional] |
| **tax_id** | **String** | Provide details of the tax id for the business | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::NewBusiness.new(
  name: ABC Tires Inc,
  personally_liable: true,
  address: null,
  phone_number: null,
  url: https://www.finicity.com/,
  email: myname@mycompany.com,
  type: Nonprofit,
  tax_id: A1234561Z
)
```

