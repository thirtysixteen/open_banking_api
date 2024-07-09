# OpenBanking::CashFlowMonthlyCashFlowCredits

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **month** | **Integer** | One instance for each complete calendar month in the report |  |
| **number_of_credits** | **String** | Number of credits by month |  |
| **total_credits_amount** | **Float** | Total amount of credits by month |  |
| **largest_credit** | **Float** | Largest credit by month |  |
| **number_of_credits_less_transfers** | **String** | Number of credits by month (less transfers) |  |
| **total_credits_amount_less_transfers** | **Float** | Total amount of credits by month (less transfers) |  |
| **average_credit_amount** | **Float** | The average credit amount |  |
| **estimated_number_of_loan_deposits** | **String** | The estimated number of loan deposits |  |
| **estimated_loan_deposit_amount** | **Float** | The estimated loan deposit amount |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowMonthlyCashFlowCredits.new(
  month: 1512111600,
  number_of_credits: 3,
  total_credits_amount: 5000,
  largest_credit: 2000,
  number_of_credits_less_transfers: 2,
  total_credits_amount_less_transfers: 4000,
  average_credit_amount: 500,
  estimated_number_of_loan_deposits: 0,
  estimated_loan_deposit_amount: 0
)
```

