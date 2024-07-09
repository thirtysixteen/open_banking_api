# OpenBanking::PaymentsApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_account_ach_details**](PaymentsApi.md#get_account_ach_details) | **GET** /aggregation/v1/customers/{customerId}/accounts/{accountId}/details | Get Account ACH Details |
| [**get_account_owner**](PaymentsApi.md#get_account_owner) | **GET** /aggregation/v1/customers/{customerId}/accounts/{accountId}/owner | Get Account Owner |
| [**get_account_owner_details**](PaymentsApi.md#get_account_owner_details) | **GET** /aggregation/v3/customers/{customerId}/accounts/{accountId}/owner | Get Account Owner Details |
| [**get_account_payment_instruction_details**](PaymentsApi.md#get_account_payment_instruction_details) | **GET** /aggregation/v3/customers/{customerId}/accounts/{accountId}/details | Get Account ACH Details with RTP |
| [**get_available_balance**](PaymentsApi.md#get_available_balance) | **GET** /aggregation/v1/customers/{customerId}/accounts/{accountId}/availableBalance | Get Available Balance - Cached |
| [**get_available_balance_live**](PaymentsApi.md#get_available_balance_live) | **GET** /aggregation/v1/customers/{customerId}/accounts/{accountId}/availableBalance/live | Get Available Balance |
| [**get_loan_payment_details**](PaymentsApi.md#get_loan_payment_details) | **GET** /aggregation/v2/customers/{customerId}/accounts/{accountId}/loanDetails | Get Loan Payment Details |


## get_account_ach_details

> <ACHDetails> get_account_ach_details(customer_id, account_id)

Get Account ACH Details

Return the real account number and routing number details for an ACH payment.  Note: this is a premium service, billable per every successful API call.  _Supported account types_: \"checking\", \"savings\", \"moneyMarket\"  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::PaymentsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID

begin
  # Get Account ACH Details
  result = api_instance.get_account_ach_details(customer_id, account_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_account_ach_details: #{e}"
end
```

#### Using the get_account_ach_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ACHDetails>, Integer, Hash)> get_account_ach_details_with_http_info(customer_id, account_id)

```ruby
begin
  # Get Account ACH Details
  data, status_code, headers = api_instance.get_account_ach_details_with_http_info(customer_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ACHDetails>
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_account_ach_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |

### Return type

[**ACHDetails**](ACHDetails.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_account_owner

> <AccountOwner> get_account_owner(customer_id, account_id)

Get Account Owner

Retrieve the names and addresses of the account owner from a financial institution.  Note: this is a premium service, billable per every successful API call.  This service retrieves account data from the institution. This usually returns quickly, but in some scenarios may take a few minutes to complete. In the event of a timeout condition, retry the call.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::PaymentsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID

begin
  # Get Account Owner
  result = api_instance.get_account_owner(customer_id, account_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_account_owner: #{e}"
end
```

#### Using the get_account_owner_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AccountOwner>, Integer, Hash)> get_account_owner_with_http_info(customer_id, account_id)

```ruby
begin
  # Get Account Owner
  data, status_code, headers = api_instance.get_account_owner_with_http_info(customer_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AccountOwner>
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_account_owner_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |

### Return type

[**AccountOwner**](AccountOwner.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_account_owner_details

> <AccountOwnerHolders> get_account_owner_details(customer_id, account_id, opts)

Get Account Owner Details

This service retrieves the account details for an account holder from an institution. The following data objects are available.  * Account holders  * Addresses  * Emails  * Phones  * Documentations  * Identity Insights   Note: The data returned varies from institution to institution as not all of them make the same data available. This is a premium service, billable per each successful API call.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::PaymentsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID
opts = {
  with_insights: false # Boolean | If this parameter is true, Identity Insights data will be returned along with the account owner information
}

begin
  # Get Account Owner Details
  result = api_instance.get_account_owner_details(customer_id, account_id, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_account_owner_details: #{e}"
end
```

#### Using the get_account_owner_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AccountOwnerHolders>, Integer, Hash)> get_account_owner_details_with_http_info(customer_id, account_id, opts)

```ruby
begin
  # Get Account Owner Details
  data, status_code, headers = api_instance.get_account_owner_details_with_http_info(customer_id, account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AccountOwnerHolders>
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_account_owner_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |
| **with_insights** | **Boolean** | If this parameter is true, Identity Insights data will be returned along with the account owner information | [optional] |

### Return type

[**AccountOwnerHolders**](AccountOwnerHolders.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_account_payment_instruction_details

> <PaymentInstructions> get_account_payment_instruction_details(customer_id, account_id)

Get Account ACH Details with RTP

Return the real account number and routing number details for an ACH payment along with the supported payment instruction details. If the RTP (Real Time Payment) value for “transferInEnabled” is true, then the account can receive RTPs. If the value for “transferOutEnabled” is true, then the account can send RTPs    Note: this is a premium service, billable per every successful API call.  _Supported account types_: \"checking\", \"savings\", \"moneyMarket\"  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::PaymentsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID

begin
  # Get Account ACH Details with RTP
  result = api_instance.get_account_payment_instruction_details(customer_id, account_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_account_payment_instruction_details: #{e}"
end
```

#### Using the get_account_payment_instruction_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentInstructions>, Integer, Hash)> get_account_payment_instruction_details_with_http_info(customer_id, account_id)

```ruby
begin
  # Get Account ACH Details with RTP
  data, status_code, headers = api_instance.get_account_payment_instruction_details_with_http_info(customer_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentInstructions>
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_account_payment_instruction_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |

### Return type

[**PaymentInstructions**](PaymentInstructions.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_available_balance

> <AvailableBalance> get_available_balance(customer_id, account_id)

Get Available Balance - Cached

Retrieve the latest cached available and cleared account balances for a customer. Since we update and store balances throughout the day, this is the most accurate balance information available when a connection to a financial institution is unavailable or when a faster response is needed. Only deposit account types are supported: Checking, Savings, Money Market, and CD.  Note: this is a premium service, billable per every successful API call. Enrollment is required.  _Supported account types_: \"checking\", \"savings\", \"moneyMarket\", \"cd\"  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::PaymentsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID

begin
  # Get Available Balance - Cached
  result = api_instance.get_available_balance(customer_id, account_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_available_balance: #{e}"
end
```

#### Using the get_available_balance_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AvailableBalance>, Integer, Hash)> get_available_balance_with_http_info(customer_id, account_id)

```ruby
begin
  # Get Available Balance - Cached
  data, status_code, headers = api_instance.get_available_balance_with_http_info(customer_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AvailableBalance>
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_available_balance_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |

### Return type

[**AvailableBalance**](AvailableBalance.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_available_balance_live

> <AvailableBalance> get_available_balance_live(customer_id, account_id, opts)

Get Available Balance

Retrieve the available and cleared account balances for a single account in real-time directly from a financial institution.   You can define an additional query parameter `balance_cache_interval` to specify the time interval of the last cached balance. This parameter is used by the server to determine whether the cached balance is still valid or if it needs to be refreshed.     Note: this is a premium service, billable per every successful API call.  _Supported account types_: \"checking\", \"savings\", \"moneyMarket\", \"cd\"  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::PaymentsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID
opts = {
  balance_cache_interval: 1 # Integer | `balance_cache_interval` (in minutes) is used to decide whether to return existing cached balance or retrieve from financial institution in real-time. Details explained below: 1. If the cached balance data at server is older than provided `balance_cache_interval` then live balance from financial institution will be retrieved. 2. If the cached balance data is within provided `balance_cache_interval` allowed interval then balance from cache will be returned. 3. If `balance_cache_interval` is 0 or not provided, then live balance from financial institution will be retrieved.
}

begin
  # Get Available Balance
  result = api_instance.get_available_balance_live(customer_id, account_id, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_available_balance_live: #{e}"
end
```

#### Using the get_available_balance_live_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AvailableBalance>, Integer, Hash)> get_available_balance_live_with_http_info(customer_id, account_id, opts)

```ruby
begin
  # Get Available Balance
  data, status_code, headers = api_instance.get_available_balance_live_with_http_info(customer_id, account_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AvailableBalance>
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_available_balance_live_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |
| **balance_cache_interval** | **Integer** | &#x60;balance_cache_interval&#x60; (in minutes) is used to decide whether to return existing cached balance or retrieve from financial institution in real-time. Details explained below: 1. If the cached balance data at server is older than provided &#x60;balance_cache_interval&#x60; then live balance from financial institution will be retrieved. 2. If the cached balance data is within provided &#x60;balance_cache_interval&#x60; allowed interval then balance from cache will be returned. 3. If &#x60;balance_cache_interval&#x60; is 0 or not provided, then live balance from financial institution will be retrieved. | [optional][default to 0] |

### Return type

[**AvailableBalance**](AvailableBalance.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_loan_payment_details

> <LoanPaymentDetails> get_loan_payment_details(customer_id, account_id)

Get Loan Payment Details

Return the loan payment details of the customer for a loan-type account.  Note: this is a premium service, billable per every successful API call.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::PaymentsApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID

begin
  # Get Loan Payment Details
  result = api_instance.get_loan_payment_details(customer_id, account_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_loan_payment_details: #{e}"
end
```

#### Using the get_loan_payment_details_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<LoanPaymentDetails>, Integer, Hash)> get_loan_payment_details_with_http_info(customer_id, account_id)

```ruby
begin
  # Get Loan Payment Details
  data, status_code, headers = api_instance.get_loan_payment_details_with_http_info(customer_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LoanPaymentDetails>
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentsApi->get_loan_payment_details_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |

### Return type

[**LoanPaymentDetails**](LoanPaymentDetails.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain

