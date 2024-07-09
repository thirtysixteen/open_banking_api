# OpenBanking::Report

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
| **consumer_id** | **String** | A consumer ID. See Create Consumer API for how to create a consumer ID. | [optional] |
| **consumer_ssn** | **String** | Last 4 digits of a SSN | [optional] |
| **dispute_statement** | **String** | The dispute text | [optional] |
| **type** | **String** | A report type. Possible values:  * &#x60;voi&#x60;  * &#x60;voa&#x60;  * &#x60;voaHistory&#x60;  * &#x60;history&#x60;  * &#x60;voieTxVerify&#x60;  * &#x60;voieWithReport&#x60;  * &#x60;voieWithInterview&#x60;  * &#x60;voieWithStatement&#x60;  * &#x60;paystatement&#x60;   * &#x60;preQualVoa&#x60;  * &#x60;assetSummary&#x60;  * &#x60;voie&#x60;  * &#x60;transactions&#x60;  * &#x60;statement&#x60;  * &#x60;voiePayroll&#x60;  * &#x60;voeTransactions&#x60;  * &#x60;voePayroll&#x60;  * &#x60;cfrp&#x60;  * &#x60;cfrb&#x60;  * &#x60;barpcra&#x60;  * &#x60;barpnoncra&#x60;  * &#x60;barbcra&#x60;  * &#x60;barbftc&#x60;  * &#x60;barbnoncra&#x60;  * &#x60;cfrpcra&#x60;  * &#x60;cfrpnoncra&#x60;  * &#x60;cracfrbcra&#x60;  * &#x60;cfrbnoncra&#x60;  * &#x60;cfrbftc&#x60;  |  |
| **status** | **String** | A report generation status. Possible values:  * &#x60;inProgress&#x60;  * &#x60;success&#x60;  * &#x60;failure&#x60;  |  |
| **constraints** | [**BaseReportAckConstraints**](BaseReportAckConstraints.md) |  |  |
| **errors** | [**Array&lt;ErrorMessage&gt;**](ErrorMessage.md) | In case errors occurred during the report generation | [optional] |
| **business_details** | [**BusinessDetails**](BusinessDetails.md) |  | [optional] |
| **report_pin** | **String** | A unique key returned per report for consumer Portal | [optional] |
| **start_date** | **Integer** | The &#x60;postedDate&#x60; of the earliest transaction analyzed for the report. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **end_date** | **Integer** | The &#x60;postedDate&#x60; of the latest transaction analyzed for the report. A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). | [optional] |
| **days** | **Integer** | Number of days covered by the report | [optional] |
| **seasoned** | **Boolean** | \&quot;true\&quot; if the report covers more than 180 days | [optional] |
| **institutions** | [**Array&lt;ReportInstitution&gt;**](ReportInstitution.md) | The details of the financial institution accounts included in the report. | [optional] |
| **customer_analytics** | [**CustomerAnalytics**](CustomerAnalytics.md) |  | [optional] |
| **portfolio_id** | **String** | A unique identifier that will be consistent across all reports created for the same customer | [optional] |
| **cash_flow_balance_summary** | [**CashFlowCashFlowBalanceSummary**](CashFlowCashFlowBalanceSummary.md) |  | [optional] |
| **cash_flow_credit_summary** | [**CashFlowCashFlowCreditSummary**](CashFlowCashFlowCreditSummary.md) |  | [optional] |
| **cash_flow_debit_summary** | [**CashFlowCashFlowDebitSummary**](CashFlowCashFlowDebitSummary.md) |  | [optional] |
| **cash_flow_characteristics_summary** | [**CashFlowCashFlowCharacteristicsSummary**](CashFlowCashFlowCharacteristicsSummary.md) |  | [optional] |
| **possible_loan_deposits** | [**Array&lt;CashFlowPossibleLoanDeposits&gt;**](CashFlowPossibleLoanDeposits.md) | A possible loan deposits record | [optional] |
| **consolidated_available_balance** | **Float** | The sum of available balance for all of the accounts included in the report | [optional] |
| **assets** | [**PrequalificationReportAssetSummary**](PrequalificationReportAssetSummary.md) |  | [optional] |
| **report_style** | **String** | A report style. Possible values are directAPIPayroll, credentialedPayroll, paystatement, voieWithInterview, voieWithStatement, voieWithReport | [optional] |
| **number_of_billable_assets** | **Integer** | Total number of billable pay statements included in the report | [optional] |
| **asset_ids** | **Array&lt;String&gt;** | The pay statements included in the report | [optional] |
| **pay_statements** | [**Array&lt;VOIEPaystubWithStatementPayStatement&gt;**](VOIEPaystubWithStatementPayStatement.md) | Extracted pay statement details, and the transaction matching summary | [optional] |
| **asset_id** | **String** | An asset ID. Generated by Connect or by using the Store Customer Pay Statement API. | [optional] |
| **employment_history** | [**Array&lt;PayrollEmploymentHistoryVOIE&gt;**](PayrollEmploymentHistoryVOIE.md) | An array of employment histories, one for each of the consumer&#39;s verified employers | [optional] |
| **gse_enabled** | **Boolean** | Mastercard Open Banking internal use only to flag reports that should not be retrieved by the GSE&#39;s (Government-Sponsored Enterprise).  This is a mandatory field for VOE-payroll and VOIE-payroll report types. | [optional] |
| **income** | [**Array&lt;ReportIncomeStreamSummary&gt;**](ReportIncomeStreamSummary.md) | Income details | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Report.new(
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
  business_details: null,
  report_pin: 2398jk,
  start_date: 1607450357,
  end_date: 1607450357,
  days: 200,
  seasoned: true,
  institutions: null,
  customer_analytics: null,
  portfolio_id: y4zsgccj4xpw-6-port,
  cash_flow_balance_summary: null,
  cash_flow_credit_summary: null,
  cash_flow_debit_summary: null,
  cash_flow_characteristics_summary: null,
  possible_loan_deposits: null,
  consolidated_available_balance: 1929.57,
  assets: null,
  report_style: credentialedPayroll,
  number_of_billable_assets: 1,
  asset_ids: null,
  pay_statements: null,
  asset_id: 097545c5-1c2a-4f20-a5ef-77f0820344c9-2018601178,
  employment_history: null,
  gse_enabled: true,
  income: null
)
```

