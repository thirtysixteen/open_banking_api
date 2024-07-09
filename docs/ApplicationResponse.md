# OpenBanking::ApplicationResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **found** | **Integer** | The total number of results matching search criteria | [optional] |
| **displaying** | **Integer** | The number of results returned | [optional] |
| **more_available** | **Boolean** | If the value of &#x60;moreAvailable&#x60; is \&quot;true\&quot;, you can retrieve the next page of results by increasing the value of the start parameter in your next request:\&quot;...&amp;start&#x3D;6&amp;limit&#x3D;5\&quot; | [optional] |
| **applications** | [**Array&lt;App&gt;**](App.md) | List of application details | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ApplicationResponse.new(
  found: 200,
  displaying: 1,
  more_available: true,
  applications: null
)
```

