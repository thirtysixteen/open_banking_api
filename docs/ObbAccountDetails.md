# OpenBanking::ObbAccountDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_number_display** | **String** | The account number from a financial institution in truncated format | [optional] |
| **account_owner** | [**ObbAccountOwner**](ObbAccountOwner.md) |  |  |
| **aggregation_attempt_date** | **String** | A timestamp showing the last aggregation attempt. This will not be present until you have run your first aggregation for the account. | [optional] |
| **aggregation_status_code** | **Integer** | The status of the most recent aggregation attempt. This will not be present until you have run your first aggregation for the account | [optional] |
| **aggregation_success_date** | **String** | A timestamp showing the last successful aggregation of the account. This will not be present until you have run your first aggregation for the account. | [optional] |
| **currency** | **String** | The currency of the account | [optional] |
| **current_balance** | **Float** | Current reported balance of the account | [optional] |
| **id** | **Integer** | An account ID represented as a number |  |
| **institution** | [**ObbInstitution**](ObbInstitution.md) |  |  |
| **institution_login_id** | **Integer** | An institution login ID (from the account record), represented as a number | [optional] |
| **name** | **String** | The account name from the institution | [optional] |
| **real_account_number_last4** | **Integer** | The last 4 digits of the ACH account number | [optional] |
| **status** | **String** | pending during account discovery, always active following successful account activation | [optional] |
| **type** | **String** | Account type, e.g. checking/saving | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbAccountDetails.new(
  account_number_display: 8888,
  account_owner: null,
  aggregation_attempt_date: 2022-03-30T14:47:19-07:00,
  aggregation_status_code: 0,
  aggregation_success_date: 2022-03-30T14:47:19-07:00,
  currency: USD,
  current_balance: 2239.22,
  id: 5011648377,
  institution: null,
  institution_login_id: 1007302745,
  name: Super Checking,
  real_account_number_last4: 5678,
  status: active,
  type: checking
)
```

