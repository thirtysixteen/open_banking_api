# OpenBanking::ThirdPartyAccessReceipt

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile** | **Integer** | Representation of the type of consent receipt | [optional] |
| **version** | **String** | A schema version of receipt | [optional] |
| **receipt_id** | **String** | This is officially the Consent Receipt ID, but is aliased as the Access Key ID. This is a unique identifier managed by Finicity that points to the contents of this JSON document. | [optional] |
| **customer_id** | **String** | This is recipient&#39;s customerId represented as a pseudo identifier | [optional] |
| **partner_id** | **String** | Your Partner ID displayed in the [Developer Dashboard](https://developer.mastercard.com/account/log-in) | [optional] |
| **products** | [**Array&lt;ThirdPartyAccessProduct&gt;**](ThirdPartyAccessProduct.md) |  | [optional] |
| **provenance** | [**ThirdPartyAccessProvenance**](ThirdPartyAccessProvenance.md) |  | [optional] |
| **timestamp** | **Time** | A date-time with time zone | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ThirdPartyAccessReceipt.new(
  profile: 3,
  version: 1,
  receipt_id: cr_4pfI2r1X8aOHrDDwrwC01NHTxOXlT1,
  customer_id: 3465230025077724000,
  partner_id: 1234583871234,
  products: null,
  provenance: null,
  timestamp: 2022-03-10T06:06:20.042584549Z
)
```

