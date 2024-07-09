# OpenBanking::VOETransactionsReportIncomeStream

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Income stream ID |  |
| **name** | **String** | A human-readable name based on the &#x60;normalizedPayee&#x60; name of the transactions for this income stream |  |
| **status** | **String** | Possible values: \&quot;ACTIVE\&quot;, \&quot;INACTIVE\&quot; |  |
| **estimate_inclusion** | **String** | Possible values: \&quot;HIGH\&quot;, \&quot;MODERATE\&quot;, \&quot;LOW\&quot;, \&quot;NO\&quot; |  |
| **confidence** | **Integer** | Level of confidence that the deposit stream represents income (example: 85%) |  |
| **cadence** | [**CadenceDetails**](CadenceDetails.md) |  |  |
| **days_since_last_transaction** | **Integer** | The number of days since the last credit transaction for the particular income stream |  |
| **next_expected_transaction_date** | **Integer** | The next expected credit transaction date for the particular income stream, based on the cadence |  |
| **income_stream_months** | **Integer** | The number of months the income transactions are observed | [optional] |
| **transactions** | [**Array&lt;ReportTransaction&gt;**](ReportTransaction.md) | A list of transaction records |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::VOETransactionsReportIncomeStream.new(
  id: dens28i3vsch-voah,
  name: none,
  status: ACTIVE,
  estimate_inclusion: HIGH,
  confidence: 70,
  cadence: null,
  days_since_last_transaction: 15,
  next_expected_transaction_date: 1572625469,
  income_stream_months: 18,
  transactions: null
)
```

