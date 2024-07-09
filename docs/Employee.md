# OpenBanking::Employee

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The name of the employee | [optional] |
| **address1** | **String** | Employee address as stated by the employer in the payroll system | [optional] |
| **address2** | **String** | Employee address as stated by the employer in the payroll system | [optional] |
| **city** | **String** | Employee city as stated by the employer in the payroll system | [optional] |
| **state** | **String** | Employee state as stated by the employer in the payroll system | [optional] |
| **zip** | **String** | Employee zip code as stated by the employer in the payroll system | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Employee.new(
  name: Patrick Purchaser,
  address1: Address 1,
  address2: Address 2,
  city: City,
  state: TX,
  zip: 99999
)
```

