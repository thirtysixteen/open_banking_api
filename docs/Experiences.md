# OpenBanking::Experiences

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | UUID that distinguishes each experience | [optional] |
| **app_name** | **String** | Your registered application name in our system | [optional] |
| **product_code** | **Array&lt;String&gt;** | A unique billing code assigned to each open banking product used by the customer, as detailed in their contract. | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Experiences.new(
  id: 84fd419a-1add-4bf4-961b-16e8285b3a92,
  app_name: Test Application Name,
  product_code: [&quot;ABC&quot;,&quot;AO&quot;]
)
```

