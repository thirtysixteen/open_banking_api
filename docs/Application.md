# OpenBanking::Application

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **app_description** | **String** | A short description of the app. This will be visible to end users in the FI interface. |  |
| **app_name** | **String** | The name of the application assigned to the customer |  |
| **app_url** | **String** | An URL for the app. This will be visible to end users in the FI interface. |  |
| **owner_address_line1** | **String** | Address line 1 |  |
| **owner_address_line2** | **String** | Address line 2 |  |
| **owner_city** | **String** | City for the business entity that owns the app. Information for registration purposes only and not given to the end user. |  |
| **owner_country** | **String** | Country for the  business entity that owns the app. Information for registration purposes only and not given to the end user. |  |
| **owner_name** | **String** | Business name for the business entity that owns the app. Information for registration purposes only and not given to the end user. |  |
| **owner_postal_code** | **String** | Zip code for the business entity that owns the app. Information for registration purposes only and not given to the end user. |  |
| **owner_state** | **String** | State for the business entity that owns the app. Information for registration purposes only and not given to the end user. |  |
| **image** | **String** | An app logo passed as a Base64 encoded image (1:1 SVG file, must be less than 50KB) |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Application.new(
  app_description: The app that makes your budgeting experience awesome,
  app_name: Awesome Budget App,
  app_url: https://www.finicity.com/,
  owner_address_line1: 434 W Ascension Way,
  owner_address_line2: Suite #200,
  owner_city: Murray,
  owner_country: USA,
  owner_name: Finicity,
  owner_postal_code: 84123,
  owner_state: UT,
  image: PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9Im5vIj8+CjxzdmcgICAKICAgeG1sbnM6c3ZnPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIKICAgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIgogICB2ZXJzaW9uPSIxLjEiCiAgIHZpZXdCb3g9IjAgMCAwIDAiCiAgIGhlaWdodD0iMCIKICAgd2lkdGg9IjAiPgogICAgPGcvPgo8L3N2Zz4K
)
```

