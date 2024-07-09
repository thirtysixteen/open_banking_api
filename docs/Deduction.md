# OpenBanking::Deduction

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | The normalized category of the deductions in the format [type][number]. The number is the will be the iterating number of the type&#39;s occurrence starting at one. | [optional] |
| **description** | **String** | The deduction line&#39;s deduction type description | [optional] |
| **amount_current** | **Float** | The amount for the deduction line deducted from employee&#39;s pay for the specified pay period | [optional] |
| **amount_ytd** | **Float** | The amount for the deduction line being deducted from the employee&#39;s pay for the current pay year | [optional] |
| **type** | **String** | Categorization based on the deduction line&#39;s description | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Deduction.new(
  name: 401,
  description: 401k,
  amount_current: 1744.61,
  amount_ytd: 1744.6,
  type: 401 Deductions
)
```

