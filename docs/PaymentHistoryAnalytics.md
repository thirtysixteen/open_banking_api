# OpenBanking::PaymentHistoryAnalytics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | Report status | [optional] |
| **risk_score** | **Float** | Calculated risk score | [optional] |
| **transaction_history** | **Integer** | Months of transactions | [optional] |
| **transactions_summary** | [**PaymentHistoryTransactionsSummary**](PaymentHistoryTransactionsSummary.md) |  | [optional] |
| **account_summaries** | [**Array&lt;PaymentHistoryAccountSummary&gt;**](PaymentHistoryAccountSummary.md) | Account-level summary of transactions | [optional] |
| **customer_summary_by_months** | [**Array&lt;PaymentHistoryCustomerMonthlySummary&gt;**](PaymentHistoryCustomerMonthlySummary.md) | Customer-level summary of transactions per month | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PaymentHistoryAnalytics.new(
  status: success,
  risk_score: 82.45,
  transaction_history: 12,
  transactions_summary: null,
  account_summaries: null,
  customer_summary_by_months: null
)
```

