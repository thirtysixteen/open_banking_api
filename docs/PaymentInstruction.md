# OpenBanking::PaymentInstruction

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | The type of payment instruction: 1. ACH: when payment instruction type is ACH (Automated Clearing House) 2. RTP: when payment instruction type is RTP (Real-Time Payments) |  |
| **account_number** | **String** | The account number from the institution |  |
| **descriptors** | [**Array&lt;Descriptor&gt;**](Descriptor.md) | List of descriptors | [optional] |
| **transfer_in_enabled** | **Boolean** | Indicates whether transfer to this account is enabled or not. Applicable for \&quot;RTP\&quot; type only. | [optional] |
| **transfer_out_enabled** | **Boolean** | Indicates whether transfer from this account is enabled or not. Applicable for \&quot;RTP\&quot; type only. | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PaymentInstruction.new(
  type: ach,
  account_number: 124344454,
  descriptors: null,
  transfer_in_enabled: true,
  transfer_out_enabled: true
)
```

