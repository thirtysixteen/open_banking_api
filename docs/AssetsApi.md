# OpenBanking::AssetsApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_asset_by_customer_id**](AssetsApi.md#get_asset_by_customer_id) | **GET** /aggregation/v1/customers/{customerId}/assets/{assetId} | Get Asset by Customer and ID |


## get_asset_by_customer_id

> File get_asset_by_customer_id(customer_id, asset_id)

Get Asset by Customer and ID

Retrieve a binary file for the given asset ID.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AssetsApi.new
customer_id = '1005061234' # String | A customer ID
asset_id = '097545c5-1c2a-4f20-a5ef-77f0820344c9-2018601178' # String | The asset ID

begin
  # Get Asset by Customer and ID
  result = api_instance.get_asset_by_customer_id(customer_id, asset_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AssetsApi->get_asset_by_customer_id: #{e}"
end
```

#### Using the get_asset_by_customer_id_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(File, Integer, Hash)> get_asset_by_customer_id_with_http_info(customer_id, asset_id)

```ruby
begin
  # Get Asset by Customer and ID
  data, status_code, headers = api_instance.get_asset_by_customer_id_with_http_info(customer_id, asset_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => File
rescue OpenBanking::ApiError => e
  puts "Error when calling AssetsApi->get_asset_by_customer_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **asset_id** | **String** | The asset ID |  |

### Return type

**File**

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream, application/json, text/plain

