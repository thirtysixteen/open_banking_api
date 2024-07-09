# OpenBanking::Branding

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **logo** | **String** | File path of the institution&#39;s logo. For white backgrounds designed at 375 x 72, has built in spacing around it to normalize brand sizing. | [optional] |
| **alternate_logo** | **String** | File path of the institution&#39;s alternate logo. For colored backgrounds designed at 375 x 72 has built in spacing around it to normalize brand sizing. | [optional] |
| **icon** | **String** | File path of the institution&#39;s icon. For search results designed at 40 x 40. | [optional] |
| **primary_color** | **String** | Hex code for the institution&#39;s primary color | [optional] |
| **tile** | **String** | File path of institution name logo. For popular banks designed at 160 x 72. | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Branding.new(
  logo: https://prod-carpintero-branding.s3.us-west-2.amazonaws.com/5/logo.svg,
  alternate_logo: https://prod-carpintero-branding.s3.us-west-2.amazonaws.com/5/alternateLogo.svg,
  icon: https://prod-carpintero-branding.s3.us-west-2.amazonaws.com/5/icon.svg,
  primary_color: #0167AE,
  tile: https://prod-carpintero-branding.s3.us-west-2.amazonaws.com/5/tile.svg
)
```

