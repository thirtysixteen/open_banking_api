# OpenBanking::TransactionalAttribute

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **aggregated_by_time_periods** | [**Array&lt;TransactionalTimeInterval&gt;**](TransactionalTimeInterval.md) | List of aggregations by specified Time Interval |  |
| **attribute_name** | **String** | Name of Attribute as mentioned in Data Dictionary |  |
| **stream_ids** | **Array&lt;String&gt;** | List of stream IDs categorized as belonging to this attribute |  |
| **transaction_ids** | **Array&lt;String&gt;** | List of transaction IDs categorized as belonging to this attribute |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::TransactionalAttribute.new(
  aggregated_by_time_periods: null,
  attribute_name: INFLOW_TRANSACTIONS,
  stream_ids: [&quot;1&quot;,&quot;2&quot;],
  transaction_ids: [&quot;6010290887&quot;,&quot;6010290914&quot;]
)
```

