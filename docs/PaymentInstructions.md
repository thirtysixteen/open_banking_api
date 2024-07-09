# OpenBanking::PaymentInstructions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payment_instruction** | [**Array&lt;PaymentInstruction&gt;**](PaymentInstruction.md) | List of payment instructions | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PaymentInstructions.new(
  payment_instruction: null
)
```

