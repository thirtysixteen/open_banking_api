# OpenBanking::ReportInstitution

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The ID of a financial institution, represented as a number |  |
| **name** | **String** | Finicity institution name |  |
| **url_home_app** | **String** | The URL of the Financial Institution |  |
| **accounts** | [**Array&lt;ReportInstitutionAccount&gt;**](ReportInstitutionAccount.md) | A list of account records | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ReportInstitution.new(
  id: 4222,
  name: FinBank Profiles,
  url_home_app: http://www.finbank.com,
  accounts: null
)
```

