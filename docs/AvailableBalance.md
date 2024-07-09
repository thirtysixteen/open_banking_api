# OpenBanking::AvailableBalance

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | A customer ID represented as a number. See Add Customer API for how to create a customer ID. |  |
| **real_account_number_last4** | **String** | The last 4 digits of the ACH account number |  |
| **available_balance** | **Float** | The available balance of the account |  |
| **available_balance_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |
| **cleared_balance** | **Float** | The cleared balance of the account. Also referred as posted balance, current balance, ledger balance |  |
| **cleared_balance_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |
| **aggregation_status_code** | **Integer** | The status of the most recent aggregation attempt (see [Aggregation Status Codes](https://developer.mastercard.com/open-banking-us/documentation/products/manage/account-aggregation/#aggregation-status-codes)). Won&#39;t be present until you have run your first aggregation for the account. |  |
| **currency** | **String** | A currency code |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AvailableBalance.new(
  id: 1005061234,
  real_account_number_last4: 5678,
  available_balance: 173.47,
  available_balance_date: 1607450357,
  cleared_balance: 222.25,
  cleared_balance_date: 1607450357,
  aggregation_status_code: null,
  currency: USD
)
```

