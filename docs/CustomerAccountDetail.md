# OpenBanking::CustomerAccountDetail

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **date_as_of** | **Integer** | (All Account Types) Most recent date of the following information. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **available_balance_amount** | **Float** | (Checking/Savings/CD/MoneyMarket) and (Mortgage/Loan) The available balance (typically the current balance with adjustments for any pending transactions) | [optional] |
| **open_date** | **Integer** | (Checking/Savings/CD/MoneyMarket) Date when account was opened. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **period_start_date** | **Integer** | (Checking/Savings/CD/MoneyMarket) Start date of period. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **period_end_date** | **Integer** | End date of period. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **period_interest_rate** | **Float** | (Checking/Savings/CD/MoneyMarket) The APY for the current period interest rate | [optional] |
| **period_deposit_amount** | **Float** | (Checking/Savings/CD/MoneyMarket) Amount deposited in period | [optional] |
| **period_interest_amount** | **Float** | (Checking/Savings/CD/MoneyMarket) Interest accrued during the current period | [optional] |
| **interest_ytd_amount** | **Float** | (Checking/Savings/CD/MoneyMarket) Interest accrued year-to-date | [optional] |
| **interest_prior_ytd_amount** | **Float** | (Checking/Savings/CD/MoneyMarket) Interest earned in prior year | [optional] |
| **maturity_date** | **Integer** | (Checking/Savings/CD/MoneyMarket) Maturity date of account type. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **interest_rate** | **String** | (Credit Card/Line Of Credit) and (Mortgage/Loan) The account&#39;s current interest rate | [optional] |
| **credit_available_amount** | **Float** | (Credit Card/Line Of Credit) The available credit (typically the credit limit minus the current balance) | [optional] |
| **credit_max_amount** | **Float** | (Credit Card/Line Of Credit) The account&#39;s credit limit | [optional] |
| **cash_advance_available_amount** | **Float** | (Credit Card/Line Of Credit) Currently available cash advance | [optional] |
| **cash_advance_max_amount** | **Float** | (Credit Card/Line Of Credit) Maximum cash advance amount | [optional] |
| **cash_advance_balance** | **Float** | (Credit Card/Line Of Credit) Balance of current cash advance | [optional] |
| **cash_advance_interest_rate** | **Float** | (Credit Card/Line Of Credit) Interest rate for cash advances | [optional] |
| **current_balance** | **Float** | (Credit Card/Line Of Credit) and (Investment) Current balance | [optional] |
| **payment_min_amount** | **Float** | (Credit Card/Line Of Credit) and (Mortgage/Loan) Minimum payment due | [optional] |
| **payment_due_date** | **Integer** | (Credit Card/Line Of Credit) Due date for the next payment. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **previous_balance** | **Float** | (Credit Card/Line Of Credit) Prior balance in last statement | [optional] |
| **statement_start_date** | **Integer** | (Credit Card/Line Of Credit) Start date of statement period. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **statement_end_date** | **Integer** | (Credit Card/Line Of Credit) End date of statement period. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **statement_purchase_amount** | **Float** | (Credit Card/Line Of Credit) Purchase amount of statement period | [optional] |
| **statement_finance_amount** | **Float** | (Credit Card/Line Of Credit) Finance amount of statement period | [optional] |
| **statement_credit_amount** | **Float** | (Credit Card/Line Of Credit) Credit amount applied in statement period | [optional] |
| **reward_earned_balance** | **Integer** | (Credit Card/Line Of Credit) Earned reward balance | [optional] |
| **past_due_amount** | **Float** | (Credit Card/Line Of Credit) Balance past due | [optional] |
| **last_payment_amount** | **Float** | (Credit Card/Line Of Credit) and (Mortgage/Loan) The amount received in the last payment | [optional] |
| **last_payment_date** | **Integer** | (Credit Card/Line Of Credit) The date of the last payment. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **statement_close_balance** | **Float** | (Credit Card/Line Of Credit) Balance of statement at close | [optional] |
| **term_of_ml** | **String** | (Mortgage/Loan) Length of loan in months | [optional] |
| **ml_holder_name** | **String** | (Mortgage/Loan) Holder of the mortgage or loan | [optional] |
| **description** | **String** | (Mortgage/Loan) Description of loan | [optional] |
| **late_fee_amount** | **Float** | (Mortgage/Loan) Late fee charged | [optional] |
| **payoff_amount** | **Float** | (Mortgage/Loan) The amount required to payoff the loan | [optional] |
| **payoff_amount_date** | **Integer** | (Mortgage/Loan) Date of final payment. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **original_maturity_date** | **Integer** | (Mortgage/Loan) Original date of loan maturity. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **principal_balance** | **Float** | (Mortgage/Loan) The principal balance | [optional] |
| **escrow_balance** | **Float** | (Mortgage/Loan) The escrow balance | [optional] |
| **interest_period** | **String** | (Mortgage/Loan) Period of interest | [optional] |
| **initial_ml_amount** | **Float** | (Mortgage/Loan) Original loan amount | [optional] |
| **initial_ml_date** | **Integer** | (Mortgage/Loan) Original date of loan. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **next_payment_principal_amount** | **Float** | (Mortgage/Loan) Amount towards principal in next payment | [optional] |
| **next_payment_interest_amount** | **Float** | (Mortgage/Loan) Amount of interest in next payment | [optional] |
| **next_payment** | **Float** | (Mortgage/Loan) Minimum payment due | [optional] |
| **next_payment_date** | **Integer** | (Mortgage/Loan) Due date for the next payment. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **last_payment_due_date** | **Integer** | (Mortgage/Loan) Due date of last payment. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **last_payment_receive_date** | **Integer** | (Mortgage/Loan) The date of the last payment. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **last_payment_principal_amount** | **Float** | (Mortgage/Loan) Amount towards principal in last payment | [optional] |
| **last_payment_interest_amount** | **Float** | (Mortgage/Loan) Amount of interest in last payment | [optional] |
| **last_payment_escrow_amount** | **Float** | (Mortgage/Loan) Amount towards escrow in last payment | [optional] |
| **last_payment_last_fee_amount** | **Float** | (Mortgage/Loan) Amount of last fee in last payment | [optional] |
| **last_payment_late_charge** | **Float** | (Mortgage/Loan) Amount of late charge in last payment | [optional] |
| **ytd_principal_paid** | **Float** | (Mortgage/Loan) Principal paid year-to-date | [optional] |
| **ytd_interest_paid** | **Float** | (Mortgage/Loan) Interest paid year-to-date | [optional] |
| **ytd_insurance_paid** | **Float** | (Mortgage/Loan) Insurance paid year-to-date | [optional] |
| **ytd_tax_paid** | **Float** | (Mortgage/Loan) Tax paid year-to-date | [optional] |
| **auto_pay_enrolled** | **Boolean** | (Mortgage/Loan) Enrolled in autopay (F/Y) | [optional] |
| **margin_allowed** | **Boolean** | Margin trading indicator (true / false) | [optional] |
| **cash_account_allowed** | **Boolean** | Cash account allowed indicator (true / false) | [optional] |
| **collateral** | **String** | (Mortgage/Loan) Collateral on loan | [optional] |
| **current_school** | **String** | (Mortgage/Loan) Current school | [optional] |
| **first_payment_date** | **Integer** | (Mortgage/Loan) First payment due date. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **first_mortgage** | **Boolean** | (Mortgage/Loan) First mortgage (F/Y) | [optional] |
| **loan_payment_freq** | **String** | (Mortgage/Loan) Frequency of payments (monthly, etc.) | [optional] |
| **original_school** | **String** | (Mortgage/Loan) Original school | [optional] |
| **recurring_payment_amount** | **Float** | (Mortgage/Loan) Recurring payment amount | [optional] |
| **lender** | **String** | (Mortgage/Loan) Owner of loan | [optional] |
| **ending_balance_amount** | **Float** | (Mortgage/Loan) Ending balance | [optional] |
| **loan_term_type** | **String** | (Mortgage/Loan) Type of loan term | [optional] |
| **payments_made** | **Integer** | (Mortgage/Loan) Number of payments made | [optional] |
| **balloon_amount** | **Float** | (Mortgage/Loan) Balloon payment amount | [optional] |
| **projected_interest** | **Float** | (Mortgage/Loan) Projected interest on the loan | [optional] |
| **interest_paid_ltd** | **Float** | (Mortgage/Loan) Interest paid since inception of loan (life to date) | [optional] |
| **interest_rate_type** | **String** | (Mortgage/Loan) Type of interest rate | [optional] |
| **loan_payment_type** | **String** | (Mortgage/Loan) Type of loan payment | [optional] |
| **repayment_plan** | **String** | (Mortgage/Loan) Type of repayment plan for the student loan | [optional] |
| **payments_remaining** | **Integer** | (Mortgage/Loan) Number of payments remaining before loan is paid off | [optional] |
| **margin_balance** | **Float** | (Investment) Net interest earned after deducting interest paid out | [optional] |
| **short_balance** | **Float** | (Investment) Sum of short balance | [optional] |
| **available_cash_balance** | **Float** | (Investment) Amount available for cash withdrawal | [optional] |
| **maturity_value_amount** | **Float** | (Investment) amount payable to an investor at maturity | [optional] |
| **vested_balance** | **Float** | (Investment) Vested amount in account | [optional] |
| **emp_match_amount** | **Float** | (Investment) Employer matched contributions | [optional] |
| **emp_pretax_contrib_amount** | **Float** | (Investment) Employer pretax contribution amount | [optional] |
| **emp_pretax_contrib_amount_ytd** | **Float** | (Investment) Employer pretax contribution amount year to date | [optional] |
| **contrib_total_ytd** | **Float** | (Investment) Total year to date contributions | [optional] |
| **cash_balance_amount** | **Float** | (Investment) Cash balance of account | [optional] |
| **pre_tax_amount** | **Float** | (Investment) Pre-tax amount of total balance | [optional] |
| **after_tax_amount** | **Float** | (Investment) After-tax amount of total balance | [optional] |
| **match_amount** | **Float** | (Investment) Amount matched | [optional] |
| **profit_sharing_amount** | **Float** | (Investment) Amount of balance for profit sharing | [optional] |
| **rollover_amount** | **Float** | (Investment) Amount of balance rolled over from original account (401k, etc.) | [optional] |
| **other_vest_amount** | **Float** | (Investment) Other vested amount | [optional] |
| **other_nonvest_amount** | **Float** | (Investment) Other nonvested amount | [optional] |
| **current_loan_balance** | **Float** | (Investment) Current loan balance | [optional] |
| **loan_rate** | **Float** | (Investment) Interest rate of loan | [optional] |
| **buy_power** | **Float** | (Investment) Money available to buy securities | [optional] |
| **rollover_ltd** | **Float** | (Investment) Life to date of money rolled over | [optional] |
| **loan_award_id** | **String** | (Student Loan) The federal unique loan identifying number | [optional] |
| **original_interest_rate** | **Float** | (Student Loan) The original interest rate to which the loan was disbursed, in APY | [optional] |
| **guarantor** | **String** | (Student Loan) The financial institution guarantor of the loan (who will pay the loan amount to the owner if the borrower defaults) | [optional] |
| **owner** | **String** | (Student Loan) Owner of the loan | [optional] |
| **interest_subsidy_type** | **String** | (Student Loan) The indication of the presence of an interest subsidy (i.e. subsidized) | [optional] |
| **interest_balance** | **Float** | (Student Loan) The total outstanding interest balance | [optional] |
| **remaining_term_of_ml** | **Float** | (Student Loan) The number of months still outstanding on a loan | [optional] |
| **initial_interest_rate** | **Float** | (Student Loan) Initial interest rate of loan | [optional] |
| **fees_balance** | **Float** | (Student Loan) The total outstanding fees balance | [optional] |
| **loan_ytd_interest_paid** | **Float** | (Student Loan) Loan interest paid year-to-date | [optional] |
| **loan_ytd_fees_paid** | **Float** | (Student Loan) Loan fees paid year-to-date | [optional] |
| **loan_ytd_principal_paid** | **Float** | (Student Loan) Loan principal paid year-to-date | [optional] |
| **loan_status** | **String** | (Student Loan) The repayment status phase (i.e. In School, Grace, Repayment, Deferment, Forbearance) | [optional] |
| **loan_status_start_date** | **Integer** | (Student Loan) The start date of the current status. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **loan_status_end_date** | **Integer** | (Student Loan) The end date of the current status. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **weighted_interest_rate** | **Float** | (Student Loan) The interest rate of multiple interest rates and balances at the group level, in APY | [optional] |
| **repayment_plan_start_date** | **Integer** | (Student Loan) The start date of the current repayment plan. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **repayment_plan_end_date** | **Integer** | (Student Loan) The end date of the current repayment plan. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **expected_payoff_date** | **Integer** | (Student Loan) The expected date of the payoff date. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **out_of_school_date** | **Integer** | (Student Loan) The date the borrower graduated or dropped below half-time enrollment in school. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **convert_to_repayment** | **Integer** | (Student Loan) The date the loan enters into repayment. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **days_delinquent** | **Integer** | (Student Loan) The number of days past a due date that a payment should have been made | [optional] |
| **total_principal_paid** | **Float** | (Student Loan) The total amount paid towards the principal balance | [optional] |
| **total_interest_paid** | **Float** | (Student Loan) The total amount paid towards interest | [optional] |
| **total_amount_paid** | **Float** | (Student Loan) The total amount paid | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CustomerAccountDetail.new(
  date_as_of: 1607450357,
  available_balance_amount: 5678.78,
  open_date: 1607450357,
  period_start_date: 1607450357,
  period_end_date: 1607450357,
  period_interest_rate: 13.245,
  period_deposit_amount: 2356.56,
  period_interest_amount: 1234.56,
  interest_ytd_amount: 1056.67,
  interest_prior_ytd_amount: 3056.79,
  maturity_date: 1607450357,
  interest_rate: 15.789,
  credit_available_amount: 3000,
  credit_max_amount: 7000,
  cash_advance_available_amount: 2000,
  cash_advance_max_amount: 3000,
  cash_advance_balance: 1000,
  cash_advance_interest_rate: 21.5,
  current_balance: 5789.34,
  payment_min_amount: 456.78,
  payment_due_date: 1607450357,
  previous_balance: 1234.56,
  statement_start_date: 1607450357,
  statement_end_date: 1607450357,
  statement_purchase_amount: 2345.9,
  statement_finance_amount: 156.78,
  statement_credit_amount: 345,
  reward_earned_balance: 500,
  past_due_amount: 3688.99,
  last_payment_amount: 567.89,
  last_payment_date: 1607450357,
  statement_close_balance: 2456.69,
  term_of_ml: 36,
  ml_holder_name: John Smith,
  description: a description,
  late_fee_amount: 35,
  payoff_amount: 45567.98,
  payoff_amount_date: 1607450357,
  original_maturity_date: 1607450357,
  principal_balance: 45056.7,
  escrow_balance: 2345.01,
  interest_period: monthly,
  initial_ml_amount: 65000,
  initial_ml_date: 1607450357,
  next_payment_principal_amount: 1256.67,
  next_payment_interest_amount: 234.56,
  next_payment: 1578,
  next_payment_date: 1607450357,
  last_payment_due_date: 1607450357,
  last_payment_receive_date: 1607450357,
  last_payment_principal_amount: 1256.67,
  last_payment_interest_amount: 234.56,
  last_payment_escrow_amount: 456.78,
  last_payment_last_fee_amount: 150,
  last_payment_late_charge: 50,
  ytd_principal_paid: 5432.01,
  ytd_interest_paid: 3948.56,
  ytd_insurance_paid: 1345.89,
  ytd_tax_paid: 1489,
  auto_pay_enrolled: true,
  margin_allowed: true,
  cash_account_allowed: true,
  collateral: nissan sentra,
  current_school: utah valley university,
  first_payment_date: 1607450357,
  first_mortgage: true,
  loan_payment_freq: monthly,
  original_school: Brigham young university,
  recurring_payment_amount: 456.23,
  lender: utah community credit union,
  ending_balance_amount: 234789.45,
  loan_term_type: fixed,
  payments_made: 14,
  balloon_amount: 1678.56,
  projected_interest: 10456.78,
  interest_paid_ltd: 56789.34,
  interest_rate_type: variable,
  loan_payment_type: principle,
  repayment_plan: Standard, Graduated, Extended, Pay As You Earn, and more.,
  payments_remaining: 45,
  margin_balance: 456,
  short_balance: 12456.89,
  available_cash_balance: 3456.78,
  maturity_value_amount: 34067.78,
  vested_balance: 45000,
  emp_match_amount: 256.99,
  emp_pretax_contrib_amount: 450,
  emp_pretax_contrib_amount_ytd: 700,
  contrib_total_ytd: 2045,
  cash_balance_amount: 2000,
  pre_tax_amount: 78564.99,
  after_tax_amount: 68564.99,
  match_amount: 378,
  profit_sharing_amount: 34678.89,
  rollover_amount: 101234.67,
  other_vest_amount: 34000,
  other_nonvest_amount: 26000,
  current_loan_balance: 345789.23,
  loan_rate: 3.275,
  buy_power: 34567.89,
  rollover_ltd: 23456.78,
  loan_award_id: 1234568,
  original_interest_rate: 12,
  guarantor: FinBank,
  owner: FinBank,
  interest_subsidy_type: Subsidy type,
  interest_balance: 2000,
  remaining_term_of_ml: 2,
  initial_interest_rate: 34567.89,
  fees_balance: 150,
  loan_ytd_interest_paid: 5623.23,
  loan_ytd_fees_paid: 5621.23,
  loan_ytd_principal_paid: 5621.23,
  loan_status: Deferment,
  loan_status_start_date: 1607450357,
  loan_status_end_date: 1607450357,
  weighted_interest_rate: 12,
  repayment_plan_start_date: 1607450357,
  repayment_plan_end_date: 1607450357,
  expected_payoff_date: 1607450357,
  out_of_school_date: 1607450357,
  convert_to_repayment: 1607450357,
  days_delinquent: 5,
  total_principal_paid: 15000,
  total_interest_paid: 1125,
  total_amount_paid: 16125
)
```

