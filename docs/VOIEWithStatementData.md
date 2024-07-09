# OpenBanking::VOIEWithStatementData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **asset_ids** | **Array&lt;String&gt;** | A list of pay statement asset IDs |  |
| **extract_earnings** | **Boolean** | Field to indicate whether to extract the earnings on all pay statements | [optional][default to true] |
| **extract_deductions** | **Boolean** | Field to indicate whether to extract the deductions on all pay statements | [optional][default to false] |
| **extract_direct_deposit** | **Boolean** | Field to indicate whether to extract the direct deposits on all pay statements | [optional][default to true] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::VOIEWithStatementData.new(
  asset_ids: null,
  extract_earnings: true,
  extract_deductions: true,
  extract_direct_deposit: true
)
```

