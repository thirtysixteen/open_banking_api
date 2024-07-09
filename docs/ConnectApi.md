# OpenBanking::ConnectApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**generate_connect_url**](ConnectApi.md#generate_connect_url) | **POST** /connect/v2/generate | Generate Connect URL |
| [**generate_fix_connect_url**](ConnectApi.md#generate_fix_connect_url) | **POST** /connect/v2/generate/fix | Generate Fix Connect URL |
| [**generate_joint_borrower_connect_url**](ConnectApi.md#generate_joint_borrower_connect_url) | **POST** /connect/v2/generate/jointBorrower | Generate Connect URL - Joint Borrower |
| [**generate_lite_connect_url**](ConnectApi.md#generate_lite_connect_url) | **POST** /connect/v2/generate/lite | Generate Lite Connect URL |
| [**get_all_experience**](ConnectApi.md#get_all_experience) | **GET** /connect/experiences | Get Experience IDs |
| [**send_connect_email**](ConnectApi.md#send_connect_email) | **POST** /connect/v2/send/email | Send Connect Email |
| [**send_joint_borrower_connect_email**](ConnectApi.md#send_joint_borrower_connect_email) | **POST** /connect/v2/send/email/jointBorrower | Send Connect Email - Joint Borrower |
| [**verify_micro_entry_microdeposit**](ConnectApi.md#verify_micro_entry_microdeposit) | **POST** /connect/v2/generate/microentry/verify | Account Validation Assistant User verification of microdeposits |


## generate_connect_url

> <ConnectUrl> generate_connect_url(connect_parameters)

Generate Connect URL

Generate a Connect URL link to add within your own applications.  Optional Parameters: * `experience`: Configure different customer experiences per Connect session by changing the brand, color, logo, icon, the type of credit decisioning report to generate after the session ends, and more. * `language`: By default, the Connect application is in English. You don't need to pass  this parameter unless you want to translate Connect into one of our supported languages.    * Spanish (United States)   * French (Canada)   MVS Developers: You can pre-populate the consumer's SSN on the Find employment records page at the beginning of the MVS payroll app. Pass the SSN value for the consumer in the body of the request call.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::ConnectApi.new
connect_parameters = OpenBanking::ConnectParameters.new({partner_id: '1234583871234', customer_id: '1005061234'}) # ConnectParameters | 

begin
  # Generate Connect URL
  result = api_instance.generate_connect_url(connect_parameters)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->generate_connect_url: #{e}"
end
```

#### Using the generate_connect_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectUrl>, Integer, Hash)> generate_connect_url_with_http_info(connect_parameters)

```ruby
begin
  # Generate Connect URL
  data, status_code, headers = api_instance.generate_connect_url_with_http_info(connect_parameters)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectUrl>
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->generate_connect_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connect_parameters** | [**ConnectParameters**](ConnectParameters.md) |  |  |

### Return type

[**ConnectUrl**](ConnectUrl.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_fix_connect_url

> <ConnectUrl> generate_fix_connect_url(fix_connect_parameters)

Generate Fix Connect URL

Use the Connect Fix API when the following conditions occur: * The connection to the user's financial institution is lost * The user's credentials were updated (for any number of reasons) * The user's MFA challenge has expired  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::ConnectApi.new
fix_connect_parameters = OpenBanking::FixConnectParameters.new({partner_id: '1234583871234', customer_id: '1005061234', institution_login_id: '1007302745'}) # FixConnectParameters | 

begin
  # Generate Fix Connect URL
  result = api_instance.generate_fix_connect_url(fix_connect_parameters)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->generate_fix_connect_url: #{e}"
end
```

#### Using the generate_fix_connect_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectUrl>, Integer, Hash)> generate_fix_connect_url_with_http_info(fix_connect_parameters)

```ruby
begin
  # Generate Fix Connect URL
  data, status_code, headers = api_instance.generate_fix_connect_url_with_http_info(fix_connect_parameters)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectUrl>
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->generate_fix_connect_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **fix_connect_parameters** | [**FixConnectParameters**](FixConnectParameters.md) |  |  |

### Return type

[**ConnectUrl**](ConnectUrl.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_joint_borrower_connect_url

> <ConnectUrl> generate_joint_borrower_connect_url(connect_joint_borrower_parameters)

Generate Connect URL - Joint Borrower

Same as Connect Full (`POST /connect/v2/generate`) but for joint borrowers.  MVS prompts both the primary and joint borrower to enter each of their financial, payroll, and paystub information in the same Connect session.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::ConnectApi.new
connect_joint_borrower_parameters = OpenBanking::ConnectJointBorrowerParameters.new({partner_id: '1234583871234', borrowers: [OpenBanking::Borrower.new({customer_id: '1005061234', consumer_id: '0bf46322c167b562e6cbed9d40e19a4c', type: 'primary'})]}) # ConnectJointBorrowerParameters | 

begin
  # Generate Connect URL - Joint Borrower
  result = api_instance.generate_joint_borrower_connect_url(connect_joint_borrower_parameters)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->generate_joint_borrower_connect_url: #{e}"
end
```

#### Using the generate_joint_borrower_connect_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectUrl>, Integer, Hash)> generate_joint_borrower_connect_url_with_http_info(connect_joint_borrower_parameters)

```ruby
begin
  # Generate Connect URL - Joint Borrower
  data, status_code, headers = api_instance.generate_joint_borrower_connect_url_with_http_info(connect_joint_borrower_parameters)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectUrl>
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->generate_joint_borrower_connect_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connect_joint_borrower_parameters** | [**ConnectJointBorrowerParameters**](ConnectJointBorrowerParameters.md) |  |  |

### Return type

[**ConnectUrl**](ConnectUrl.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_lite_connect_url

> <ConnectUrl> generate_lite_connect_url(lite_connect_parameters)

Generate Lite Connect URL

Connect Lite is a variation of Connect Full (`POST /connect/v2/generate`), which has a limited set of features. * Sign in, user's credentials, and Multi-Factor Authentication (MFA) * No user account management  The Connect Web SDK isn't a requirement when using Connect lite. However, if you want to use the SDK events, routes, and user events, then you must integrate with the Connect Web SDK.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::ConnectApi.new
lite_connect_parameters = OpenBanking::LiteConnectParameters.new({partner_id: '1234583871234', customer_id: '1005061234', institution_id: 4222}) # LiteConnectParameters | 

begin
  # Generate Lite Connect URL
  result = api_instance.generate_lite_connect_url(lite_connect_parameters)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->generate_lite_connect_url: #{e}"
end
```

#### Using the generate_lite_connect_url_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectUrl>, Integer, Hash)> generate_lite_connect_url_with_http_info(lite_connect_parameters)

```ruby
begin
  # Generate Lite Connect URL
  data, status_code, headers = api_instance.generate_lite_connect_url_with_http_info(lite_connect_parameters)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectUrl>
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->generate_lite_connect_url_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **lite_connect_parameters** | [**LiteConnectParameters**](LiteConnectParameters.md) |  |  |

### Return type

[**ConnectUrl**](ConnectUrl.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## get_all_experience

> <Array<Experiences>> get_all_experience(app_name, opts)

Get Experience IDs

Retrieve Connect experiences by application name. Optionally, filter the experiences by product codes.

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

api_instance = OpenBanking::ConnectApi.new
app_name = 'test app' # String | Unique name of the application provided to Mastercard during app registration.
opts = {
  product_code: ['inner_example'] # Array<String> | A unique billing code assigned to each open banking product used by the customer, as detailed in their contract.
}

begin
  # Get Experience IDs
  result = api_instance.get_all_experience(app_name, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->get_all_experience: #{e}"
end
```

#### Using the get_all_experience_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<Experiences>>, Integer, Hash)> get_all_experience_with_http_info(app_name, opts)

```ruby
begin
  # Get Experience IDs
  data, status_code, headers = api_instance.get_all_experience_with_http_info(app_name, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<Experiences>>
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->get_all_experience_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **app_name** | **String** | Unique name of the application provided to Mastercard during app registration. |  |
| **product_code** | [**Array&lt;String&gt;**](String.md) | A unique billing code assigned to each open banking product used by the customer, as detailed in their contract. | [optional] |

### Return type

[**Array&lt;Experiences&gt;**](Experiences.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## send_connect_email

> <ConnectEmailUrl> send_connect_email(connect_email_parameters)

Send Connect Email

Same as Connect Full (`POST /connect/v2/generate`) but send a Connect email to a consumer.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::ConnectApi.new
connect_email_parameters = OpenBanking::ConnectEmailParameters.new({partner_id: '1234583871234', customer_id: '1005061234', consumer_id: '0bf46322c167b562e6cbed9d40e19a4c', email: OpenBanking::EmailOptions.new({to: 'bob@example.com'})}) # ConnectEmailParameters | 

begin
  # Send Connect Email
  result = api_instance.send_connect_email(connect_email_parameters)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->send_connect_email: #{e}"
end
```

#### Using the send_connect_email_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectEmailUrl>, Integer, Hash)> send_connect_email_with_http_info(connect_email_parameters)

```ruby
begin
  # Send Connect Email
  data, status_code, headers = api_instance.send_connect_email_with_http_info(connect_email_parameters)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectEmailUrl>
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->send_connect_email_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connect_email_parameters** | [**ConnectEmailParameters**](ConnectEmailParameters.md) |  |  |

### Return type

[**ConnectEmailUrl**](ConnectEmailUrl.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## send_joint_borrower_connect_email

> <ConnectEmailUrl> send_joint_borrower_connect_email(connect_joint_borrower_email_parameters)

Send Connect Email - Joint Borrower

Same as Connect Joint Borrower (`POST /connect/v2/generate/jointBorrower`) but send a Connect email  to at least one of the joint borrower's email addresses.  When the consumer opens the email, MVS prompts both the primary and joint borrower to enter each of their financial, payroll, and paystub information in the same Connect session.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::ConnectApi.new
connect_joint_borrower_email_parameters = OpenBanking::ConnectJointBorrowerEmailParameters.new({partner_id: '1234583871234', borrowers: [OpenBanking::Borrower.new({customer_id: '1005061234', consumer_id: '0bf46322c167b562e6cbed9d40e19a4c', type: 'primary'})], email: OpenBanking::EmailOptions.new({to: 'bob@example.com'}), experience: 'default'}) # ConnectJointBorrowerEmailParameters | 

begin
  # Send Connect Email - Joint Borrower
  result = api_instance.send_joint_borrower_connect_email(connect_joint_borrower_email_parameters)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->send_joint_borrower_connect_email: #{e}"
end
```

#### Using the send_joint_borrower_connect_email_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectEmailUrl>, Integer, Hash)> send_joint_borrower_connect_email_with_http_info(connect_joint_borrower_email_parameters)

```ruby
begin
  # Send Connect Email - Joint Borrower
  data, status_code, headers = api_instance.send_joint_borrower_connect_email_with_http_info(connect_joint_borrower_email_parameters)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectEmailUrl>
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->send_joint_borrower_connect_email_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **connect_joint_borrower_email_parameters** | [**ConnectJointBorrowerEmailParameters**](ConnectJointBorrowerEmailParameters.md) |  |  |

### Return type

[**ConnectEmailUrl**](ConnectEmailUrl.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## verify_micro_entry_microdeposit

> <ConnectUrl> verify_micro_entry_microdeposit(micro_entry_verify_request_parameter)

Account Validation Assistant User verification of microdeposits

The UI re-engages the consumer to enter two microdeposit amounts found in their account and validates them.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::ConnectApi.new
micro_entry_verify_request_parameter = OpenBanking::MicroEntryVerifyRequestParameter.new # MicroEntryVerifyRequestParameter | 

begin
  # Account Validation Assistant User verification of microdeposits
  result = api_instance.verify_micro_entry_microdeposit(micro_entry_verify_request_parameter)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->verify_micro_entry_microdeposit: #{e}"
end
```

#### Using the verify_micro_entry_microdeposit_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConnectUrl>, Integer, Hash)> verify_micro_entry_microdeposit_with_http_info(micro_entry_verify_request_parameter)

```ruby
begin
  # Account Validation Assistant User verification of microdeposits
  data, status_code, headers = api_instance.verify_micro_entry_microdeposit_with_http_info(micro_entry_verify_request_parameter)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConnectUrl>
rescue OpenBanking::ApiError => e
  puts "Error when calling ConnectApi->verify_micro_entry_microdeposit_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **micro_entry_verify_request_parameter** | [**MicroEntryVerifyRequestParameter**](MicroEntryVerifyRequestParameter.md) |  |  |

### Return type

[**ConnectUrl**](ConnectUrl.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain

