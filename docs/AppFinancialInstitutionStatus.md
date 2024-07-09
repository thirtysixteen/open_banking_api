# OpenBanking::AppFinancialInstitutionStatus

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The ID of a financial institution, represented as a number |  |
| **abbrv_name** | **String** | The application&#39;s abbreviated name | [optional] |
| **logo_url** | **String** | An URL to a logo file | [optional] |
| **decryption_key_activated** | **Boolean** | Status of decryption keys for financial institution app registration |  |
| **created_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |
| **last_modified_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |
| **status** | **Boolean** | \&quot;false\&quot; indicates registration is still pending |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AppFinancialInstitutionStatus.new(
  id: 4222,
  abbrv_name: VAEJ,
  logo_url: https://prod-direct-integration-client.s3.us-west-2.amazonaws.com/976521f99-7b36-4b3b-a3e0-faff9545836d/102224/90x90.png,
  decryption_key_activated: false,
  created_date: 1607450357,
  last_modified_date: 1607450357,
  status: true
)
```

