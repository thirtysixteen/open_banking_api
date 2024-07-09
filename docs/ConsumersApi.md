# OpenBanking::ConsumersApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_consumer**](ConsumersApi.md#create_consumer) | **POST** /decisioning/v1/customers/{customerId}/consumer | Create Consumer |
| [**get_consumer**](ConsumersApi.md#get_consumer) | **GET** /decisioning/v1/consumers/{consumerId} | Get Consumer by ID |
| [**get_consumer_for_customer**](ConsumersApi.md#get_consumer_for_customer) | **GET** /decisioning/v1/customers/{customerId}/consumer | Get Consumer For Customer |
| [**modify_consumer**](ConsumersApi.md#modify_consumer) | **PUT** /decisioning/v1/consumers/{consumerId} | Modify Consumer by ID |


## create_consumer

> <CreatedConsumer> create_consumer(customer_id, new_consumer)

Create Consumer

Create a consumer record associated with the given customer. A consumer persists as the owner of any reports that are generated, even after the original customer is deleted from the system.  A consumer must be created for the given customer before calling any of the Generate Report services.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::ConsumersApi.new
customer_id = '1005061234' # String | A customer ID
new_consumer = OpenBanking::NewConsumer.new({first_name: 'John', last_name: 'Smith', address: '434 W Ascension Way Suite #200 Murray UT 84123', city: 'Murray', state: 'UT', zip: '84123', phone: '1-801-984-4200', ssn: '999-99-9999', birthday: OpenBanking::Birthday.new}) # NewConsumer | 

begin
  # Create Consumer
  result = api_instance.create_consumer(customer_id, new_consumer)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ConsumersApi->create_consumer: #{e}"
end
```

#### Using the create_consumer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreatedConsumer>, Integer, Hash)> create_consumer_with_http_info(customer_id, new_consumer)

```ruby
begin
  # Create Consumer
  data, status_code, headers = api_instance.create_consumer_with_http_info(customer_id, new_consumer)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreatedConsumer>
rescue OpenBanking::ApiError => e
  puts "Error when calling ConsumersApi->create_consumer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **new_consumer** | [**NewConsumer**](NewConsumer.md) |  |  |

### Return type

[**CreatedConsumer**](CreatedConsumer.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## get_consumer

> <Consumer> get_consumer(consumer_id)

Get Consumer by ID

Get the details of a consumer record by consumer ID.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::ConsumersApi.new
consumer_id = '0bf46322c167b562e6cbed9d40e19a4c' # String | The consumer ID

begin
  # Get Consumer by ID
  result = api_instance.get_consumer(consumer_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ConsumersApi->get_consumer: #{e}"
end
```

#### Using the get_consumer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Consumer>, Integer, Hash)> get_consumer_with_http_info(consumer_id)

```ruby
begin
  # Get Consumer by ID
  data, status_code, headers = api_instance.get_consumer_with_http_info(consumer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Consumer>
rescue OpenBanking::ApiError => e
  puts "Error when calling ConsumersApi->get_consumer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **consumer_id** | **String** | The consumer ID |  |

### Return type

[**Consumer**](Consumer.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_consumer_for_customer

> <Consumer> get_consumer_for_customer(customer_id)

Get Consumer For Customer

Get the details of a consumer record by customer ID.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::ConsumersApi.new
customer_id = '1005061234' # String | A customer ID

begin
  # Get Consumer For Customer
  result = api_instance.get_consumer_for_customer(customer_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ConsumersApi->get_consumer_for_customer: #{e}"
end
```

#### Using the get_consumer_for_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Consumer>, Integer, Hash)> get_consumer_for_customer_with_http_info(customer_id)

```ruby
begin
  # Get Consumer For Customer
  data, status_code, headers = api_instance.get_consumer_for_customer_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Consumer>
rescue OpenBanking::ApiError => e
  puts "Error when calling ConsumersApi->get_consumer_for_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |

### Return type

[**Consumer**](Consumer.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## modify_consumer

> modify_consumer(consumer_id, consumer_update)

Modify Consumer by ID

Modify an existing consumer. All fields are required for a consumer record, but individual fields for this call are optional because fields that are not specified will be left unchanged.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::ConsumersApi.new
consumer_id = '0bf46322c167b562e6cbed9d40e19a4c' # String | The consumer ID
consumer_update = OpenBanking::ConsumerUpdate.new # ConsumerUpdate | 

begin
  # Modify Consumer by ID
  api_instance.modify_consumer(consumer_id, consumer_update)
rescue OpenBanking::ApiError => e
  puts "Error when calling ConsumersApi->modify_consumer: #{e}"
end
```

#### Using the modify_consumer_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> modify_consumer_with_http_info(consumer_id, consumer_update)

```ruby
begin
  # Modify Consumer by ID
  data, status_code, headers = api_instance.modify_consumer_with_http_info(consumer_id, consumer_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling ConsumersApi->modify_consumer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **consumer_id** | **String** | The consumer ID |  |
| **consumer_update** | [**ConsumerUpdate**](ConsumerUpdate.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain

