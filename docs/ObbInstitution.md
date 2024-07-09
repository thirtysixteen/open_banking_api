# OpenBanking::ObbInstitution

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **institution_icon_url** | **String** | URL of the institution logo icon for reporting | [optional] |
| **institution_id** | **Integer** | ID of the financial institution |  |
| **institution_name** | **String** | Name of the financial institution | [optional] |
| **institution_primary_color** | **String** | Primary branding color of the institution, in hex color format | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbInstitution.new(
  institution_icon_url: https://prod-carpintero-branding.s3.us-west-2.amazonaws.com/101732/icon.svg,
  institution_id: 12345,
  institution_name: Wells Fargo,
  institution_primary_color: #1B3E4A
)
```

