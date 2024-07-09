# OpenBanking::CashFlowMonthlyCashFlowCreditSummaries

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **month** | **Integer** | One instance for each complete calendar month in the report |  |
| **number_of_credits** | **String** | Number of credits by month across all accounts |  |
| **total_credits_amount** | **Float** | Total amount of credits by month across all accounts |  |
| **largest_credit** | **Float** | Largest credit by month across all accounts |  |
| **number_of_credits_less_transfers** | **String** | Number of credits by month (less transfers) across all accounts |  |
| **total_credits_amount_less_transfers** | **Float** | Total amount of credits by month (less transfers) across all accounts |  |
| **average_credit_amount** | **Float** | The average credit amount |  |
| **estimated_number_of_loan_deposits** | **String** | The estimated number of loan deposits by month |  |
| **estimated_loan_deposit_amount** | **Float** | The estimated loan deposit amount by month |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowMonthlyCashFlowCreditSummaries.new(
  month: 1512111600,
  number_of_credits: 57,
  total_credits_amount: 3479.39,
  largest_credit: 3000.49,
  number_of_credits_less_transfers: 5,
  total_credits_amount_less_transfers: 25.46,
  average_credit_amount: 500,
  estimated_number_of_loan_deposits: 0,
  estimated_loan_deposit_amount: 0
)
```

