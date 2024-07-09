# OpenBanking::BalanceAndCashFlowAnalyticsReportConstraints

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_ids** | **Array&lt;Integer&gt;** | The list of account IDs to include in the report. If omitted, all accounts on record for the customer will be used. | [optional] |
| **length_of_report** | **Integer** | Number of days to search for transactions. Must be one of 30, 90, 180, 270, 365, or 730. If omitted, defaults to 2 years from current time at which the request was received (730 days). | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::BalanceAndCashFlowAnalyticsReportConstraints.new(
  account_ids: null,
  length_of_report: 730
)
```

