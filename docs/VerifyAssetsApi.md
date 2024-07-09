# OpenBanking::VerifyAssetsApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**generate_prequalification_cra_report**](VerifyAssetsApi.md#generate_prequalification_cra_report) | **POST** /decisioning/v2/customers/{customerId}/preQualVoa | Generate Prequalification (CRA) Report |
| [**generate_prequalification_non_cra_report**](VerifyAssetsApi.md#generate_prequalification_non_cra_report) | **POST** /decisioning/v2/customers/{customerId}/assetSummary | Generate Prequalification (Non-CRA) Report |
| [**generate_voa_report**](VerifyAssetsApi.md#generate_voa_report) | **POST** /decisioning/v2/customers/{customerId}/voa | Generate VOA Report |
| [**generate_voa_with_income_report**](VerifyAssetsApi.md#generate_voa_with_income_report) | **POST** /decisioning/v2/customers/{customerId}/voaHistory | Generate VOA With Income Report |


## generate_prequalification_cra_report

> <PrequalificationReportAck> generate_prequalification_cra_report(customer_id, prequalification_report_constraints, opts)

Generate Prequalification (CRA) Report

Retrieve all checking, savings, money market, and investment accounts for a consumer. The account, owner information, and the number of insufficient funds (NSFs) for checking accounts are also provided.  If no account of type checking, savings, money market, or investment is found, the service will return HTTP 400 Bad Request.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::VerifyAssetsApi.new
customer_id = '1005061234' # String | A customer ID
prequalification_report_constraints = OpenBanking::PrequalificationReportConstraints.new # PrequalificationReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate Prequalification (CRA) Report
  result = api_instance.generate_prequalification_cra_report(customer_id, prequalification_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyAssetsApi->generate_prequalification_cra_report: #{e}"
end
```

#### Using the generate_prequalification_cra_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PrequalificationReportAck>, Integer, Hash)> generate_prequalification_cra_report_with_http_info(customer_id, prequalification_report_constraints, opts)

```ruby
begin
  # Generate Prequalification (CRA) Report
  data, status_code, headers = api_instance.generate_prequalification_cra_report_with_http_info(customer_id, prequalification_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PrequalificationReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyAssetsApi->generate_prequalification_cra_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **prequalification_report_constraints** | [**PrequalificationReportConstraints**](PrequalificationReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**PrequalificationReportAck**](PrequalificationReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_prequalification_non_cra_report

> <PrequalificationReportAck> generate_prequalification_non_cra_report(customer_id, prequalification_report_constraints, opts)

Generate Prequalification (Non-CRA) Report

Retrieve all checking, savings, money market, and investment accounts for a customer. The account, owner information, and the number of insufficient funds (NSFs) for checking accounts are also provided.  If no account type of checking, savings, money market, or investment is found, the service will return HTTP 400 Bad Request.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::VerifyAssetsApi.new
customer_id = '1005061234' # String | A customer ID
prequalification_report_constraints = OpenBanking::PrequalificationReportConstraints.new # PrequalificationReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate Prequalification (Non-CRA) Report
  result = api_instance.generate_prequalification_non_cra_report(customer_id, prequalification_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyAssetsApi->generate_prequalification_non_cra_report: #{e}"
end
```

#### Using the generate_prequalification_non_cra_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PrequalificationReportAck>, Integer, Hash)> generate_prequalification_non_cra_report_with_http_info(customer_id, prequalification_report_constraints, opts)

```ruby
begin
  # Generate Prequalification (Non-CRA) Report
  data, status_code, headers = api_instance.generate_prequalification_non_cra_report_with_http_info(customer_id, prequalification_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PrequalificationReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyAssetsApi->generate_prequalification_non_cra_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **prequalification_report_constraints** | [**PrequalificationReportConstraints**](PrequalificationReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**PrequalificationReportAck**](PrequalificationReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_voa_report

> <VOAReportAck> generate_voa_report(customer_id, voa_report_constraints, opts)

Generate VOA Report

Generate a Verification of Assets (VOA) report for all checking, savings, money market, and investment accounts for the given customer. This service retrieves up to twelve months of transaction history for each account and uses this information to generate the VOA report.  This is a premium service. The billing rate is the variable rate for Verification of Assets under the current subscription plan. The billable event is the successful generation of a VOA report.  Before calling this API, a consumer must be created for the given customer ID (see Consumers APIs).  If no account of type checking, savings, money market, or investment is found, the service will return HTTP 400 Bad Request.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::VerifyAssetsApi.new
customer_id = '1005061234' # String | A customer ID
voa_report_constraints = OpenBanking::VOAReportConstraints.new # VOAReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate VOA Report
  result = api_instance.generate_voa_report(customer_id, voa_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyAssetsApi->generate_voa_report: #{e}"
end
```

#### Using the generate_voa_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<VOAReportAck>, Integer, Hash)> generate_voa_report_with_http_info(customer_id, voa_report_constraints, opts)

```ruby
begin
  # Generate VOA Report
  data, status_code, headers = api_instance.generate_voa_report_with_http_info(customer_id, voa_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <VOAReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyAssetsApi->generate_voa_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **voa_report_constraints** | [**VOAReportConstraints**](VOAReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**VOAReportAck**](VOAReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_voa_with_income_report

> <VOAWithIncomeReportAck> generate_voa_with_income_report(customer_id, voa_with_income_report_constraints, opts)

Generate VOA With Income Report

Generate a Verification of Assets with Income (VOAI) report for all checking, savings, money market, and investment accounts for the given customer. This service retrieves up to 24 months of transaction history for each account and uses this information to generate the VOAI report. The report includes 1 - 6 months of all debit and credit transactions for asset verification. By default, the history is set to 61 days, however, you can change the transaction history in this section by setting the `fromDate` parameter. The report also includes up to 24 months of income credit transactions (ordered by account and confidence level) regardless of `fromDate` for income verification.  This is a premium service. The billable event is the successful generation of a VOAI report.  Before calling this API, a consumer must be created for the given customer ID (see Consumers APIs).  If no account of type checking, savings, money market, or investment is found, the service will return HTTP 400 Bad Request.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::VerifyAssetsApi.new
customer_id = '1005061234' # String | A customer ID
voa_with_income_report_constraints = OpenBanking::VOAWithIncomeReportConstraints.new # VOAWithIncomeReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate VOA With Income Report
  result = api_instance.generate_voa_with_income_report(customer_id, voa_with_income_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyAssetsApi->generate_voa_with_income_report: #{e}"
end
```

#### Using the generate_voa_with_income_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<VOAWithIncomeReportAck>, Integer, Hash)> generate_voa_with_income_report_with_http_info(customer_id, voa_with_income_report_constraints, opts)

```ruby
begin
  # Generate VOA With Income Report
  data, status_code, headers = api_instance.generate_voa_with_income_report_with_http_info(customer_id, voa_with_income_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <VOAWithIncomeReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyAssetsApi->generate_voa_with_income_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **voa_with_income_report_constraints** | [**VOAWithIncomeReportConstraints**](VOAWithIncomeReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**VOAWithIncomeReportAck**](VOAWithIncomeReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain

