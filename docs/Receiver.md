# OpenBanking::Receiver

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **routing_number** | **String** | Routing number of receiving bank |  |
| **account_number** | **String** | Micro entries receiving account number of bank |  |
| **account_type** | **String** | The list of supported account types. * \&quot;personalChecking\&quot;: Personal Checking * \&quot;businessChecking\&quot;: Business Checking * \&quot;personalSavings\&quot;: Personal Savings * \&quot;businessSavings\&quot;: Business Savings * \&quot;checking\&quot;: Standard checking, will be deprecated * \&quot;savings\&quot;: Standard savings, will be deprecated |  |
| **name** | **String** | Name of the customer |  |
| **memo** | **String** | Transaction memo to be displayed for transactions | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Receiver.new(
  routing_number: 123456789,
  account_number: 123456,
  account_type: personalChecking,
  name: Bob Smith,
  memo: micro deposit transfer
)
```

