# OpenBanking::BusinessesAPIApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_business_details**](BusinessesAPIApi.md#add_business_details) | **POST** /business-services/customers/{customer_id}/businesses | Create a New Business for a Customer |
| [**get_business_by_customer**](BusinessesAPIApi.md#get_business_by_customer) | **GET** /business-services/customers/{customer_id}/businesses | Get Business for Customer |
| [**get_business_by_id**](BusinessesAPIApi.md#get_business_by_id) | **GET** /business-services/businesses/{business_id} | Get Business by ID |
| [**update_business**](BusinessesAPIApi.md#update_business) | **PUT** /business-services/businesses/{business_id} | Update Business by ID |


## add_business_details

> <Business> add_business_details(customer_id, new_business)

Create a New Business for a Customer

Create a new business record for the associated customer. A customer can have one business record associated.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::BusinessesAPIApi.new
customer_id = '1005061234' # String | Unique identifier of the customer
new_business = OpenBanking::NewBusiness.new({name: 'ABC Tires Inc', personally_liable: true, address: OpenBanking::NewAddress.new, phone_number: OpenBanking::PhoneNumberFormat.new}) # NewBusiness | 

begin
  # Create a New Business for a Customer
  result = api_instance.add_business_details(customer_id, new_business)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling BusinessesAPIApi->add_business_details: #{e}"
end
```

#### Using the add_business_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Business>, Integer, Hash)> add_business_details_with_http_info(customer_id, new_business)

```ruby
begin
  # Create a New Business for a Customer
  data, status_code, headers = api_instance.add_business_details_with_http_info(customer_id, new_business)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Business>
rescue OpenBanking::ApiError => e
  puts "Error when calling BusinessesAPIApi->add_business_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | Unique identifier of the customer |  |
| **new_business** | [**NewBusiness**](NewBusiness.md) |  |  |

### Return type

[**Business**](Business.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_business_by_customer

> <Array<Business>> get_business_by_customer(customer_id)

Get Business for Customer

Retrieve business details associated with a specific customer. By providing the unique customer identifier, details about the associated business can be accessed.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::BusinessesAPIApi.new
customer_id = '1005061234' # String | Unique identifier of the customer

begin
  # Get Business for Customer
  result = api_instance.get_business_by_customer(customer_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling BusinessesAPIApi->get_business_by_customer: #{e}"
end
```

#### Using the get_business_by_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Business>>, Integer, Hash)> get_business_by_customer_with_http_info(customer_id)

```ruby
begin
  # Get Business for Customer
  data, status_code, headers = api_instance.get_business_by_customer_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Business>>
rescue OpenBanking::ApiError => e
  puts "Error when calling BusinessesAPIApi->get_business_by_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | Unique identifier of the customer |  |

### Return type

[**Array&lt;Business&gt;**](Business.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_business_by_id

> <Array<Business>> get_business_by_id(business_id)

Get Business by ID

Retrieve business details.  _Supported regions_: ![\\U0001F1FA\\U0001F1F8](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::BusinessesAPIApi.new
business_id = '192323' # String | Unique identifier of the business

begin
  # Get Business by ID
  result = api_instance.get_business_by_id(business_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling BusinessesAPIApi->get_business_by_id: #{e}"
end
```

#### Using the get_business_by_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Business>>, Integer, Hash)> get_business_by_id_with_http_info(business_id)

```ruby
begin
  # Get Business by ID
  data, status_code, headers = api_instance.get_business_by_id_with_http_info(business_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Business>>
rescue OpenBanking::ApiError => e
  puts "Error when calling BusinessesAPIApi->get_business_by_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_id** | **String** | Unique identifier of the business |  |

### Return type

[**Array&lt;Business&gt;**](Business.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_business

> <Business> update_business(business_id, new_business)

Update Business by ID

Update the details of a business based on its unique identifier. By providing the specific business ID and the updated information in the request, modifications can be made to the business's profile.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::BusinessesAPIApi.new
business_id = '192323' # String | Unique identifier of the business
new_business = OpenBanking::NewBusiness.new({name: 'ABC Tires Inc', personally_liable: true, address: OpenBanking::NewAddress.new, phone_number: OpenBanking::PhoneNumberFormat.new}) # NewBusiness | 

begin
  # Update Business by ID
  result = api_instance.update_business(business_id, new_business)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling BusinessesAPIApi->update_business: #{e}"
end
```

#### Using the update_business_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Business>, Integer, Hash)> update_business_with_http_info(business_id, new_business)

```ruby
begin
  # Update Business by ID
  data, status_code, headers = api_instance.update_business_with_http_info(business_id, new_business)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Business>
rescue OpenBanking::ApiError => e
  puts "Error when calling BusinessesAPIApi->update_business_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_id** | **String** | Unique identifier of the business |  |
| **new_business** | [**NewBusiness**](NewBusiness.md) |  |  |

### Return type

[**Business**](Business.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

