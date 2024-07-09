# OpenBanking::InstitutionResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **found** | **Integer** | The total number of results matching search criteria | [optional] |
| **displaying** | **Integer** | The number of results returned | [optional] |
| **more_available** | **Boolean** | If the value of &#x60;moreAvailable&#x60; is \&quot;true\&quot;, you can retrieve the next page of results by increasing the value of the start parameter in your next request:\&quot;...&amp;start&#x3D;6&amp;limit&#x3D;5\&quot; | [optional] |
| **institutions** | [**Array&lt;FinancialInstitution&gt;**](FinancialInstitution.md) | List of institution details for an application | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::InstitutionResponse.new(
  found: 200,
  displaying: 1,
  more_available: true,
  institutions: [{&quot;institutionId&quot;:170716,&quot;status&quot;:true,&quot;createdDate&quot;:&quot;2020-07-30T16:11:23Z&quot;,&quot;modifiedDate&quot;:&quot;2020-07-30T16:11:23Z&quot;}]
)
```

