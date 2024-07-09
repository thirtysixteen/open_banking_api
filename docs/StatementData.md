# OpenBanking::StatementData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **Integer** | An account ID represented as a number |  |
| **statement_index** | **Integer** | Index of the statement to include in the report. Request statements from 1-24. By default, 1 is the most recent statement. Increase the index value to count back (by month) and retrieve its most recent statement. | [optional][default to 1] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::StatementData.new(
  account_id: 5011648377,
  statement_index: 1
)
```

