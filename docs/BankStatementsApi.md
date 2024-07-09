# OpenBanking::BankStatementsApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**generate_statement_report**](BankStatementsApi.md#generate_statement_report) | **POST** /decisioning/v2/customers/{customerId}/statement | Generate Statement Report |
| [**get_customer_account_multiple_statement**](BankStatementsApi.md#get_customer_account_multiple_statement) | **GET** /aggregation/v3/customers/{customerId}/accounts/{accountId}/statement | Get Customer Account Multiple Statements |
| [**get_customer_account_statement**](BankStatementsApi.md#get_customer_account_statement) | **GET** /aggregation/v1/customers/{customerId}/accounts/{accountId}/statement | Get Customer Account Statement |


## generate_statement_report

> <StatementReportAck> generate_statement_report(customer_id, statement_report_constraints, opts)

Generate Statement Report

Generate a Statement Report for the given accounts under the given customer.  This is a premium service. A billable event will be created upon the successful generation of the Statement Report.  Before calling this API, a consumer must be created for the given customer ID (see Consumers APIs).  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::BankStatementsApi.new
customer_id = '1005061234' # String | A customer ID
statement_report_constraints = OpenBanking::StatementReportConstraints.new({statement_report_data: OpenBanking::StatementData.new({account_id: 5011648377})}) # StatementReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate Statement Report
  result = api_instance.generate_statement_report(customer_id, statement_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling BankStatementsApi->generate_statement_report: #{e}"
end
```

#### Using the generate_statement_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StatementReportAck>, Integer, Hash)> generate_statement_report_with_http_info(customer_id, statement_report_constraints, opts)

```ruby
begin
  # Generate Statement Report
  data, status_code, headers = api_instance.generate_statement_report_with_http_info(customer_id, statement_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StatementReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling BankStatementsApi->generate_statement_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **statement_report_constraints** | [**StatementReportConstraints**](StatementReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**StatementReportAck**](StatementReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## get_customer_account_multiple_statement

> <CustomerAccountMultipleStatements> get_customer_account_multiple_statement(customer_id, account_id, opts)

Get Customer Account Multiple Statements

This endpoint retrieves account statements for a given customer. The maximum number of statements that can be returned is 24.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::BankStatementsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID
opts = {
  index: '1,2,3,4,5,6' # String | Request statements with comma-separated indexes between 1-24. The default value is 1 and it will return the most recent statement. Increasing the index will return older statements, for example, setting the index value to 6 will return the sixth most recent statement.
}

begin
  # Get Customer Account Multiple Statements
  result = api_instance.get_customer_account_multiple_statement(customer_id, account_id, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling BankStatementsApi->get_customer_account_multiple_statement: #{e}"
end
```

#### Using the get_customer_account_multiple_statement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccountMultipleStatements>, Integer, Hash)> get_customer_account_multiple_statement_with_http_info(customer_id, account_id, opts)

```ruby
begin
  # Get Customer Account Multiple Statements
  data, status_code, headers = api_instance.get_customer_account_multiple_statement_with_http_info(customer_id, account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccountMultipleStatements>
rescue OpenBanking::ApiError => e
  puts "Error when calling BankStatementsApi->get_customer_account_multiple_statement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |
| **index** | **String** | Request statements with comma-separated indexes between 1-24. The default value is 1 and it will return the most recent statement. Increasing the index will return older statements, for example, setting the index value to 6 will return the sixth most recent statement. | [optional][default to &#39;1&#39;] |

### Return type

[**CustomerAccountMultipleStatements**](CustomerAccountMultipleStatements.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customer_account_statement

> File get_customer_account_statement(customer_id, account_id, opts)

Get Customer Account Statement

Retrieve the customer's bank statements in PDF format. Up to 24 months of history is available depending on the financial institution. Since this is a premium service, charges incur per each successful statement retrieved.  For certified financial institutions, statements are available for the following account types: * Checking * Savings * Money market * CDs * Investments * Mortgage * Credit cards * Loans * Line of credit * Student Loans  Note: setting the timeout to 180 seconds is recommended to allow enough time for a response.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::BankStatementsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID
opts = {
  index: 1, # Integer | Request statements from 1-24. By default, 1 is the most recent statement. Increase the index value to count back (by month) and retrieve its most recent statement.
  type: 'taxStatement' # String | The type of statement to retrieve
}

begin
  # Get Customer Account Statement
  result = api_instance.get_customer_account_statement(customer_id, account_id, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling BankStatementsApi->get_customer_account_statement: #{e}"
end
```

#### Using the get_customer_account_statement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(File, Integer, Hash)> get_customer_account_statement_with_http_info(customer_id, account_id, opts)

```ruby
begin
  # Get Customer Account Statement
  data, status_code, headers = api_instance.get_customer_account_statement_with_http_info(customer_id, account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => File
rescue OpenBanking::ApiError => e
  puts "Error when calling BankStatementsApi->get_customer_account_statement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |
| **index** | **Integer** | Request statements from 1-24. By default, 1 is the most recent statement. Increase the index value to count back (by month) and retrieve its most recent statement. | [optional][default to 1] |
| **type** | **String** | The type of statement to retrieve | [optional] |

### Return type

**File**

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream, application/json, text/plain

