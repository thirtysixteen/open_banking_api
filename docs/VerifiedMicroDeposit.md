# OpenBanking::VerifiedMicroDeposit

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | Micro entries successful verification status | [optional] |
| **status_description** | **String** | Micro entries successful verification description | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::VerifiedMicroDeposit.new(
  status: Verified,
  status_description: Micro entries are successfully verified
)
```

