# OpenBanking::PayrollEmployeeRecord

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Full name of the employee: first, middle (if stated), and last name |  |
| **given_name** | **String** | First name of employee | [optional] |
| **middle_name** | **String** | Middle name of employee, if stated | [optional] |
| **family_name** | **String** | Last name of employee | [optional] |
| **address** | [**Array&lt;PayrollEmployeeAddress&gt;**](PayrollEmployeeAddress.md) | Array of addresses | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PayrollEmployeeRecord.new(
  name: John Doe Smith,
  given_name: John,
  middle_name: Doe,
  family_name: Smith,
  address: null
)
```

