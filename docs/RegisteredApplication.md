# OpenBanking::RegisteredApplication

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pre_app_id** | **Integer** | Identifier to track the application registration from the App Registration and Get App Registration Status APIs, represented as a number |  |
| **status** | **String** | The status of an app registration request. \&quot;A\&quot; means approved. \&quot;P\&quot; means pending which is the status when initially submitted or when the app is modified and awaiting approval. \&quot;R\&quot; means rejected. If it is rejected there will be a note with the rejected reason. |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::RegisteredApplication.new(
  pre_app_id: 2581,
  status: P
)
```

