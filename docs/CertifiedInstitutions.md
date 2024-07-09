# OpenBanking::CertifiedInstitutions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **found** | **Integer** | The total number of results matching search criteria |  |
| **displaying** | **Integer** | The number of results returned |  |
| **more_available** | **Boolean** | If the value of &#x60;moreAvailable&#x60; is \&quot;true\&quot;, you can retrieve the next page of results by increasing the value of the start parameter in your next request:\&quot;...&amp;start&#x3D;6&amp;limit&#x3D;5\&quot; |  |
| **requested_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |
| **institutions** | [**Array&lt;CertifiedInstitution&gt;**](CertifiedInstitution.md) | A list of institutions |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CertifiedInstitutions.new(
  found: 200,
  displaying: 1,
  more_available: true,
  requested_date: 1607450357,
  institutions: null
)
```

