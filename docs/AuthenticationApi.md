# OpenBanking::AuthenticationApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_token**](AuthenticationApi.md#create_token) | **POST** /aggregation/v2/partners/authentication | Create Access Token |
| [**modify_partner_secret**](AuthenticationApi.md#modify_partner_secret) | **PUT** /aggregation/v2/partners/authentication | Modify Partner Secret |


## create_token

> <AccessToken> create_token(partner_credentials)

Create Access Token

Send Partner ID and Partner Secret to the Partner Authentication service to obtain a token for accessing Finicity APIs. * The token is valid for two hours and is required on all calls to the Finicity APIs * As a best practice, use a single token for all calls. Assign a timestamp for each token, and then check the current timestamp before making any calls. If the token is greater than 90 minutes, generate a new one. * ⚠️ After five failed attempts to authenticate, your account will be locked. To reset your account, you can report a support issue using the support.finicity.com portal. Alternatively, contact your Client Success Manager or your onboarding representative.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

### Examples

```ruby
require 'time'
require 'open_banking'
# setup authorization
OpenBanking.configure do |config|
  # Configure API key authorization: FinicityAppKey
  config.api_key['FinicityAppKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppKey'] = 'Bearer'
end

api_instance = OpenBanking::AuthenticationApi.new
partner_credentials = OpenBanking::PartnerCredentials.new({partner_id: '1234583871234', partner_secret: 'aqJ5Ic4SEVx2IgDQ6oR4'}) # PartnerCredentials | 

begin
  # Create Access Token
  result = api_instance.create_token(partner_credentials)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AuthenticationApi->create_token: #{e}"
end
```

#### Using the create_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AccessToken>, Integer, Hash)> create_token_with_http_info(partner_credentials)

```ruby
begin
  # Create Access Token
  data, status_code, headers = api_instance.create_token_with_http_info(partner_credentials)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AccessToken>
rescue OpenBanking::ApiError => e
  puts "Error when calling AuthenticationApi->create_token_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **partner_credentials** | [**PartnerCredentials**](PartnerCredentials.md) |  |  |

### Return type

[**AccessToken**](AccessToken.md)

### Authorization

[FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## modify_partner_secret

> modify_partner_secret(partner_credentials_with_new_secret)

Modify Partner Secret

Change the Partner Secret used to authenticate this partner.  The secret does not expire, but can be changed by calling this API. A valid Partner Secret may contain upper and lowercase characters, numbers, and the characters !, @, #, $, %, &, *, _, -, +. It must include at least one number and at least one letter, and its length should be between 12 and 255 characters.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

### Examples

```ruby
require 'time'
require 'open_banking'
# setup authorization
OpenBanking.configure do |config|
  # Configure API key authorization: FinicityAppKey
  config.api_key['FinicityAppKey'] = 'YOUR API KEY'
  # Uncomment the following line to set a prefix for the API key, e.g. 'Bearer' (defaults to nil)
  # config.api_key_prefix['FinicityAppKey'] = 'Bearer'
end

api_instance = OpenBanking::AuthenticationApi.new
partner_credentials_with_new_secret = OpenBanking::PartnerCredentialsWithNewSecret.new({partner_id: '1234583871234', partner_secret: 'aqJ5Ic4SEVx2IgDQ6oR4', new_partner_secret: 'OrU7tjiA3tIspCgb85xV'}) # PartnerCredentialsWithNewSecret | 

begin
  # Modify Partner Secret
  api_instance.modify_partner_secret(partner_credentials_with_new_secret)
rescue OpenBanking::ApiError => e
  puts "Error when calling AuthenticationApi->modify_partner_secret: #{e}"
end
```

#### Using the modify_partner_secret_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> modify_partner_secret_with_http_info(partner_credentials_with_new_secret)

```ruby
begin
  # Modify Partner Secret
  data, status_code, headers = api_instance.modify_partner_secret_with_http_info(partner_credentials_with_new_secret)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling AuthenticationApi->modify_partner_secret_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **partner_credentials_with_new_secret** | [**PartnerCredentialsWithNewSecret**](PartnerCredentialsWithNewSecret.md) |  |  |

### Return type

nil (empty response body)

### Authorization

[FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

