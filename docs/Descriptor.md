# OpenBanking::Descriptor

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment Instruction Descriptor Type |  |
| **value** | **String** | Value that the Descriptor Type Holds |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Descriptor.new(
  type: routingNumber,
  value: 2434345
)
```

