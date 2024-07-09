# OpenBanking::CashFlowPossibleLoanDepositsAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Finicity account ID |  |
| **owner_name** | **String** | The name(s) of the account owner(s). If the owner information is not available, this field will not appear in the report. If the account has multiple owners then all owners will be listed separated by |. |  |
| **owner_address** | **String** | The mailing address of the account owner(s). If the owner information is not available, this field will not appear in the report. If the account has multiple owners then the address of the primary owner will be listed. |  |
| **name** | **String** | The account name from the institution |  |
| **number** | **String** | The account number from the institution (obfuscated) |  |
| **type** | **String** | CFR: &#x60;ALL&#x60; (&#x60;checking&#x60; / &#x60;savings&#x60; / &#x60;loan&#x60; / &#x60;mortgage&#x60; / &#x60;credit card&#x60; / &#x60;CD&#x60; / &#x60;MM&#x60; / &#x60;investment&#x60;...) |  |
| **aggregation_status_code** | **Integer** | The status of the most recent aggregation attempt for this account (non-zero means the account was not accessed successfully for this report, and additional fields for this account may not be reliable) |  |
| **current_balance** | **Float** | The cleared balance of the account as-of &#x60;balanceDate&#x60; |  |
| **available_balance** | **Float** | Available balance |  |
| **balance_date** | **Integer** | A timestamp showing when the &#x60;balance&#x60; was captured |  |
| **transactions** | [**Array&lt;ReportTransaction&gt;**](ReportTransaction.md) | a list of transaction records |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CashFlowPossibleLoanDepositsAccount.new(
  id: 6681984,
  owner_name: PATRICK PURCHASER|LORRAINE PURCHASER,
  owner_address: 7195 BELMONT ST. PARLIN, NJ 08859,
  name: Checking,
  number: XX1111,
  type: checking,
  aggregation_status_code: 0,
  current_balance: 100000,
  available_balance: 1000,
  balance_date: 1614880526,
  transactions: null
)
```

