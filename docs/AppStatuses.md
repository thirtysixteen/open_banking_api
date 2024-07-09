# OpenBanking::AppStatuses

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **total_records** | **Integer** | The total number of results |  |
| **total_pages** | **Integer** | The total number of pages |  |
| **page_number** | **Integer** | The current page number |  |
| **number_of_records_per_page** | **Integer** | The number of results per page |  |
| **applications** | [**Array&lt;AppStatus&gt;**](AppStatus.md) | A list of applications with their statuses |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AppStatuses.new(
  total_records: 50,
  total_pages: 5,
  page_number: 2,
  number_of_records_per_page: 10,
  applications: null
)
```

