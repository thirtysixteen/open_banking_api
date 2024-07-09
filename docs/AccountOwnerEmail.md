# OpenBanking::AccountOwnerEmail

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **is_primary** | **Boolean** | The email is primary. | [optional] |
| **email** | **String** | An email address | [optional] |
| **email_type** | **String** | The account owner&#39;s email type.  * \&quot;Personal\&quot;  * \&quot;Business\&quot; | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AccountOwnerEmail.new(
  is_primary: true,
  email: myname@mycompany.com,
  email_type: Personal
)
```

