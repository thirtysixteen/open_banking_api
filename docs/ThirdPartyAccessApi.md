# OpenBanking::ThirdPartyAccessApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**generate_third_party_access_key**](ThirdPartyAccessApi.md#generate_third_party_access_key) | **POST** /aggregation/v1/partners/accessKey | Generate Third Party Access Key |
| [**revoke_third_party_access_key**](ThirdPartyAccessApi.md#revoke_third_party_access_key) | **DELETE** /aggregation/v1/partners/accessKey/{consentReceiptId} | Revoke Third Party Access |
| [**update_third_party_access_key**](ThirdPartyAccessApi.md#update_third_party_access_key) | **PUT** /aggregation/v1/partners/accessKey/{consentReceiptId} | Update Third Party Access |


## generate_third_party_access_key

> <ThirdPartyAccessKeyReceiptData> generate_third_party_access_key(third_party_access_key_data)

Generate Third Party Access Key

Generate access key for third party partners. A partner can provide access to third party partners with this access key.

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

api_instance = OpenBanking::ThirdPartyAccessApi.new
third_party_access_key_data = OpenBanking::ThirdPartyAccessKeyData.new({customer_id: '1005061234', partner_id: '1234583871234', third_party_partner_id: '1234583871234', products: [OpenBanking::ThirdPartyAccessProduct.new({product: 'moneyTransferDetails', account_id: '5011648377', access_period: OpenBanking::ThirdPartyAccessPeriod.new({type: 'timeframe', start_time: Time.parse('2022-03-10T06:06:20.042584549Z'), end_time: Time.parse('2022-03-10T06:06:20.042584549Z')})})]}) # ThirdPartyAccessKeyData | 

begin
  # Generate Third Party Access Key
  result = api_instance.generate_third_party_access_key(third_party_access_key_data)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ThirdPartyAccessApi->generate_third_party_access_key: #{e}"
end
```

#### Using the generate_third_party_access_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ThirdPartyAccessKeyReceiptData>, Integer, Hash)> generate_third_party_access_key_with_http_info(third_party_access_key_data)

```ruby
begin
  # Generate Third Party Access Key
  data, status_code, headers = api_instance.generate_third_party_access_key_with_http_info(third_party_access_key_data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ThirdPartyAccessKeyReceiptData>
rescue OpenBanking::ApiError => e
  puts "Error when calling ThirdPartyAccessApi->generate_third_party_access_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **third_party_access_key_data** | [**ThirdPartyAccessKeyData**](ThirdPartyAccessKeyData.md) |  |  |

### Return type

[**ThirdPartyAccessKeyReceiptData**](ThirdPartyAccessKeyReceiptData.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## revoke_third_party_access_key

> revoke_third_party_access_key(consent_receipt_id)

Revoke Third Party Access

Revoke access of third party partners

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

api_instance = OpenBanking::ThirdPartyAccessApi.new
consent_receipt_id = 'cr_4pfI3r1X8aOHrDDwrwC01NHFxOXlT1' # String | Third party access key receipt ID

begin
  # Revoke Third Party Access
  api_instance.revoke_third_party_access_key(consent_receipt_id)
rescue OpenBanking::ApiError => e
  puts "Error when calling ThirdPartyAccessApi->revoke_third_party_access_key: #{e}"
end
```

#### Using the revoke_third_party_access_key_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> revoke_third_party_access_key_with_http_info(consent_receipt_id)

```ruby
begin
  # Revoke Third Party Access
  data, status_code, headers = api_instance.revoke_third_party_access_key_with_http_info(consent_receipt_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling ThirdPartyAccessApi->revoke_third_party_access_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **consent_receipt_id** | **String** | Third party access key receipt ID |  |

### Return type

nil (empty response body)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## update_third_party_access_key

> <ThirdPartyAccessKeyReceiptData> update_third_party_access_key(consent_receipt_id, third_party_access_key_data)

Update Third Party Access

Update access for third party partners

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

api_instance = OpenBanking::ThirdPartyAccessApi.new
consent_receipt_id = 'cr_4pfI3r1X8aOHrDDwrwC01NHFxOXlT1' # String | Third party access key receipt ID
third_party_access_key_data = OpenBanking::ThirdPartyAccessKeyData.new({customer_id: '1005061234', partner_id: '1234583871234', third_party_partner_id: '1234583871234', products: [OpenBanking::ThirdPartyAccessProduct.new({product: 'moneyTransferDetails', account_id: '5011648377', access_period: OpenBanking::ThirdPartyAccessPeriod.new({type: 'timeframe', start_time: Time.parse('2022-03-10T06:06:20.042584549Z'), end_time: Time.parse('2022-03-10T06:06:20.042584549Z')})})]}) # ThirdPartyAccessKeyData | 

begin
  # Update Third Party Access
  result = api_instance.update_third_party_access_key(consent_receipt_id, third_party_access_key_data)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ThirdPartyAccessApi->update_third_party_access_key: #{e}"
end
```

#### Using the update_third_party_access_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ThirdPartyAccessKeyReceiptData>, Integer, Hash)> update_third_party_access_key_with_http_info(consent_receipt_id, third_party_access_key_data)

```ruby
begin
  # Update Third Party Access
  data, status_code, headers = api_instance.update_third_party_access_key_with_http_info(consent_receipt_id, third_party_access_key_data)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ThirdPartyAccessKeyReceiptData>
rescue OpenBanking::ApiError => e
  puts "Error when calling ThirdPartyAccessApi->update_third_party_access_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **consent_receipt_id** | **String** | Third party access key receipt ID |  |
| **third_party_access_key_data** | [**ThirdPartyAccessKeyData**](ThirdPartyAccessKeyData.md) |  |  |

### Return type

[**ThirdPartyAccessKeyReceiptData**](ThirdPartyAccessKeyReceiptData.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain

