# OpenBanking::CashFlowPossibleLoanDepositsInstitutions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Finicity institution ID |  |
| **name** | **String** | Finicity institution name |  |
| **url_home_app** | **String** | The URL of the Financial Institution |  |
| **accounts** | [**Array&lt;CashFlowPossibleLoanDepositsAccount&gt;**](CashFlowPossibleLoanDepositsAccount.md) | A list of account records |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowPossibleLoanDepositsInstitutions.new(
  id: 102105,
  name: FinBank Profiles,
  url_home_app: http://www.finbank.com,
  accounts: null
)
```

