# OpenBanking::MicroDepositVerification

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amounts** | **Array&lt;Float&gt;** | The list of amounts to be verified |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::MicroDepositVerification.new(
  amounts: [0.12,0.15]
)
```

