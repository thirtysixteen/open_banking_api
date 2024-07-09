# OpenBanking::CustomerAccountMultipleStatements

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **statements** | [**Array&lt;CustomerAccountMultipleStatement&gt;**](CustomerAccountMultipleStatement.md) | List of customer account statements |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CustomerAccountMultipleStatements.new(
  statements: [{&quot;index&quot;:&quot;1&quot;,&quot;id&quot;:&quot;a9e96186-2896-4a21-8759-450403dadf47-1063025272&quot;,&quot;asOfDate&quot;:1669036741,&quot;description&quot;:&quot;08/28/2020 - 09/27/2020&quot;,&quot;documentDate&quot;:&quot;2020-09-27&quot;},{&quot;index&quot;:&quot;2&quot;,&quot;asOfDate&quot;:1669036741,&quot;code&quot;:&quot;960&quot;,&quot;message&quot;:&quot;statement not found.&quot;}]
)
```

