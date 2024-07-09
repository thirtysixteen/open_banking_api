# OpenBanking::AppStatus

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **partner_id** | **String** | Your Partner ID displayed in the [Developer Dashboard](https://developer.mastercard.com/account/log-in) |  |
| **pre_app_id** | **String** | Identifier to track the application registration from the App Registration and Get App Registration Status APIs |  |
| **note** | **String** | A note on the registration. Typically used to indicate reasons for rejected apps. | [optional] |
| **application_id** | **String** | &#x60;applicationId&#x60; value returned from the Get App Registration Status API and the partner assign the customers to. This cannot be changed once set. Only applicable in cases of partners with multiple registered applications. If the partner only has one app, this can usually be omitted. This field is populated after the app is in a status approved. | [optional] |
| **app_name** | **String** | The name of the application assigned to the customer |  |
| **submitted_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |
| **modified_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |
| **status** | **String** | The status of an app registration request. \&quot;A\&quot; means approved. \&quot;P\&quot; means pending which is the status when initially submitted or when the app is modified and awaiting approval. \&quot;R\&quot; means rejected. If it is rejected there will be a note with the rejected reason. |  |
| **scopes** | **String** | Indicates scopes of data accessible to the app | [optional] |
| **institution_details** | [**Array&lt;AppFinancialInstitutionStatus&gt;**](AppFinancialInstitutionStatus.md) | A list of the registration status for each FI for the application | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AppStatus.new(
  partner_id: 1234583871234,
  pre_app_id: 2581,
  note: Approved,
  application_id: 123456789,
  app_name: Awesome Budget App,
  submitted_date: 1607450357,
  modified_date: 1607450357,
  status: P,
  scopes: Account Info,
  institution_details: null
)
```

