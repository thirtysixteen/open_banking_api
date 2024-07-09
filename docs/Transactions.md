# OpenBanking::Transactions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **found** | **Integer** | The total number of results matching search criteria |  |
| **displaying** | **Integer** | The number of results returned |  |
| **more_available** | **Boolean** | If the value of &#x60;moreAvailable&#x60; is \&quot;true\&quot;, you can retrieve the next page of results by increasing the value of the start parameter in your next request:\&quot;...&amp;start&#x3D;6&amp;limit&#x3D;5\&quot; |  |
| **from_date** | **Integer** | Value of the &#x60;fromDate&#x60; request parameter that generated this response |  |
| **to_date** | **Integer** | Value of the &#x60;toDate&#x60; request parameter that generated this response |  |
| **sort** | **String** | Value of the sort request parameter that generated this response |  |
| **transactions** | [**Array&lt;Transaction&gt;**](Transaction.md) | The array of transactions |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Transactions.new(
  found: 200,
  displaying: 1,
  more_available: true,
  from_date: 1607450357,
  to_date: 1607450357,
  sort: desc,
  transactions: null
)
```

