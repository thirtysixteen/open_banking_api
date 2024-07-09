# OpenBanking::App

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pre_app_id** | **Integer** | The Pre-app Id is generated after the partner submits the request to create an application using the /aggregation/v1/partners/applications API. | [optional] |
| **application_id** | **String** | The Application Id is assigned to the pre-app after the pre-app approval. | [optional] |
| **status** | **String** | The application registration status with Mastercard.&#39;A&#39;&#x3D;Active , &#39;P&#39;&#x3D;Pending , &#39;D&#39;&#x3D;Deleted , &#39;R&#39;&#x3D;Rejected. | [optional] |
| **name** | **String** | The name of the application submitted by the partner. | [optional] |
| **scopes** | **String** | The scope of the application for the partner. | [optional] |
| **note** | **String** | The note for the pre-application status. | [optional] |
| **created_date** | **String** | The application creation date and time in ISO 8601 format. | [optional] |
| **modified_date** | **String** | The application modification date and time are in ISO 8601 format. | [optional] |
| **submitted_date** | **String** | The application submitted date and time in ISO 8601 format. | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::App.new(
  pre_app_id: 13,
  application_id: 234dsfdsf-535fdgdtrtr-546464564,
  status: A,
  name: Mvelopes,
  scopes: Account Number, Account Info,
  note: Approved,
  created_date: 2020-06-02T06:00:00Z,
  modified_date: 2020-06-02T06:00:00Z,
  submitted_date: 2020-06-02T06:00:00Z
)
```

