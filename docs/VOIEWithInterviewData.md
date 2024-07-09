# OpenBanking::VOIEWithInterviewData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tx_verify_interview** | [**Array&lt;TxVerifyInterview&gt;**](TxVerifyInterview.md) | An array of &#x60;TxVerifyInterview&#x60; objects |  |
| **extract_earnings** | **Boolean** | Field to indicate whether to extract the earnings on all pay statements | [optional][default to true] |
| **extract_deductions** | **Boolean** | Field to indicate whether to extract the deductions on all pay statements | [optional][default to false] |
| **extract_direct_deposit** | **Boolean** | Field to indicate whether to extract the direct deposits on all pay statements | [optional][default to true] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::VOIEWithInterviewData.new(
  tx_verify_interview: null,
  extract_earnings: true,
  extract_deductions: true,
  extract_direct_deposit: true
)
```

