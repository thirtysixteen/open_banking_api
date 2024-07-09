# OpenBanking::ConnectEmailUrl

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **link** | **String** | A generated Connect URL |  |
| **email_config** | [**EmailOptions**](EmailOptions.md) |  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ConnectEmailUrl.new(
  link: https://connect2.finicity.com?customerId&#x3D;5025024821&amp;institutionId&#x3D;102105&amp;origin&#x3D;url&amp;partnerId&#x3D;2445583925753&amp;signature&#x3D;b5667164db7a9a0007b59267785c996ca3bc9ce97f2e72c98099cead76edfad9&amp;timestamp&#x3D;1648050761908&amp;ttl&#x3D;1648057961908&amp;type&#x3D;lite&amp;webhookContentType&#x3D;application%2Fjson,
  email_config: null
)
```

