# OpenBanking::ReportSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A report ID |  |
| **request_id** | **String** | Finicity indicator to track all activity associated with this report |  |
| **requester_name** | **String** | Name of a Finicity partner |  |
| **created_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |
| **consumer_id** | **String** | A consumer ID. See Create Consumer API for how to create a consumer ID. | [optional] |
| **consumer_ssn** | **String** | Last 4 digits of a SSN | [optional] |
| **type** | **String** | A report type. Possible values:  * &#x60;voi&#x60;  * &#x60;voa&#x60;  * &#x60;voaHistory&#x60;  * &#x60;history&#x60;  * &#x60;voieTxVerify&#x60;  * &#x60;voieWithReport&#x60;  * &#x60;voieWithInterview&#x60;  * &#x60;voieWithStatement&#x60;  * &#x60;paystatement&#x60;   * &#x60;preQualVoa&#x60;  * &#x60;assetSummary&#x60;  * &#x60;voie&#x60;  * &#x60;transactions&#x60;  * &#x60;statement&#x60;  * &#x60;voiePayroll&#x60;  * &#x60;voeTransactions&#x60;  * &#x60;voePayroll&#x60;  * &#x60;cfrp&#x60;  * &#x60;cfrb&#x60;  * &#x60;barpcra&#x60;  * &#x60;barpnoncra&#x60;  * &#x60;barbcra&#x60;  * &#x60;barbftc&#x60;  * &#x60;barbnoncra&#x60;  * &#x60;cfrpcra&#x60;  * &#x60;cfrpnoncra&#x60;  * &#x60;cracfrbcra&#x60;  * &#x60;cfrbnoncra&#x60;  * &#x60;cfrbftc&#x60;  |  |
| **status** | **String** | A report generation status. Possible values:  * &#x60;inProgress&#x60;  * &#x60;success&#x60;  * &#x60;failure&#x60;  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ReportSummary.new(
  id: u4hstnnak45g,
  request_id: cjqm4wtdcn,
  requester_name: Finicity Test API,
  created_date: 1607450357,
  consumer_id: 0bf46322c167b562e6cbed9d40e19a4c,
  consumer_ssn: 9999,
  type: voi,
  status: inProgress
)
```

