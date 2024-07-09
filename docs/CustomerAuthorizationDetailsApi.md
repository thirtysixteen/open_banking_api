# OpenBanking::CustomerAuthorizationDetailsApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_customer_authorization_details**](CustomerAuthorizationDetailsApi.md#get_customer_authorization_details) | **GET** /customers/institution-logins/{institution_login_id}/authorization-details | Returns customer authorization details for the institution login identification. |


## get_customer_authorization_details

> <CustomerAuthorizationDetails> get_customer_authorization_details(institution_login_id)

Returns customer authorization details for the institution login identification.

The endpoint provides customer authorization details like authorization start date, authorization end date against the requested institution login id  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CustomerAuthorizationDetailsApi.new
institution_login_id = 7008461438 # Integer | Institution login id of the customer.

begin
  # Returns customer authorization details for the institution login identification.
  result = api_instance.get_customer_authorization_details(institution_login_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomerAuthorizationDetailsApi->get_customer_authorization_details: #{e}"
end
```

#### Using the get_customer_authorization_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAuthorizationDetails>, Integer, Hash)> get_customer_authorization_details_with_http_info(institution_login_id)

```ruby
begin
  # Returns customer authorization details for the institution login identification.
  data, status_code, headers = api_instance.get_customer_authorization_details_with_http_info(institution_login_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAuthorizationDetails>
rescue OpenBanking::ApiError => e
  puts "Error when calling CustomerAuthorizationDetailsApi->get_customer_authorization_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **institution_login_id** | **Integer** | Institution login id of the customer. |  |

### Return type

[**CustomerAuthorizationDetails**](CustomerAuthorizationDetails.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain

