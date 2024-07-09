# OpenBanking::MicroDepositInitiation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **institution_login_id** | **String** | An institution login ID (from the account record) | [optional] |
| **receiver** | [**Receiver**](Receiver.md) |  |  |
| **callback_url** | **String** | A callback URL where to receive micro deposit notifications | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::MicroDepositInitiation.new(
  institution_login_id: 1007302745,
  receiver: null,
  callback_url: https://www.mydomain.com/listener
)
```

