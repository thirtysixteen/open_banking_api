# OpenBanking::PaymentHistoryAccountSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_number_display** | **String** | Last four digits of the account |  |
| **financial_institution** | **String** | Name of the account&#39;s institution |  |
| **institution_icon** | **String** | URL of institution icon |  |
| **currency** | **String** | A currency code |  |
| **status** | **String** | An account status |  |
| **account_name** | **String** | The account name from the institution |  |
| **account_owner** | [**PaymentHistoryAccountSummaryAccountOwner**](PaymentHistoryAccountSummaryAccountOwner.md) |  |  |
| **account_type** | **String** | The list of supported account types. * \&quot;checking\&quot;: Standard checking * \&quot;savings\&quot;: Standard savings * \&quot;cd\&quot;: Certificates of deposit * \&quot;moneyMarket\&quot;: Money Market * \&quot;creditCard\&quot;: Standard credit cards * \&quot;lineOfCredit\&quot;: Home equity, line of credit * \&quot;investment\&quot;: Generic investment (no details) * \&quot;investmentTaxDeferred\&quot;: Generic tax-advantaged investment (no details) * \&quot;employeeStockPurchasePlan\&quot;: ESPP, Employee Stock Ownership Plans (ESOP), Stock Purchase Plans * \&quot;ira\&quot;: Individual Retirement Account (not Rollover or Roth) * \&quot;401k\&quot;: 401K Plan * \&quot;roth\&quot;: Roth IRA, Roth 401K * \&quot;403b\&quot;: 403B Plan * \&quot;529plan\&quot;: 529 Plan (True value is 529) * \&quot;rollover\&quot;: Rollover IRA * \&quot;ugma\&quot;: Uniform Gifts to Minors Act * \&quot;utma\&quot;: Uniform Transfers to Minors Act * \&quot;keogh\&quot;: Keogh Plan * \&quot;457plan\&quot;: 457 Plan (True value is 457) * \&quot;401a\&quot;: 401A Plan * \&quot;brokerageAccount\&quot;: Brokerage Account * \&quot;educationSavings\&quot;: Education Savings Account that is not a 529 * \&quot;healthSavingsAccount\&quot;: HSA (Health Savings Accounts) * \&quot;pension\&quot;: Pension * \&quot;profitSharingPlan\&quot;: Profit Sharing Plan * \&quot;roth401k\&quot;: Roth 401K * \&quot;sepIRA\&quot;: Simplified Employee Pension IRA * \&quot;simpleIRA\&quot;: Simple IRA * \&quot;thriftSavingsPlan\&quot;: Thrift Savings Plan * \&quot;variableAnnuity\&quot;: Variable Annuity * \&quot;cryptocurrency\&quot;: Cryptocurrency Wallet, Cryptocurrency Account * \&quot;mortgage\&quot;: Standard Mortgages * \&quot;loan\&quot;: Auto loans, equity loans, other loans * \&quot;studentLoan\&quot;: Student Loan * \&quot;studentLoanGroup\&quot;: Student Loan Group * \&quot;studentLoanAccount\&quot;: Student Loan Account |  |
| **beginning_balance** | **Float** | Beginning balance of account |  |
| **average_monthly_balance** | **Float** | Monthly average balance of account |  |
| **current_balance** | **Float** | Current balance of account |  |
| **begin_date** | **String** | Begin date of account |  |
| **end_date** | **String** | End date of account |  |
| **total_nonsufficient_funds** | **Float** | Total of NSF transactions in this account | [optional] |
| **days_since_nonsufficient_funds** | **Integer** | Days since the latest NSF transaction for this account |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PaymentHistoryAccountSummary.new(
  account_number_display: 2222,
  financial_institution: FinBank,
  institution_icon: https://my-sample-app.com/12345/some-icon.jpg,
  currency: USD,
  status: pending,
  account_name: My 401k,
  account_owner: null,
  account_type: checking,
  beginning_balance: 123.45,
  average_monthly_balance: 123.45,
  current_balance: 123.45,
  begin_date: 2023-06-01,
  end_date: 2023-06-01,
  total_nonsufficient_funds: 123.45,
  days_since_nonsufficient_funds: 3
)
```

