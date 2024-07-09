# OpenBanking::PayrollReportAck

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A report ID |  |
| **customer_type** | **String** | The type of customer (\&quot;active\&quot; or \&quot;testing\&quot; or \&quot;\&quot; for all types) |  |
| **customer_id** | **Integer** | A customer ID represented as a number. See Add Customer API for how to create a customer ID. |  |
| **request_id** | **String** | Finicity indicator to track all activity associated with this report |  |
| **requester_name** | **String** | Name of a Finicity partner |  |
| **end_user** | [**ConsumerEndUser**](ConsumerEndUser.md) |  | [optional] |
| **created_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). Note: If the report is retrieved on a day other than the day it was generated, on the header of the PDF version of the report there will be a \&quot;Retrieved Date\&quot; populated. |  |
| **title** | **String** | Title of the report |  |
| **consumer_id** | **String** | A consumer ID. See Create Consumer API for how to create a consumer ID. |  |
| **consumer_ssn** | **String** | Last 4 digits of a SSN |  |
| **dispute_statement** | **String** | The dispute text | [optional] |
| **type** | **String** | A report type. Possible values:  * &#x60;voi&#x60;  * &#x60;voa&#x60;  * &#x60;voaHistory&#x60;  * &#x60;history&#x60;  * &#x60;voieTxVerify&#x60;  * &#x60;voieWithReport&#x60;  * &#x60;voieWithInterview&#x60;  * &#x60;voieWithStatement&#x60;  * &#x60;paystatement&#x60;   * &#x60;preQualVoa&#x60;  * &#x60;assetSummary&#x60;  * &#x60;voie&#x60;  * &#x60;transactions&#x60;  * &#x60;statement&#x60;  * &#x60;voiePayroll&#x60;  * &#x60;voeTransactions&#x60;  * &#x60;voePayroll&#x60;  * &#x60;cfrp&#x60;  * &#x60;cfrb&#x60;  * &#x60;barpcra&#x60;  * &#x60;barpnoncra&#x60;  * &#x60;barbcra&#x60;  * &#x60;barbftc&#x60;  * &#x60;barbnoncra&#x60;  * &#x60;cfrpcra&#x60;  * &#x60;cfrpnoncra&#x60;  * &#x60;cracfrbcra&#x60;  * &#x60;cfrbnoncra&#x60;  * &#x60;cfrbftc&#x60;  |  |
| **status** | **String** | A report generation status. Possible values:  * &#x60;inProgress&#x60;  * &#x60;success&#x60;  * &#x60;failure&#x60;  |  |
| **constraints** | [**PayrollReportConstraintsOut**](PayrollReportConstraintsOut.md) |  |  |
| **errors** | [**Array&lt;ErrorMessage&gt;**](ErrorMessage.md) | In case errors occurred during the report generation | [optional] |
| **portfolio_id** | **String** | A unique identifier that will be consistent across all reports created for the same customer |  |
| **report_style** | **String** | A report style. Possible values are directAPIPayroll, credentialedPayroll, paystatement, voieWithInterview, voieWithStatement, voieWithReport | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PayrollReportAck.new(
  id: u4hstnnak45g,
  customer_type: active,
  customer_id: 1005061234,
  request_id: cjqm4wtdcn,
  requester_name: Finicity Test API,
  end_user: null,
  created_date: 1607450357,
  title: Finicity Asset Ready Report (CRA),
  consumer_id: 0bf46322c167b562e6cbed9d40e19a4c,
  consumer_ssn: 9999,
  dispute_statement: Statement dispute text,
  type: voi,
  status: inProgress,
  constraints: null,
  errors: null,
  portfolio_id: y4zsgccj4xpw-6-port,
  report_style: credentialedPayroll
)
```

