# OpenBanking::PartnerCredentialsWithNewSecret

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **partner_id** | **String** | Your Partner ID displayed in the [Developer Dashboard](https://developer.mastercard.com/account/log-in) |  |
| **partner_secret** | **String** | Your Partner Secret displayed in the [Developer Dashboard](https://developer.mastercard.com/account/log-in) |  |
| **new_partner_secret** | **String** | A new value for the Partner Secret |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PartnerCredentialsWithNewSecret.new(
  partner_id: 1234583871234,
  partner_secret: aqJ5Ic4SEVx2IgDQ6oR4,
  new_partner_secret: OrU7tjiA3tIspCgb85xV
)
```

