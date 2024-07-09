# OpenBanking::CustomersApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_customer**](CustomersApi.md#add_customer) | **POST** /aggregation/v2/customers/active | Add Customer |
| [**add_testing_customer**](CustomersApi.md#add_testing_customer) | **POST** /aggregation/v2/customers/testing | Add Testing Customer |
| [**delete_customer**](CustomersApi.md#delete_customer) | **DELETE** /aggregation/v1/customers/{customerId} | Delete Access to Customer by ID |
| [**get_customer**](CustomersApi.md#get_customer) | **GET** /aggregation/v1/customers/{customerId} | Get Customer by ID |
| [**get_customer_with_app_data**](CustomersApi.md#get_customer_with_app_data) | **GET** /aggregation/v1/customers/{customerId}/application | Get Customer With App Data by ID |
| [**get_customers**](CustomersApi.md#get_customers) | **GET** /aggregation/v1/customers | Get Customers |
| [**modify_customer**](CustomersApi.md#modify_customer) | **PUT** /aggregation/v1/customers/{customerId} | Modify Customer by ID |


## add_customer

> <CreatedCustomer> add_customer(new_customer)

Add Customer

Enroll an active customer, which is the actual owner of one or more real-world accounts. This is a billable customer.  Active customers must use the \"FinBank Billable\" profiles for testing purposes.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CustomersApi.new
new_customer = OpenBanking::NewCustomer.new({username: 'customerusername1'}) # NewCustomer | 

begin
  # Add Customer
  result = api_instance.add_customer(new_customer)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->add_customer: #{e}"
end
```

#### Using the add_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreatedCustomer>, Integer, Hash)> add_customer_with_http_info(new_customer)

```ruby
begin
  # Add Customer
  data, status_code, headers = api_instance.add_customer_with_http_info(new_customer)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreatedCustomer>
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->add_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **new_customer** | [**NewCustomer**](NewCustomer.md) |  |  |

### Return type

[**CreatedCustomer**](CreatedCustomer.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## add_testing_customer

> <CreatedCustomer> add_testing_customer(new_customer)

Add Testing Customer

Enroll a testing customer (Test Drive accounts).  For using testing customers with FinBank OAuth, you must register a test application with your systems engineer or account manager. Then, use that testing `applicationId` when creating testing customers.  Testing Customers can access FinBank profiles (except \"FinBank Billable\" profiles), and cannot access live financial institutions.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CustomersApi.new
new_customer = OpenBanking::NewCustomer.new({username: 'customerusername1'}) # NewCustomer | 

begin
  # Add Testing Customer
  result = api_instance.add_testing_customer(new_customer)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->add_testing_customer: #{e}"
end
```

#### Using the add_testing_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreatedCustomer>, Integer, Hash)> add_testing_customer_with_http_info(new_customer)

```ruby
begin
  # Add Testing Customer
  data, status_code, headers = api_instance.add_testing_customer_with_http_info(new_customer)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreatedCustomer>
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->add_testing_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **new_customer** | [**NewCustomer**](NewCustomer.md) |  |  |

### Return type

[**CreatedCustomer**](CreatedCustomer.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## delete_customer

> delete_customer(customer_id)

Delete Access to Customer by ID

Delete access to a customer and all associated accounts. This will delete access to the customer and all their linked accounts. The customer data will no longer be accessible. Any customer data already collected will be retained in accordance with our enterprise data retention policy consistent with legal and business purposes.  ⚠️ Use this service carefully! It will not pause for confirmation before performing the operation! _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CustomersApi.new
customer_id = '1005061234' # String | A customer ID

begin
  # Delete Access to Customer by ID
  api_instance.delete_customer(customer_id)
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->delete_customer: #{e}"
end
```

#### Using the delete_customer_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_customer_with_http_info(customer_id)

```ruby
begin
  # Delete Access to Customer by ID
  data, status_code, headers = api_instance.delete_customer_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->delete_customer_with_http_info: #{e}"
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


## get_customer

> <GetCustomer200Response> get_customer(customer_id)

Get Customer by ID

Retrieve a customer by ID.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CustomersApi.new
customer_id = '1005061234' # String | A customer ID

begin
  # Get Customer by ID
  result = api_instance.get_customer(customer_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->get_customer: #{e}"
end
```

#### Using the get_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<GetCustomer200Response>, Integer, Hash)> get_customer_with_http_info(customer_id)

```ruby
begin
  # Get Customer by ID
  data, status_code, headers = api_instance.get_customer_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <GetCustomer200Response>
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->get_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |

### Return type

[**GetCustomer200Response**](GetCustomer200Response.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customer_with_app_data

> <CustomerWithAppData> get_customer_with_app_data(customer_id)

Get Customer With App Data by ID

Retrieve a customer along with additional details about the OAuth application.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CustomersApi.new
customer_id = '1005061234' # String | A customer ID

begin
  # Get Customer With App Data by ID
  result = api_instance.get_customer_with_app_data(customer_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->get_customer_with_app_data: #{e}"
end
```

#### Using the get_customer_with_app_data_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerWithAppData>, Integer, Hash)> get_customer_with_app_data_with_http_info(customer_id)

```ruby
begin
  # Get Customer With App Data by ID
  data, status_code, headers = api_instance.get_customer_with_app_data_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerWithAppData>
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->get_customer_with_app_data_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |

### Return type

[**CustomerWithAppData**](CustomerWithAppData.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_customers

> <Customers> get_customers(opts)

Get Customers

Find all customers enrolled by the current partner, where the search text is found in the customer's username or any combination of `firstName` and `lastName` fields. If no search text is provided, all customers will be returned.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CustomersApi.new
opts = {
  username: 'customerusername1', # String | Username for exact match (will return 0 or 1 record)
  type: 'active', # String | \"testing\" or \"active\" to return only customers of that type, or leave empty to return all customers
  search: 'Search Value', # String | The text you wish to match. Leave this empty if you wish to return all customers. Must be URL-encoded (see: [Handling Spaces in Queries](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/)).
  start: 1, # Integer | Index of the page of results to return
  limit: 1 # Integer | Maximum number of results per page
}

begin
  # Get Customers
  result = api_instance.get_customers(opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->get_customers: #{e}"
end
```

#### Using the get_customers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Customers>, Integer, Hash)> get_customers_with_http_info(opts)

```ruby
begin
  # Get Customers
  data, status_code, headers = api_instance.get_customers_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Customers>
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->get_customers_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** | Username for exact match (will return 0 or 1 record) | [optional] |
| **type** | **String** | \&quot;testing\&quot; or \&quot;active\&quot; to return only customers of that type, or leave empty to return all customers | [optional] |
| **search** | **String** | The text you wish to match. Leave this empty if you wish to return all customers. Must be URL-encoded (see: [Handling Spaces in Queries](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/)). | [optional] |
| **start** | **Integer** | Index of the page of results to return | [optional][default to 1] |
| **limit** | **Integer** | Maximum number of results per page | [optional][default to 25] |

### Return type

[**Customers**](Customers.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## modify_customer

> modify_customer(customer_id, customer_update)

Modify Customer by ID

Modify an enrolled customer by ID.  You must specify either `firstName`, `lastName`, or both in the request.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CustomersApi.new
customer_id = '1005061234' # String | A customer ID
customer_update = OpenBanking::CustomerUpdate.new # CustomerUpdate | 

begin
  # Modify Customer by ID
  api_instance.modify_customer(customer_id, customer_update)
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->modify_customer: #{e}"
end
```

#### Using the modify_customer_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> modify_customer_with_http_info(customer_id, customer_update)

```ruby
begin
  # Modify Customer by ID
  data, status_code, headers = api_instance.modify_customer_with_http_info(customer_id, customer_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomersApi->modify_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **customer_update** | [**CustomerUpdate**](CustomerUpdate.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain

