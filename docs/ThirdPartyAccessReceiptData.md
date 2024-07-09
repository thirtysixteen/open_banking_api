# OpenBanking::ThirdPartyAccessReceiptData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **receipt** | [**ThirdPartyAccessReceipt**](ThirdPartyAccessReceipt.md) |  | [optional] |
| **proof** | [**ThirdPartyAccessProof**](ThirdPartyAccessProof.md) |  | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ThirdPartyAccessReceiptData.new(
  receipt: null,
  proof: null
)
```

