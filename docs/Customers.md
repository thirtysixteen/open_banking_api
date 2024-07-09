# OpenBanking::Customers

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **found** | **Integer** | The total number of results matching search criteria | [optional] |
| **displaying** | **Integer** | The number of results returned |  |
| **more_available** | **Boolean** | If the value of &#x60;moreAvailable&#x60; is \&quot;true\&quot;, you can retrieve the next page of results by increasing the value of the start parameter in your next request:\&quot;...&amp;start&#x3D;6&amp;limit&#x3D;5\&quot; |  |
| **customers** | [**Array&lt;Customer&gt;**](Customer.md) | A list of customer records |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Customers.new(
  found: 200,
  displaying: 1,
  more_available: true,
  customers: null
)
```

