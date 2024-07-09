# OpenBanking::ThirdPartyAccessKeyData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID. See Add Customer API for how to create a customer ID. |  |
| **partner_id** | **String** | Your Partner ID displayed in the [Developer Dashboard](https://developer.mastercard.com/account/log-in) |  |
| **third_party_partner_id** | **String** | Your Partner ID displayed in the [Developer Dashboard](https://developer.mastercard.com/account/log-in) |  |
| **provenance** | [**ThirdPartyAccessProvenance**](ThirdPartyAccessProvenance.md) |  | [optional] |
| **products** | [**Array&lt;ThirdPartyAccessProduct&gt;**](ThirdPartyAccessProduct.md) |  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ThirdPartyAccessKeyData.new(
  customer_id: 1005061234,
  partner_id: 1234583871234,
  third_party_partner_id: 1234583871234,
  provenance: null,
  products: null
)
```

