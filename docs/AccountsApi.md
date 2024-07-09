# OpenBanking::AccountsApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_customer_account**](AccountsApi.md#delete_customer_account) | **DELETE** /aggregation/v1/customers/{customerId}/accounts/{accountId} | Delete Access to Customer Account by ID |
| [**delete_customer_accounts_by_institution_login**](AccountsApi.md#delete_customer_accounts_by_institution_login) | **DELETE** /aggregation/v1/customers/{customerId}/institutionLogins/{institutionLoginId} | Delete Access to Customer Accounts by Institution Login ID |
| [**get_customer_account**](AccountsApi.md#get_customer_account) | **GET** /aggregation/v2/customers/{customerId}/accounts/{accountId} | Get Customer Account by ID |
| [**get_customer_accounts**](AccountsApi.md#get_customer_accounts) | **GET** /aggregation/v1/customers/{customerId}/accounts | Get Customer Accounts |
| [**get_customer_accounts_by_institution**](AccountsApi.md#get_customer_accounts_by_institution) | **GET** /aggregation/v1/customers/{customerId}/institutions/{institutionId}/accounts | Get Customer Accounts by Institution ID |
| [**get_customer_accounts_by_institution_login**](AccountsApi.md#get_customer_accounts_by_institution_login) | **GET** /aggregation/v1/customers/{customerId}/institutionLogins/{institutionLoginId}/accounts | Get Customer Accounts by Institution Login ID |
| [**refresh_customer_accounts**](AccountsApi.md#refresh_customer_accounts) | **POST** /aggregation/v1/customers/{customerId}/accounts | Refresh Customer Accounts |
| [**refresh_customer_accounts_by_institution_login**](AccountsApi.md#refresh_customer_accounts_by_institution_login) | **POST** /aggregation/v1/customers/{customerId}/institutionLogins/{institutionLoginId}/accounts | Refresh Customer Accounts by Institution Login ID |
| [**refresh_customer_accounts_by_institution_login_v2**](AccountsApi.md#refresh_customer_accounts_by_institution_login_v2) | **POST** /aggregation/v2/customers/{customerId}/institutionLogins/{institutionLoginId}/accounts | Refresh Customer Account by Institution Login ID for Data Access Tiers |
| [**refresh_customer_accounts_v2**](AccountsApi.md#refresh_customer_accounts_v2) | **POST** /aggregation/v2/customers/{customerId}/accounts | Refresh Customer Accounts for Data Access Tiers |


## delete_customer_account

> delete_customer_account(customer_id, account_id)

Delete Access to Customer Account by ID

This will delete access to a specific account only. If the given account is not the last account, then partners and their customers will have the flexibility to continue to access data from other connected accounts using the consented (Oauth) token for the customer. The customer data on that specific account will no longer be accessible. Any customer data already collected will be retained in accordance with our enterprise retention policy consistent with legal and business purposes. ​ _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID

begin
  # Delete Access to Customer Account by ID
  api_instance.delete_customer_account(customer_id, account_id)
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->delete_customer_account: #{e}"
end
```

#### Using the delete_customer_account_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_customer_account_with_http_info(customer_id, account_id)

```ruby
begin
  # Delete Access to Customer Account by ID
  data, status_code, headers = api_instance.delete_customer_account_with_http_info(customer_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->delete_customer_account_with_http_info: #{e}"
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


## delete_customer_accounts_by_institution_login

> delete_customer_accounts_by_institution_login(customer_id, institution_login_id)

Delete Access to Customer Accounts by Institution Login ID

Delete access to all customer accounts for a given FI.​ This will delete access to the underlying account(s) under a given Institution Login ID. The customer data will no longer be accessible. Any customer data already collected will be retained in accordance with our enterprise retention policy consistent with legal and business purposes. _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsApi.new
customer_id = '1005061234' # String | A customer ID
institution_login_id = '1007302745' # String | The institution login ID

begin
  # Delete Access to Customer Accounts by Institution Login ID
  api_instance.delete_customer_accounts_by_institution_login(customer_id, institution_login_id)
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->delete_customer_accounts_by_institution_login: #{e}"
end
```

#### Using the delete_customer_accounts_by_institution_login_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_customer_accounts_by_institution_login_with_http_info(customer_id, institution_login_id)

```ruby
begin
  # Delete Access to Customer Accounts by Institution Login ID
  data, status_code, headers = api_instance.delete_customer_accounts_by_institution_login_with_http_info(customer_id, institution_login_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->delete_customer_accounts_by_institution_login_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **institution_login_id** | **String** | The institution login ID |  |

### Return type

nil (empty response body)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customer_account

> <CustomerAccount> get_customer_account(customer_id, account_id)

Get Customer Account by ID

Get a customer account by ID.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID

begin
  # Get Customer Account by ID
  result = api_instance.get_customer_account(customer_id, account_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->get_customer_account: #{e}"
end
```

#### Using the get_customer_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccount>, Integer, Hash)> get_customer_account_with_http_info(customer_id, account_id)

```ruby
begin
  # Get Customer Account by ID
  data, status_code, headers = api_instance.get_customer_account_with_http_info(customer_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccount>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->get_customer_account_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |

### Return type

[**CustomerAccount**](CustomerAccount.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customer_accounts

> <CustomerAccounts> get_customer_accounts(customer_id, opts)

Get Customer Accounts

Get all accounts owned by the given customer.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsApi.new
customer_id = '1005061234' # String | A customer ID
opts = {
  status: 'pending', # String | A filter to fetch account in the given status
  account_type: 'ava' # String | A filter to fetch accounts for the given type. Currently supported types: \"ava\"
}

begin
  # Get Customer Accounts
  result = api_instance.get_customer_accounts(customer_id, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->get_customer_accounts: #{e}"
end
```

#### Using the get_customer_accounts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccounts>, Integer, Hash)> get_customer_accounts_with_http_info(customer_id, opts)

```ruby
begin
  # Get Customer Accounts
  data, status_code, headers = api_instance.get_customer_accounts_with_http_info(customer_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccounts>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->get_customer_accounts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **status** | **String** | A filter to fetch account in the given status | [optional] |
| **account_type** | **String** | A filter to fetch accounts for the given type. Currently supported types: \&quot;ava\&quot; | [optional] |

### Return type

[**CustomerAccounts**](CustomerAccounts.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customer_accounts_by_institution

> <CustomerAccounts> get_customer_accounts_by_institution(customer_id, institution_id)

Get Customer Accounts by Institution ID

Get all active accounts owned by the given customer at the given institution.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsApi.new
customer_id = '1005061234' # String | A customer ID
institution_id = 4222 # Integer | The institution ID

begin
  # Get Customer Accounts by Institution ID
  result = api_instance.get_customer_accounts_by_institution(customer_id, institution_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->get_customer_accounts_by_institution: #{e}"
end
```

#### Using the get_customer_accounts_by_institution_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccounts>, Integer, Hash)> get_customer_accounts_by_institution_with_http_info(customer_id, institution_id)

```ruby
begin
  # Get Customer Accounts by Institution ID
  data, status_code, headers = api_instance.get_customer_accounts_by_institution_with_http_info(customer_id, institution_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccounts>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->get_customer_accounts_by_institution_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **institution_id** | **Integer** | The institution ID |  |

### Return type

[**CustomerAccounts**](CustomerAccounts.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customer_accounts_by_institution_login

> <CustomerAccounts> get_customer_accounts_by_institution_login(customer_id, institution_login_id)

Get Customer Accounts by Institution Login ID

Get all accounts associated with the given institution login. All accounts returned are accessible by a single set of credentials on a single institution.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsApi.new
customer_id = '1005061234' # String | A customer ID
institution_login_id = '1007302745' # String | The institution login ID

begin
  # Get Customer Accounts by Institution Login ID
  result = api_instance.get_customer_accounts_by_institution_login(customer_id, institution_login_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->get_customer_accounts_by_institution_login: #{e}"
end
```

#### Using the get_customer_accounts_by_institution_login_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccounts>, Integer, Hash)> get_customer_accounts_by_institution_login_with_http_info(customer_id, institution_login_id)

```ruby
begin
  # Get Customer Accounts by Institution Login ID
  data, status_code, headers = api_instance.get_customer_accounts_by_institution_login_with_http_info(customer_id, institution_login_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccounts>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->get_customer_accounts_by_institution_login_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **institution_login_id** | **String** | The institution login ID |  |

### Return type

[**CustomerAccounts**](CustomerAccounts.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## refresh_customer_accounts

> <CustomerAccounts> refresh_customer_accounts(customer_id)

Refresh Customer Accounts

Refresh account and transaction data for all accounts associated with the  given `customerId` with a connection to the institution.  Client apps are not permitted to automate calls to the Refresh services. Active accounts are automatically refreshed by Finicity once per day. Because many financial institutions only post transactions once per day, calling Refresh services repeatedly is usually a waste of resources and is not recommended.  Apps may call Refresh services for a specific customer when there is a specific business case for the need of data that is up to date as of the moment. Please discuss with your account manager and systems engineer for further clarification.  The recommended timeout setting for this request is 120 seconds in order to receive a response. However, you can terminate the connection after making the call the operation will still complete. You will have to pull the account records to check for an updated aggregation attempt date to know when the refresh is complete.  Note: This service is not available for all Data Access Tiers.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsApi.new
customer_id = '1005061234' # String | A customer ID

begin
  # Refresh Customer Accounts
  result = api_instance.refresh_customer_accounts(customer_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->refresh_customer_accounts: #{e}"
end
```

#### Using the refresh_customer_accounts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccounts>, Integer, Hash)> refresh_customer_accounts_with_http_info(customer_id)

```ruby
begin
  # Refresh Customer Accounts
  data, status_code, headers = api_instance.refresh_customer_accounts_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccounts>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->refresh_customer_accounts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |

### Return type

[**CustomerAccounts**](CustomerAccounts.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## refresh_customer_accounts_by_institution_login

> <CustomerAccounts> refresh_customer_accounts_by_institution_login(customer_id, institution_login_id)

Refresh Customer Accounts by Institution Login ID

Refresh account and transaction data for all accounts associated with a given `institutionLoginId` with a connection to the institution.  Client apps are not permitted to automate calls to the Refresh services. Active accounts are automatically refreshed by Finicity once per day. Because many financial institutions only post transactions once per day, calling Refresh repeatedly is usually a waste of resources and is not recommended.  Apps may call Refresh services for a specific customer when there is a specific business case for the need of data that is up to date as of the moment. Please discuss with your account manager and systems engineer for further clarification.  The recommended timeout setting for this request is 120 seconds in order to receive a response. However, you can terminate the connection after making the call the operation will still complete. You will have to pull the account records to check for an updated aggregation attempt date to know when the refresh is complete.  Note: This service is not available for all Data Access Tiers.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsApi.new
customer_id = '1005061234' # String | A customer ID
institution_login_id = '1007302745' # String | The institution login ID

begin
  # Refresh Customer Accounts by Institution Login ID
  result = api_instance.refresh_customer_accounts_by_institution_login(customer_id, institution_login_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->refresh_customer_accounts_by_institution_login: #{e}"
end
```

#### Using the refresh_customer_accounts_by_institution_login_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccounts>, Integer, Hash)> refresh_customer_accounts_by_institution_login_with_http_info(customer_id, institution_login_id)

```ruby
begin
  # Refresh Customer Accounts by Institution Login ID
  data, status_code, headers = api_instance.refresh_customer_accounts_by_institution_login_with_http_info(customer_id, institution_login_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccounts>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->refresh_customer_accounts_by_institution_login_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **institution_login_id** | **String** | The institution login ID |  |

### Return type

[**CustomerAccounts**](CustomerAccounts.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## refresh_customer_accounts_by_institution_login_v2

> refresh_customer_accounts_by_institution_login_v2(customer_id, institution_login_id)

Refresh Customer Account by Institution Login ID for Data Access Tiers

Refresh account and transaction data for all accounts associated with a given 'institutionLoginId` with a connection to the institution. Client apps are not permitted to automate calls to the Refresh services. Active accounts are automatically refreshed by Finicity once per day.  Apps may call Refresh services for a specific customer when there is a specific business case for the need of data that is up to date as of the moment. Please discuss with your account manager and systems engineer for further clarification.  Note: This service will be used for Data Access Tiers ASD, AFD and ATD.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsApi.new
customer_id = '1005061234' # String | A customer ID
institution_login_id = '1007302745' # String | The institution login ID

begin
  # Refresh Customer Account by Institution Login ID for Data Access Tiers
  api_instance.refresh_customer_accounts_by_institution_login_v2(customer_id, institution_login_id)
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->refresh_customer_accounts_by_institution_login_v2: #{e}"
end
```

#### Using the refresh_customer_accounts_by_institution_login_v2_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> refresh_customer_accounts_by_institution_login_v2_with_http_info(customer_id, institution_login_id)

```ruby
begin
  # Refresh Customer Account by Institution Login ID for Data Access Tiers
  data, status_code, headers = api_instance.refresh_customer_accounts_by_institution_login_v2_with_http_info(customer_id, institution_login_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->refresh_customer_accounts_by_institution_login_v2_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **institution_login_id** | **String** | The institution login ID |  |

### Return type

nil (empty response body)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## refresh_customer_accounts_v2

> refresh_customer_accounts_v2(customer_id)

Refresh Customer Accounts for Data Access Tiers

Refresh account and transaction data for all accounts associated with the  given `customerId` with a connection to the institution.  Client apps are not permitted to automate calls to the Refresh services. Active accounts are automatically refreshed by Finicity once per day. Apps may call Refresh services for a specific customer when there is a specific business case for the need of data that is up to date as of the moment. Please discuss with your account manager and systems engineer for further clarification.  Note: This service will be used for Data Access Tiers ASD, AFD and ATD.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountsApi.new
customer_id = '1005061234' # String | A customer ID

begin
  # Refresh Customer Accounts for Data Access Tiers
  api_instance.refresh_customer_accounts_v2(customer_id)
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->refresh_customer_accounts_v2: #{e}"
end
```

#### Using the refresh_customer_accounts_v2_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> refresh_customer_accounts_v2_with_http_info(customer_id)

```ruby
begin
  # Refresh Customer Accounts for Data Access Tiers
  data, status_code, headers = api_instance.refresh_customer_accounts_v2_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountsApi->refresh_customer_accounts_v2_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |

### Return type

nil (empty response body)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain

