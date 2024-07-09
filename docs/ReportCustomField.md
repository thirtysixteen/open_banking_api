# OpenBanking::ReportCustomField

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **label** | **String** | The name of the custom field | [optional] |
| **value** | **String** | The value of the custom field | [optional] |
| **shown** | **Boolean** | If the custom field will show on the PDF or not | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ReportCustomField.new(
  label: loanID,
  value: 123456,
  shown: true
)
```

