# OpenBanking::ThirdPartyAccessProvenance

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **client_fingerprint** | **String** | Calling client identifier | [optional] |
| **ip_address** | **String** | Calling client IP address | [optional] |
| **token** | **String** | Calling client cookie | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ThirdPartyAccessProvenance.new(
  client_fingerprint: LU9ZYxcDNQCwEmAxH52XFzaRiGMAAAAABclSKxW5S9P8pUMDV4fbpg,
  ip_address: 8.8.8.8,
  token: P9YbR+srNVyQI35893d+BzPrhGMAAAAAuacVUt+3m4svbaFjVSbHEA&#x3D;&#x3D;
)
```

