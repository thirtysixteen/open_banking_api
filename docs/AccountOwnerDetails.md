# OpenBanking::AccountOwnerDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **relationship** | **String** | The type of relationship to the account: * \&quot;AUTHORIZED_USER\&quot;  * \&quot;BUSINESS\&quot;  * \&quot;FOR_BENEFIT_OF_PRIMARY\&quot;  * \&quot;FOR_BENEFIT_OF_PRIMARY_JOINT_RESTRICTED\&quot;  * \&quot;FOR_BENEFIT_OF_SECONDARY\&quot;  * \&quot;FOR_BENEFIT_OF_SECONDARY_JOINT_RESTRICTED\&quot;  * \&quot;FOR_BENEFIT_OF_SOLE_OWNER_RESTRICTED\&quot;  * \&quot;POWER_OF_ATTORNEY\&quot;  * \&quot;PRIMARY_JOINT_TENANTS\&quot;  * \&quot;PRIMARY\&quot;  * \&quot;PRIMARY_BORROWER\&quot;  * \&quot;PRIMARY_JOINT\&quot;  * \&quot;SECONDARY\&quot;  * \&quot;SECONDARY_JOINT_TENANTS\&quot;  * \&quot;SECONDARY_BORROWER\&quot;  * \&quot;SECONDARY_JOINT\&quot;  * \&quot;SOLE_OWNER\&quot;  * \&quot;TRUSTEE\&quot;  * \&quot;UNIFORM_TRANSFER_TO_MINOR\&quot; | [optional] |
| **owner_name** | **String** | The full name of the account owner. Multiple account owners are returned in one string per the source data from the institution. |  |
| **first_name** | **String** | The first name of the account holder | [optional] |
| **middle_name** | **String** | The middle name of the account holder | [optional] |
| **last_name** | **String** | The last name of the account holder | [optional] |
| **suffix** | **String** | A generational or academic suffix | [optional] |
| **name_classification** | **String** | The classification of the account holder: * \&quot;person / personal / home\&quot; * \&quot;business\&quot; * \&quot;other\&quot; | [optional] |
| **name_classificationconfidencescore** | **Float** | The confidence score (between zero and one) of the name classification. | [optional] |
| **addresses** | [**Array&lt;AccountOwnerAddress&gt;**](AccountOwnerAddress.md) | List of addresses |  |
| **emails** | [**Array&lt;AccountOwnerEmail&gt;**](AccountOwnerEmail.md) | List of emails | [optional] |
| **phones** | [**Array&lt;AccountOwnerPhone&gt;**](AccountOwnerPhone.md) | List of phones | [optional] |
| **documentations** | [**Array&lt;AccountOwnerDocumentation&gt;**](AccountOwnerDocumentation.md) | List of account owner documentation | [optional] |
| **identity_insights** | [**AccountOwnerIdentityInsights**](AccountOwnerIdentityInsights.md) |  | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AccountOwnerDetails.new(
  relationship: AUTHORIZED_USER,
  owner_name: John Smith, PhD,
  first_name: John,
  middle_name: L,
  last_name: Smith,
  suffix: PhD,
  name_classification: person,
  name_classificationconfidencescore: 0.9,
  addresses: null,
  emails: null,
  phones: null,
  documentations: null,
  identity_insights: null
)
```

