# OpenBanking::CustomerAuthorizationDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **institution_login_id** | **Integer** | Institution login id of the customer. |  |
| **authorization_start_date** | **String** | Authorization start date and time in ISO 8601 format. |  |
| **authorization_end_date** | **String** | Authorization end date and time in ISO 8601 format. |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CustomerAuthorizationDetails.new(
  institution_login_id: 7009561328,
  authorization_start_date: 2020-07-30T16:11:23:20Z,
  authorization_end_date: 2020-07-30T16:11:23:20Z
)
```

