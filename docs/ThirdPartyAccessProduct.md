# OpenBanking::ThirdPartyAccessProduct

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product** | **String** | Third party access token can be generated for the following product types:   * \&quot;moneyTransferDetails\&quot;: Retrieve account details for money transfer * \&quot;availableBalance\&quot;: Retrieves the latest cached available and cleared     account balances for an account. * \&quot;availableBalanceLive\&quot;: Retrieves the available and cleared account balances live from the financial institution * \&quot;accountOwner\&quot;: Retrieves names and addresses of the account owner from a financial institution. * \&quot;paymentIndicator\&quot;: Get the Payment Success Indicator response, scoring the likelihood of payment settlement * \&quot;paymentFeedback\&quot;: Create feedback loop for Payment Success Indicator (PSI) and/or Payment Routing Optimizer (PRO) * \&quot;paymentRouting\&quot;: Product recommends the best rail to use as well as the best time to initiate the payment |  |
| **payor_id** | **String** | The Finicity Partner ID who should be billed when the Requester requests data from Finicity. If no value specified, then the Recipient will be billed. | [optional] |
| **max_calls** | **Integer** | Max number of calls to the consented product (consented API) | [optional] |
| **account_id** | **String** | An account ID |  |
| **access_period** | [**ThirdPartyAccessPeriod**](ThirdPartyAccessPeriod.md) |  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ThirdPartyAccessProduct.new(
  product: moneyTransferDetails,
  payor_id: 2445581559892,
  max_calls: 200,
  account_id: 5011648377,
  access_period: null
)
```

