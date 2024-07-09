# OpenBanking::PayrollEmployerAddress

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **address1** | **String** | Employer address as stated by the employer in the payroll system | [optional] |
| **city** | **String** | Employer city as stated by the employer in the payroll system | [optional] |
| **state** | **String** | Employer state as stated by the employer in the payroll system | [optional] |
| **zip** | **String** | Employer zip code as stated by the employer in the payroll system | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PayrollEmployerAddress.new(
  address1: Address 1,
  city: City,
  state: TX,
  zip: 99999
)
```

