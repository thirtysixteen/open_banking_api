# OpenBanking::AccountValidationAssistanceApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_micro_deposits_details**](AccountValidationAssistanceApi.md#get_micro_deposits_details) | **GET** /microentry/v1/customers/{customerId}/accounts/{accountId} | Get Micro Entries Details |
| [**initiate_micro_amount_deposits**](AccountValidationAssistanceApi.md#initiate_micro_amount_deposits) | **POST** /microentry/v1/customers/{customerId} | Initiate Micro Entries |
| [**verify_micro_amount_deposits**](AccountValidationAssistanceApi.md#verify_micro_amount_deposits) | **POST** /microentry/v1/customers/{customerId}/accounts/{accountId}/amounts | Verify Micro Entries |


## get_micro_deposits_details

> <MicroDepositDetails> get_micro_deposits_details(customer_id, account_id)

Get Micro Entries Details

Fetch the micro entries details. `customerId` and `accountId` are the identifiers of the customer and account receiving the micro entries.    _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountValidationAssistanceApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID

begin
  # Get Micro Entries Details
  result = api_instance.get_micro_deposits_details(customer_id, account_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountValidationAssistanceApi->get_micro_deposits_details: #{e}"
end
```

#### Using the get_micro_deposits_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MicroDepositDetails>, Integer, Hash)> get_micro_deposits_details_with_http_info(customer_id, account_id)

```ruby
begin
  # Get Micro Entries Details
  data, status_code, headers = api_instance.get_micro_deposits_details_with_http_info(customer_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MicroDepositDetails>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountValidationAssistanceApi->get_micro_deposits_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |

### Return type

[**MicroDepositDetails**](MicroDepositDetails.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## initiate_micro_amount_deposits

> <InitiatedMicroDeposit> initiate_micro_amount_deposits(customer_id, micro_deposit_initiation)

Initiate Micro Entries

Initiate the micro entries to customer's account.  Two random micro amounts less than a dollar each will be deposited to provided customer's account.    _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountValidationAssistanceApi.new
customer_id = '1005061234' # String | A customer ID
micro_deposit_initiation = OpenBanking::MicroDepositInitiation.new({receiver: OpenBanking::Receiver.new({routing_number: '123456789', account_number: '123456', account_type: 'personalChecking', name: 'Bob Smith'})}) # MicroDepositInitiation | 

begin
  # Initiate Micro Entries
  result = api_instance.initiate_micro_amount_deposits(customer_id, micro_deposit_initiation)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountValidationAssistanceApi->initiate_micro_amount_deposits: #{e}"
end
```

#### Using the initiate_micro_amount_deposits_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InitiatedMicroDeposit>, Integer, Hash)> initiate_micro_amount_deposits_with_http_info(customer_id, micro_deposit_initiation)

```ruby
begin
  # Initiate Micro Entries
  data, status_code, headers = api_instance.initiate_micro_amount_deposits_with_http_info(customer_id, micro_deposit_initiation)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InitiatedMicroDeposit>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountValidationAssistanceApi->initiate_micro_amount_deposits_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **micro_deposit_initiation** | [**MicroDepositInitiation**](MicroDepositInitiation.md) |  |  |

### Return type

[**InitiatedMicroDeposit**](InitiatedMicroDeposit.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## verify_micro_amount_deposits

> <VerifiedMicroDeposit> verify_micro_amount_deposits(customer_id, account_id, micro_deposit_verification)

Verify Micro Entries

Verify the micro entries as received by customer in customer's account. Customer needs to verify the micro amounts received in customer's account. `customerId` and `accountId` are the identifiers of the customer and account  receiving the micro entries.    _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AccountValidationAssistanceApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID
micro_deposit_verification = OpenBanking::MicroDepositVerification.new({amounts: [0.12, 0.15]}) # MicroDepositVerification | 

begin
  # Verify Micro Entries
  result = api_instance.verify_micro_amount_deposits(customer_id, account_id, micro_deposit_verification)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountValidationAssistanceApi->verify_micro_amount_deposits: #{e}"
end
```

#### Using the verify_micro_amount_deposits_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<VerifiedMicroDeposit>, Integer, Hash)> verify_micro_amount_deposits_with_http_info(customer_id, account_id, micro_deposit_verification)

```ruby
begin
  # Verify Micro Entries
  data, status_code, headers = api_instance.verify_micro_amount_deposits_with_http_info(customer_id, account_id, micro_deposit_verification)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <VerifiedMicroDeposit>
rescue OpenBanking::ApiError => e
  puts "Error when calling AccountValidationAssistanceApi->verify_micro_amount_deposits_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |
| **micro_deposit_verification** | [**MicroDepositVerification**](MicroDepositVerification.md) |  |  |

### Return type

[**VerifiedMicroDeposit**](VerifiedMicroDeposit.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain

