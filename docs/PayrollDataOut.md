# OpenBanking::PayrollDataOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payroll_data_retrieval_id** | **String** | An ID to identify the data retrieved from the payroll providers for the report. | [optional] |
| **payroll_aggregator_response_id** | **String** | An ID to identify the data retrieved from the payroll providers for the report. | [optional] |
| **consent_method** | **String** | Client-collected consent payroll report tagging. | [optional] |
| **employment_ids** | **Array&lt;String&gt;** | An array of employmentIds | [optional] |
| **payroll_account_ids** | **Array&lt;String&gt;** | An array of payrollAccountIds | [optional] |
| **report_id** | **String** | A report ID | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PayrollDataOut.new(
  payroll_data_retrieval_id: hahvhe2k0000,
  payroll_aggregator_response_id: hahvhe2k0000,
  consent_method: Written Generic - Finicity Set,
  employment_ids: null,
  payroll_account_ids: null,
  report_id: u4hstnnak45g
)
```

