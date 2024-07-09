# OpenBanking::EmailOptions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **to** | **String** | The email address for the customer receiving the Connect email |  |
| **from** | **String** | The name of a person or business sending the Connect email | [optional] |
| **support_phone** | **String** | The support phone number listed in the email | [optional] |
| **subject** | **String** | The subject line of the email. The default is \&quot;Verify your Financial Information\&quot;. | [optional] |
| **first_name** | **String** | The first name of the customer or both names of the customers for joint borrowers. Example: \&quot;Marvin and Jenny\&quot;. | [optional] |
| **institution_name** | **String** | The name of your company | [optional] |
| **institution_address** | **String** | The institution address to appear in the footer of the email | [optional] |
| **signature** | **Array&lt;String&gt;** | A signature for the email | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::EmailOptions.new(
  to: bob@example.com,
  from: test.lender@test.com,
  support_phone: 800-555-5555,
  subject: Verify your income,
  first_name: Bob,
  institution_name: Acme Lending,
  institution_address: 222 Winnipeg Drive SLC UT, 84109,
  signature: [&quot;Cindy Mayfield&quot;,&quot;Senior Loan Officer&quot;,&quot;Direct 123-456-7890&quot;]
)
```

