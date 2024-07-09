# OpenBanking::FinancialInstitution

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **institution_id** | **Integer** | The financial institution identification at Mastercard. | [optional] |
| **status** | **Boolean** | Application registration status against the financial institution. | [optional] |
| **created_date** | **String** | The application creation date and time at financial institutions are in ISO 8601 format. | [optional] |
| **modified_date** | **String** | The application modification date and time at financial institutions in ISO 8601 format. | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::FinancialInstitution.new(
  institution_id: 170716,
  status: true,
  created_date: 2020-07-30T16:11:23Z,
  modified_date: 2020-07-30T16:11:23Z
)
```

