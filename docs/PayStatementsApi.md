# OpenBanking::PayStatementsApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**store_customer_pay_statement**](PayStatementsApi.md#store_customer_pay_statement) | **POST** /aggregation/v1/customers/{customerId}/payStatements | Store Customer Pay Statement |


## store_customer_pay_statement

> <Asset> store_customer_pay_statement(customer_id, pay_statement)

Store Customer Pay Statement

Upload pay statements for a customer.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::PayStatementsApi.new
customer_id = '1005061234' # String | A customer ID
pay_statement = OpenBanking::PayStatement.new({label: 'lastPayPeriod', statement: 'VGhpcyBtdXN0IGJlIGFuIGltYWdl'}) # PayStatement | 

begin
  # Store Customer Pay Statement
  result = api_instance.store_customer_pay_statement(customer_id, pay_statement)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PayStatementsApi->store_customer_pay_statement: #{e}"
end
```

#### Using the store_customer_pay_statement_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Asset>, Integer, Hash)> store_customer_pay_statement_with_http_info(customer_id, pay_statement)

```ruby
begin
  # Store Customer Pay Statement
  data, status_code, headers = api_instance.store_customer_pay_statement_with_http_info(customer_id, pay_statement)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Asset>
rescue OpenBanking::ApiError => e
  puts "Error when calling PayStatementsApi->store_customer_pay_statement_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **pay_statement** | [**PayStatement**](PayStatement.md) |  |  |

### Return type

[**Asset**](Asset.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain

