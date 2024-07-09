# OpenBanking::StreamModel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **cadence** | **Integer** | Number of days that occur between each transaction in the stream |  |
| **id** | **String** | Stream Id assigned to identified Stream |  |
| **payee** | **String** | The party in the transaction that is receiving the funds |  |
| **payor** | **String** | The party in the transaction that is sending the funds |  |
| **recency** | **Integer** | Number of days since the last transaction occurred in the stream |  |
| **transaction_ids** | **Array&lt;String&gt;** | List of Transaction IDs that comprise the stream |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::StreamModel.new(
  cadence: 30,
  id: 1,
  payee: Walmart,
  payor: Elizabeth Johnson,
  recency: 2,
  transaction_ids: [&quot;6010290887&quot;,&quot;6010290914&quot;]
)
```

