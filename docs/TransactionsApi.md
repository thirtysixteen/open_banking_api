# OpenBanking::TransactionsApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**generate_transactions_report**](TransactionsApi.md#generate_transactions_report) | **POST** /decisioning/v2/customers/{customerId}/transactions | Generate Transactions Report |
| [**get_all_customer_transactions**](TransactionsApi.md#get_all_customer_transactions) | **GET** /aggregation/v3/customers/{customerId}/transactions | Get All Customer Transactions |
| [**get_customer_account_transactions**](TransactionsApi.md#get_customer_account_transactions) | **GET** /aggregation/v4/customers/{customerId}/accounts/{accountId}/transactions | Get Customer Account Transactions |
| [**get_customer_transaction**](TransactionsApi.md#get_customer_transaction) | **GET** /aggregation/v2/customers/{customerId}/transactions/{transactionId} | Get Customer Transaction by ID |
| [**load_historic_transactions_for_customer_account**](TransactionsApi.md#load_historic_transactions_for_customer_account) | **POST** /aggregation/v1/customers/{customerId}/accounts/{accountId}/transactions/historic | Load Historic Transactions for Customer Account |


## generate_transactions_report

> <TransactionsReportAck> generate_transactions_report(customer_id, to_date, transactions_report_constraints, opts)

Generate Transactions Report

Generate a Transaction Report for the given accounts under the given customer. This service retrieves up to 24 months of transaction history for the given customer. It then uses this information to generate the Transaction Report.  This is a premium service. A billable event will be created upon the successful generation of the Transactions Report.  Before calling this API, a consumer must be created for the given customer ID (see Consumers APIs).  There cannot be more than 24 months between `fromDate` and `toDate`.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

### Examples

```ruby
require 'time'
require 'open_banking'
# setup authorization
OpenBanking.configure do |config|
  # Configure API key authorization: FinicityAppToken
  config.api_key['FinicityAppToken'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppToken'] = 'Bearer'

  # Configure API key authorization: FinicityAppKey
  config.api_key['FinicityAppKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppKey'] = 'Bearer'
end

api_instance = OpenBanking::TransactionsApi.new
customer_id = '1005061234' # String | A customer ID
to_date = 1607450357 # Integer | A end date
transactions_report_constraints = OpenBanking::TransactionsReportConstraints.new # TransactionsReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook', # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
  include_pending: false # Boolean | If pending transactions must be included
}

begin
  # Generate Transactions Report
  result = api_instance.generate_transactions_report(customer_id, to_date, transactions_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling TransactionsApi->generate_transactions_report: #{e}"
end
```

#### Using the generate_transactions_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TransactionsReportAck>, Integer, Hash)> generate_transactions_report_with_http_info(customer_id, to_date, transactions_report_constraints, opts)

```ruby
begin
  # Generate Transactions Report
  data, status_code, headers = api_instance.generate_transactions_report_with_http_info(customer_id, to_date, transactions_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TransactionsReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling TransactionsApi->generate_transactions_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **to_date** | **Integer** | A end date |  |
| **transactions_report_constraints** | [**TransactionsReportConstraints**](TransactionsReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |
| **include_pending** | **Boolean** | If pending transactions must be included | [optional][default to false] |

### Return type

[**TransactionsReportAck**](TransactionsReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## get_all_customer_transactions

> <Transactions> get_all_customer_transactions(customer_id, from_date, to_date, opts)

Get All Customer Transactions

Get all transactions available for this customer within the given date range, across all accounts. This service supports paging and sorting by `transactionDate` (or `postedDate` if no transaction date is provided), with a maximum of 1000 transactions per request.  Standard consumer aggregation provides up to 180 days of transactions prior to the date each account was added to the Finicity system. To access older transactions, you must first call the service Load Historic Transactions for Account.  There is no limit for the size of the window between `fromDate` and `toDate`, however, the maximum number of transactions returned on one page is 1000.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

### Examples

```ruby
require 'time'
require 'open_banking'
# setup authorization
OpenBanking.configure do |config|
  # Configure API key authorization: FinicityAppToken
  config.api_key['FinicityAppToken'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppToken'] = 'Bearer'

  # Configure API key authorization: FinicityAppKey
  config.api_key['FinicityAppKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppKey'] = 'Bearer'
end

api_instance = OpenBanking::TransactionsApi.new
customer_id = '1005061234' # String | A customer ID
from_date = 1607450357 # Integer | A start date
to_date = 1607450357 # Integer | A end date
opts = {
  start: 1, # Integer | Index of the page of results to return
  limit: 1, # Integer | Maximum number of results per page
  sort: 'desc', # String | Date sort order: \"asc\" for ascending, \"desc\" for descending
  include_pending: false # Boolean | If pending transactions must be included
}

begin
  # Get All Customer Transactions
  result = api_instance.get_all_customer_transactions(customer_id, from_date, to_date, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling TransactionsApi->get_all_customer_transactions: #{e}"
end
```

#### Using the get_all_customer_transactions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Transactions>, Integer, Hash)> get_all_customer_transactions_with_http_info(customer_id, from_date, to_date, opts)

```ruby
begin
  # Get All Customer Transactions
  data, status_code, headers = api_instance.get_all_customer_transactions_with_http_info(customer_id, from_date, to_date, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Transactions>
rescue OpenBanking::ApiError => e
  puts "Error when calling TransactionsApi->get_all_customer_transactions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **from_date** | **Integer** | A start date |  |
| **to_date** | **Integer** | A end date |  |
| **start** | **Integer** | Index of the page of results to return | [optional][default to 1] |
| **limit** | **Integer** | Maximum number of results per page | [optional][default to 25] |
| **sort** | **String** | Date sort order: \&quot;asc\&quot; for ascending, \&quot;desc\&quot; for descending | [optional][default to &#39;desc&#39;] |
| **include_pending** | **Boolean** | If pending transactions must be included | [optional][default to false] |

### Return type

[**Transactions**](Transactions.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customer_account_transactions

> <Transactions> get_customer_account_transactions(customer_id, account_id, from_date, to_date, opts)

Get Customer Account Transactions

Get all transactions available for this customer account within the given date range. This service supports paging and sorting by `transactionDate` (or `postedDate` if no transaction date is provided), with a maximum of 1000 transactions per request.  Standard consumer aggregation provides up to 180 days of transactions prior to the date each account was added to the Finicity system. To access older transactions, you must first call the Cash Flow Verification service Load Historic Transactions for Account.  There is no limit for the size of the window between `fromDate` and `toDate`, however, the maximum number of transactions returned on one page is 1000.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

### Examples

```ruby
require 'time'
require 'open_banking'
# setup authorization
OpenBanking.configure do |config|
  # Configure API key authorization: FinicityAppToken
  config.api_key['FinicityAppToken'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppToken'] = 'Bearer'

  # Configure API key authorization: FinicityAppKey
  config.api_key['FinicityAppKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppKey'] = 'Bearer'
end

api_instance = OpenBanking::TransactionsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID
from_date = 1607450357 # Integer | A start date
to_date = 1607450357 # Integer | A end date
opts = {
  start: 1, # Integer | Index of the page of results to return
  limit: 1, # Integer | Maximum number of results per page
  sort: 'desc', # String | Date sort order: \"asc\" for ascending, \"desc\" for descending
  include_pending: false # Boolean | If pending transactions must be included
}

begin
  # Get Customer Account Transactions
  result = api_instance.get_customer_account_transactions(customer_id, account_id, from_date, to_date, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling TransactionsApi->get_customer_account_transactions: #{e}"
end
```

#### Using the get_customer_account_transactions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Transactions>, Integer, Hash)> get_customer_account_transactions_with_http_info(customer_id, account_id, from_date, to_date, opts)

```ruby
begin
  # Get Customer Account Transactions
  data, status_code, headers = api_instance.get_customer_account_transactions_with_http_info(customer_id, account_id, from_date, to_date, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Transactions>
rescue OpenBanking::ApiError => e
  puts "Error when calling TransactionsApi->get_customer_account_transactions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |
| **from_date** | **Integer** | A start date |  |
| **to_date** | **Integer** | A end date |  |
| **start** | **Integer** | Index of the page of results to return | [optional][default to 1] |
| **limit** | **Integer** | Maximum number of results per page | [optional][default to 25] |
| **sort** | **String** | Date sort order: \&quot;asc\&quot; for ascending, \&quot;desc\&quot; for descending | [optional][default to &#39;desc&#39;] |
| **include_pending** | **Boolean** | If pending transactions must be included | [optional][default to false] |

### Return type

[**Transactions**](Transactions.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customer_transaction

> <Transaction> get_customer_transaction(customer_id, transaction_id)

Get Customer Transaction by ID

Get details for the given transaction.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

### Examples

```ruby
require 'time'
require 'open_banking'
# setup authorization
OpenBanking.configure do |config|
  # Configure API key authorization: FinicityAppToken
  config.api_key['FinicityAppToken'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppToken'] = 'Bearer'

  # Configure API key authorization: FinicityAppKey
  config.api_key['FinicityAppKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppKey'] = 'Bearer'
end

api_instance = OpenBanking::TransactionsApi.new
customer_id = '1005061234' # String | A customer ID
transaction_id = 21284820852 # Integer | A transaction ID

begin
  # Get Customer Transaction by ID
  result = api_instance.get_customer_transaction(customer_id, transaction_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling TransactionsApi->get_customer_transaction: #{e}"
end
```

#### Using the get_customer_transaction_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Transaction>, Integer, Hash)> get_customer_transaction_with_http_info(customer_id, transaction_id)

```ruby
begin
  # Get Customer Transaction by ID
  data, status_code, headers = api_instance.get_customer_transaction_with_http_info(customer_id, transaction_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Transaction>
rescue OpenBanking::ApiError => e
  puts "Error when calling TransactionsApi->get_customer_transaction_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **transaction_id** | **Integer** | A transaction ID |  |

### Return type

[**Transaction**](Transaction.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## load_historic_transactions_for_customer_account

> load_historic_transactions_for_customer_account(customer_id, account_id)

Load Historic Transactions for Customer Account

Connect to the account's financial institution and load up to 24 months of historic transactions for the account. Length of history varies by institution.  This is a premium service. The billable event is a call to this service specifying a customer ID that has not been seen before by this service. (If this service is called multiple times with the same customer ID, to load transactions from multiple accounts, only one billable event has occurred.)  The recommended timeout setting for this request is 180 seconds in order to receive a response. However, you can terminate the connection after making the call the operation will still complete. You will have to pull the account records to check for an updated aggregation attempt date to know when the refresh is complete.  The date range sent to the institution is calculated from the account's `createdDate`. This means that calling this service a second time for the same account normally will not add any new transactions for the account. For this reason, a second call to this service for a known account ID will usually return immediately.  In a few specific scenarios, it may be desirable to force a second connection to the institution for a known account ID. Some examples are:  * The institution's policy has changed, making more transactions available * Finicity has now added a longer transaction history support for the institution * The first call encountered an error, and the resulting Aggregation Ticket has now been fixed by the Finicity Support Team  In these cases, the POST request can contain the parameter `force=true` in the request body to force the second connection.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

### Examples

```ruby
require 'time'
require 'open_banking'
# setup authorization
OpenBanking.configure do |config|
  # Configure API key authorization: FinicityAppToken
  config.api_key['FinicityAppToken'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppToken'] = 'Bearer'

  # Configure API key authorization: FinicityAppKey
  config.api_key['FinicityAppKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppKey'] = 'Bearer'
end

api_instance = OpenBanking::TransactionsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID

begin
  # Load Historic Transactions for Customer Account
  api_instance.load_historic_transactions_for_customer_account(customer_id, account_id)
rescue OpenBanking::ApiError => e
  puts "Error when calling TransactionsApi->load_historic_transactions_for_customer_account: #{e}"
end
```

#### Using the load_historic_transactions_for_customer_account_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> load_historic_transactions_for_customer_account_with_http_info(customer_id, account_id)

```ruby
begin
  # Load Historic Transactions for Customer Account
  data, status_code, headers = api_instance.load_historic_transactions_for_customer_account_with_http_info(customer_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling TransactionsApi->load_historic_transactions_for_customer_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |

### Return type

nil (empty response body)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain

