# OpenBanking::TxPushSubscriptionParameters

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **callback_url** | **String** | A callback URL where to receive TxPush notifications |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::TxPushSubscriptionParameters.new(
  callback_url: https://www.mydomain.com/txpush/listener
)
```

