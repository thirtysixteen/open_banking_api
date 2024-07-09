# OpenBanking::SubscriptionRecord

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | ID of a TxPush subscription |  |
| **account_id** | **Integer** | An account ID represented as a number |  |
| **type** | **String** | A TxPush subscription type (\&quot;account\&quot; or \&quot;transaction\&quot;) |  |
| **callback_url** | **String** | A callback URL where to receive TxPush notifications |  |
| **signing_key** | **String** | Signing key for events |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::SubscriptionRecord.new(
  id: 17554874,
  account_id: 5011648377,
  type: account,
  callback_url: https://www.mydomain.com/txpush/listener,
  signing_key: zg4U0v1IvTzFEHIXzJMxPHnfUwWZAMVpXrUuNuL9IvZI0QzkDdwp39IAKuNOFxOVqCOgHLMS1Zpe4ZL40NX83aJkqI6v0Ez5B7BLBtvr7Ag11kPH3uG1taTeOV0CTyI4LOg7ohSHn0DqaRu2aBq26KI90nYe0CecTCzzhu4yMXL43JV8YfydAexNdkzfg8tY44MlhBPUh2neHW2EFTT2ja4s4Ul10JgID03un8WBSrIm2adHw3QYJB4jk4k1e
)
```

