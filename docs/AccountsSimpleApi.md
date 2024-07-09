# OpenBanking::AccountsSimpleApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_customer_account_simple**](AccountsSimpleApi.md#get_customer_account_simple) | **GET** /aggregation/v1/customers/{customerId}/accounts/{accountId}/simple | Get Customer Account by ID (Simple) |
| [**get_customer_accounts_by_institution_login_simple**](AccountsSimpleApi.md#get_customer_accounts_by_institution_login_simple) | **GET** /aggregation/v1/customers/{customerId}/institutionLogins/{institutionLoginId}/accounts/simple | Get Customer Accounts by Institution Login ID (Simple) |
| [**get_customer_accounts_by_institution_simple**](AccountsSimpleApi.md#get_customer_accounts_by_institution_simple) | **GET** /aggregation/v1/customers/{customerId}/institutions/{institutionId}/accounts/simple | Get Customer Accounts by Institution ID (Simple) |
| [**get_customer_accounts_simple**](AccountsSimpleApi.md#get_customer_accounts_simple) | **GET** /aggregation/v1/customers/{customerId}/accounts/simple | Get Customer Accounts (Simple) |


## get_customer_account_simple

> <CustomerAccountSimple> get_customer_account_simple(customer_id, account_id)

Get Customer Account by ID (Simple)

This API is a lighter version of Get Customer Accounts by ID, returning only basic information of a customer account.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsSimpleApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID

begin
  # Get Customer Account by ID (Simple)
  result = api_instance.get_customer_account_simple(customer_id, account_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsSimpleApi->get_customer_account_simple: #{e}"
end
```

#### Using the get_customer_account_simple_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccountSimple>, Integer, Hash)> get_customer_account_simple_with_http_info(customer_id, account_id)

```ruby
begin
  # Get Customer Account by ID (Simple)
  data, status_code, headers = api_instance.get_customer_account_simple_with_http_info(customer_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccountSimple>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsSimpleApi->get_customer_account_simple_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |

### Return type

[**CustomerAccountSimple**](CustomerAccountSimple.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customer_accounts_by_institution_login_simple

> <CustomerAccountsSimple> get_customer_accounts_by_institution_login_simple(customer_id, institution_login_id)

Get Customer Accounts by Institution Login ID (Simple)

This API is a lighter version of Get Customer Accounts by Institution Login ID, returning only basic information of all active accounts owned by the given customer at the given institution login ID.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsSimpleApi.new
customer_id = '1005061234' # String | A customer ID
institution_login_id = '1007302745' # String | The institution login ID

begin
  # Get Customer Accounts by Institution Login ID (Simple)
  result = api_instance.get_customer_accounts_by_institution_login_simple(customer_id, institution_login_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsSimpleApi->get_customer_accounts_by_institution_login_simple: #{e}"
end
```

#### Using the get_customer_accounts_by_institution_login_simple_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccountsSimple>, Integer, Hash)> get_customer_accounts_by_institution_login_simple_with_http_info(customer_id, institution_login_id)

```ruby
begin
  # Get Customer Accounts by Institution Login ID (Simple)
  data, status_code, headers = api_instance.get_customer_accounts_by_institution_login_simple_with_http_info(customer_id, institution_login_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccountsSimple>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsSimpleApi->get_customer_accounts_by_institution_login_simple_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **institution_login_id** | **String** | The institution login ID |  |

### Return type

[**CustomerAccountsSimple**](CustomerAccountsSimple.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customer_accounts_by_institution_simple

> <CustomerAccountsSimple> get_customer_accounts_by_institution_simple(customer_id, institution_id)

Get Customer Accounts by Institution ID (Simple)

This API is a lighter version of Get Customer Accounts by Institution ID, returning only basic information of active accounts owned by the given customer at the given institution.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsSimpleApi.new
customer_id = '1005061234' # String | A customer ID
institution_id = 4222 # Integer | The institution ID

begin
  # Get Customer Accounts by Institution ID (Simple)
  result = api_instance.get_customer_accounts_by_institution_simple(customer_id, institution_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsSimpleApi->get_customer_accounts_by_institution_simple: #{e}"
end
```

#### Using the get_customer_accounts_by_institution_simple_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccountsSimple>, Integer, Hash)> get_customer_accounts_by_institution_simple_with_http_info(customer_id, institution_id)

```ruby
begin
  # Get Customer Accounts by Institution ID (Simple)
  data, status_code, headers = api_instance.get_customer_accounts_by_institution_simple_with_http_info(customer_id, institution_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccountsSimple>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsSimpleApi->get_customer_accounts_by_institution_simple_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **institution_id** | **Integer** | The institution ID |  |

### Return type

[**CustomerAccountsSimple**](CustomerAccountsSimple.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customer_accounts_simple

> <CustomerAccountsSimple> get_customer_accounts_simple(customer_id)

Get Customer Accounts (Simple)

This API is a lighter version of Get Customer Accounts, returning only basic information of all active customer accounts.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsSimpleApi.new
customer_id = '1005061234' # String | A customer ID

begin
  # Get Customer Accounts (Simple)
  result = api_instance.get_customer_accounts_simple(customer_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsSimpleApi->get_customer_accounts_simple: #{e}"
end
```

#### Using the get_customer_accounts_simple_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccountsSimple>, Integer, Hash)> get_customer_accounts_simple_with_http_info(customer_id)

```ruby
begin
  # Get Customer Accounts (Simple)
  data, status_code, headers = api_instance.get_customer_accounts_simple_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccountsSimple>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsSimpleApi->get_customer_accounts_simple_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |

### Return type

[**CustomerAccountsSimple**](CustomerAccountsSimple.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain

