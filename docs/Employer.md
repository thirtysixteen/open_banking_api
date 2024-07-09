# OpenBanking::Employer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of the employer | [optional] |
| **address1** | **String** | Employer address as stated by the employer in the payroll system | [optional] |
| **address2** | **String** | Employer address as stated by the employer in the payroll system | [optional] |
| **city** | **String** | Employer city as stated by the employer in the payroll system | [optional] |
| **state** | **String** | Employer state as stated by the employer in the payroll system | [optional] |
| **zip** | **String** | Employer zip code as stated by the employer in the payroll system | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Employer.new(
  name: Rocket Surgery,
  address1: Address 1,
  address2: Address 2,
  city: City,
  state: TX,
  zip: 99999
)
```

