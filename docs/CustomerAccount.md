# OpenBanking::CustomerAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | An account ID |  |
| **number** | **String** | The account number from the institution |  |
| **account_number_display** | **String** | The account number from a financial institution in truncated format:    * Last four digits: \&quot;1234\&quot;    * Last four digits with suffix: \&quot;1234-9\&quot;    * Full value for string accounts: \&quot;john@gmail.com\&quot; example: &#39;1234-9&#39; |  |
| **real_account_number_last4** | **String** | The last 4 digits of the ACH account number | [optional] |
| **name** | **String** | The account name from the institution |  |
| **balance** | **Float** | The cleared balance of the account as of &#x60;balanceDate&#x60; | [optional] |
| **type** | **String** | The list of supported account types. * \&quot;checking\&quot;: Standard checking * \&quot;savings\&quot;: Standard savings * \&quot;cd\&quot;: Certificates of deposit * \&quot;moneyMarket\&quot;: Money Market * \&quot;creditCard\&quot;: Standard credit cards * \&quot;lineOfCredit\&quot;: Home equity, line of credit * \&quot;investment\&quot;: Generic investment (no details) * \&quot;investmentTaxDeferred\&quot;: Generic tax-advantaged investment (no details) * \&quot;employeeStockPurchasePlan\&quot;: ESPP, Employee Stock Ownership Plans (ESOP), Stock Purchase Plans * \&quot;ira\&quot;: Individual Retirement Account (not Rollover or Roth) * \&quot;401k\&quot;: 401K Plan * \&quot;roth\&quot;: Roth IRA, Roth 401K * \&quot;403b\&quot;: 403B Plan * \&quot;529plan\&quot;: 529 Plan (True value is 529) * \&quot;rollover\&quot;: Rollover IRA * \&quot;ugma\&quot;: Uniform Gifts to Minors Act * \&quot;utma\&quot;: Uniform Transfers to Minors Act * \&quot;keogh\&quot;: Keogh Plan * \&quot;457plan\&quot;: 457 Plan (True value is 457) * \&quot;401a\&quot;: 401A Plan * \&quot;brokerageAccount\&quot;: Brokerage Account * \&quot;educationSavings\&quot;: Education Savings Account that is not a 529 * \&quot;healthSavingsAccount\&quot;: HSA (Health Savings Accounts) * \&quot;pension\&quot;: Pension * \&quot;profitSharingPlan\&quot;: Profit Sharing Plan * \&quot;roth401k\&quot;: Roth 401K * \&quot;sepIRA\&quot;: Simplified Employee Pension IRA * \&quot;simpleIRA\&quot;: Simple IRA * \&quot;thriftSavingsPlan\&quot;: Thrift Savings Plan * \&quot;variableAnnuity\&quot;: Variable Annuity * \&quot;cryptocurrency\&quot;: Cryptocurrency Wallet, Cryptocurrency Account * \&quot;mortgage\&quot;: Standard Mortgages * \&quot;loan\&quot;: Auto loans, equity loans, other loans * \&quot;studentLoan\&quot;: Student Loan * \&quot;studentLoanGroup\&quot;: Student Loan Group * \&quot;studentLoanAccount\&quot;: Student Loan Account |  |
| **aggregation_status_code** | **Integer** | The status of the most recent aggregation attempt (see [Aggregation Status Codes](https://developer.mastercard.com/open-banking-us/documentation/products/manage/account-aggregation/#aggregation-status-codes)). Won&#39;t be present until you have run your first aggregation for the account. | [optional] |
| **status** | **String** | \&quot;pending\&quot; during account discovery, always \&quot;active\&quot; following   successful account activation |  |
| **customer_id** | **String** | A customer ID. See Add Customer API for how to create a customer ID. |  |
| **institution_id** | **String** | The ID of a financial institution |  |
| **balance_date** | **Integer** | A timestamp showing when the balance was captured. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **aggregation_success_date** | **Integer** | A timestamp showing the last successful aggregation of the account. This will not be present until you have run your first aggregation for the account. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **aggregation_attempt_date** | **Integer** | A timestamp showing the last aggregation attempt, whether successful or not. This will not be present until you have run your first aggregation for the account. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **created_date** | **Integer** | A timestamp showing when the account was added to the system. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |
| **last_updated_date** | **Integer** | A timestamp showing when the account was last modified to the system. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **market_segment** | **String** | The market segment of the account. Possible values: personal, business | [optional] |
| **currency** | **String** | A currency code |  |
| **last_transaction_date** | **Integer** | The date of the latest transaction on the account. This will not be present until you have run your first aggregation for the account. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **oldest_transaction_date** | **Integer** | The date of the oldest transaction in the transactions for the account. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **institution_login_id** | **Integer** | An institution login ID (from the account record), represented as a number |  |
| **detail** | [**CustomerAccountDetail**](CustomerAccountDetail.md) |  | [optional] |
| **position** | [**Array&lt;CustomerAccountPosition&gt;**](CustomerAccountPosition.md) | Investment holdings | [optional] |
| **display_position** | **Integer** | Display position of the account at the financial institution, \&quot;1\&quot;     being the top listed account | [optional] |
| **parent_account** | **String** | The assigned account ID for the account one level higher in the student loan account hierarchy | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CustomerAccount.new(
  id: 5011648377,
  number: 2000004444,
  account_number_display: null,
  real_account_number_last4: 5678,
  name: Super Checking,
  balance: 401.26,
  type: checking,
  aggregation_status_code: null,
  status: active,
  customer_id: 1005061234,
  institution_id: 4222,
  balance_date: 1607450357,
  aggregation_success_date: 1607450357,
  aggregation_attempt_date: 1607450357,
  created_date: 1607450357,
  last_updated_date: 1607450357,
  market_segment: personal,
  currency: USD,
  last_transaction_date: 1607450357,
  oldest_transaction_date: 1607450357,
  institution_login_id: 1007302745,
  detail: null,
  position: null,
  display_position: 2,
  parent_account: 5011648377
)
```

