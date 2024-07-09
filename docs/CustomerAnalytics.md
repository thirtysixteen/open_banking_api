# OpenBanking::CustomerAnalytics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **transactional_attributes** | [**Array&lt;TransactionalAttribute&gt;**](TransactionalAttribute.md) | List of calculated transactional attributes |  |
| **state_attributes** | [**Array&lt;StateAttribute&gt;**](StateAttribute.md) | List of calculated state attributes |  |
| **streams** | [**Array&lt;StreamModel&gt;**](StreamModel.md) | List of generated streams |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CustomerAnalytics.new(
  transactional_attributes: null,
  state_attributes: null,
  streams: null
)
```

