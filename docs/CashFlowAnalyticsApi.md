# OpenBanking::CashFlowAnalyticsApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**generate_cash_flow_analytics**](CashFlowAnalyticsApi.md#generate_cash_flow_analytics) | **POST** /analytics/cashflow/v1/customer/{customerId} | Generate Cash Flow Analytics |
| [**generate_cash_flow_analytics_fcra**](CashFlowAnalyticsApi.md#generate_cash_flow_analytics_fcra) | **POST** /analytics/cashflow/v1/customer/{customerId}/fcra | Generate Cash Flow Analytics - FCRA |
| [**generate_cashflow_analytics_report**](CashFlowAnalyticsApi.md#generate_cashflow_analytics_report) | **POST** /decisioning/v2/customers/{customerId}/reports/cashflow-analytics/userTypes/{userType} | Generate Cashflow Analytics Report - Personal/Business |
| [**get_obb_analytics_report**](CashFlowAnalyticsApi.md#get_obb_analytics_report) | **GET** /analytics/data/v1/{obb_report_id} | Get OBB Analytics Report |
| [**get_obb_analytics_report_fcra**](CashFlowAnalyticsApi.md#get_obb_analytics_report_fcra) | **GET** /analytics/data/v1/{obb_report_id}/fcra | Get OBB Analytics Report - FCRA |


## generate_cash_flow_analytics

> <ObbAnalyticsReportAck> generate_cash_flow_analytics(customer_id, balance_and_cash_flow_analytics_report_constraints, opts)

Generate Cash Flow Analytics

Cash Flow Analytics for Business analyzes cash flow over time to report metrics and identify behavior that may indicate risk.  Calculated metrics include: * Average transaction value by month over the requested time period * Net cash flow over the requested time period and broken down by month * Count and report of weeks in the requested time period where there   were zero transactions posted to the customer's accounts  * Minimum/maximum/average/sum/count of deposits by month * Minimum/maximum/average/sum/count of withdrawals by month * Estimated amount of deposits that can be classified as business   revenue  * Number of transactions posted incurring a non-sufficient funds (NSF)   fee, and net amount charged in NSF fees   This version of the API is intended for piloting and integration testing your application with the Cash Flow Analytics product. It does not adhere to FCRA requirements, and should not be used for production/lending purposes. See _Generate Cash Flow Analytics - FCRA_ for the FCRA compliant version of this API.  A successful call to this API will generate analytics and store a report within Finicity. The report can be retrieved via _Get Cash Flow Analytics Report_ (operation: _GetCashFlowAnalyticsReport_).  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CashFlowAnalyticsApi.new
customer_id = '1005061234' # String | A customer ID
balance_and_cash_flow_analytics_report_constraints = OpenBanking::BalanceAndCashFlowAnalyticsReportConstraints.new # BalanceAndCashFlowAnalyticsReportConstraints | 
opts = {
  reference_number: 'abc123' # String | Partner-provided reference number to correlate reports.
}

begin
  # Generate Cash Flow Analytics
  result = api_instance.generate_cash_flow_analytics(customer_id, balance_and_cash_flow_analytics_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowAnalyticsApi->generate_cash_flow_analytics: #{e}"
end
```

#### Using the generate_cash_flow_analytics_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ObbAnalyticsReportAck>, Integer, Hash)> generate_cash_flow_analytics_with_http_info(customer_id, balance_and_cash_flow_analytics_report_constraints, opts)

```ruby
begin
  # Generate Cash Flow Analytics
  data, status_code, headers = api_instance.generate_cash_flow_analytics_with_http_info(customer_id, balance_and_cash_flow_analytics_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ObbAnalyticsReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowAnalyticsApi->generate_cash_flow_analytics_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **balance_and_cash_flow_analytics_report_constraints** | [**BalanceAndCashFlowAnalyticsReportConstraints**](BalanceAndCashFlowAnalyticsReportConstraints.md) |  |  |
| **reference_number** | **String** | Partner-provided reference number to correlate reports. | [optional] |

### Return type

[**ObbAnalyticsReportAck**](ObbAnalyticsReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_cash_flow_analytics_fcra

> <ObbAnalyticsReportAck> generate_cash_flow_analytics_fcra(customer_id, balance_and_cash_flow_analytics_report_constraints, opts)

Generate Cash Flow Analytics - FCRA

Cash Flow Analytics for Business analyzes cash flow over time to report metrics and identify behavior that may indicate risk.  Calculated metrics include: * Average transaction value by month over the requested time period * Net cash flow over the requested time period and broken down by month * Count and report of weeks in the requested time period where there   were zero transactions posted to the customer's accounts  * Minimum/maximum/average/sum/count of deposits by month * Minimum/maximum/average/sum/count of withdrawals by month * Estimated amount of deposits that can be classified as business   revenue  * Number of transactions posted incurring a non-sufficient funds (NSF)   fee, and net amount charged in NSF fees   This version of the API is intended for production use. It maintains and enforces all compliance with FCRA rules and requirements.  *Note:* this is a premium service, billable per every successful API call for non-testing customers.  A successful call to this API will generate analytics and store a report within Finicity. The report can be retrieved via _Get Cash Flow Analytics Report - FCRA_ (operation: _GetCashFlowAnalyticsReportFCRA_).  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CashFlowAnalyticsApi.new
customer_id = '1005061234' # String | A customer ID
balance_and_cash_flow_analytics_report_constraints = OpenBanking::BalanceAndCashFlowAnalyticsReportConstraints.new # BalanceAndCashFlowAnalyticsReportConstraints | 
opts = {
  reference_number: 'abc123' # String | Partner-provided reference number to correlate reports.
}

begin
  # Generate Cash Flow Analytics - FCRA
  result = api_instance.generate_cash_flow_analytics_fcra(customer_id, balance_and_cash_flow_analytics_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowAnalyticsApi->generate_cash_flow_analytics_fcra: #{e}"
end
```

#### Using the generate_cash_flow_analytics_fcra_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ObbAnalyticsReportAck>, Integer, Hash)> generate_cash_flow_analytics_fcra_with_http_info(customer_id, balance_and_cash_flow_analytics_report_constraints, opts)

```ruby
begin
  # Generate Cash Flow Analytics - FCRA
  data, status_code, headers = api_instance.generate_cash_flow_analytics_fcra_with_http_info(customer_id, balance_and_cash_flow_analytics_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ObbAnalyticsReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowAnalyticsApi->generate_cash_flow_analytics_fcra_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **balance_and_cash_flow_analytics_report_constraints** | [**BalanceAndCashFlowAnalyticsReportConstraints**](BalanceAndCashFlowAnalyticsReportConstraints.md) |  |  |
| **reference_number** | **String** | Partner-provided reference number to correlate reports. | [optional] |

### Return type

[**ObbAnalyticsReportAck**](ObbAnalyticsReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## generate_cashflow_analytics_report

> <AnalyticsReportAck> generate_cashflow_analytics_report(customer_id, user_type, analytics_report_constraints, opts)

Generate Cashflow Analytics Report - Personal/Business

Generate a Cashflow Analytics Report for a given customer. This service retrieves up to two years of transaction history from connected accounts.  Cashflow Analytics analyzes transaction over time to report metrics and identify behavior that may indicate risk.  Before calling this API, a consumer or business may need to be created for the given customer ID based on the user type (see Consumer/Business APIs).  If no account type of checking or savings is found, the service will return HTTP 400 Bad Request.  This is a premium service, billable per every successful API call for non-testing customers. A successful call to this API will generate analytics report which can be retrieved via Get Report by Customer or Get Report by Consumer.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CashFlowAnalyticsApi.new
customer_id = '1005061234' # String | A customer ID
user_type = 'personal' # String | UserType indicates if the request is for a business or personal use case, Allowed values: business/personal.
analytics_report_constraints = OpenBanking::AnalyticsReportConstraints.new # AnalyticsReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate Cashflow Analytics Report - Personal/Business
  result = api_instance.generate_cashflow_analytics_report(customer_id, user_type, analytics_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowAnalyticsApi->generate_cashflow_analytics_report: #{e}"
end
```

#### Using the generate_cashflow_analytics_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AnalyticsReportAck>, Integer, Hash)> generate_cashflow_analytics_report_with_http_info(customer_id, user_type, analytics_report_constraints, opts)

```ruby
begin
  # Generate Cashflow Analytics Report - Personal/Business
  data, status_code, headers = api_instance.generate_cashflow_analytics_report_with_http_info(customer_id, user_type, analytics_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AnalyticsReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowAnalyticsApi->generate_cashflow_analytics_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **user_type** | **String** | UserType indicates if the request is for a business or personal use case, Allowed values: business/personal. |  |
| **analytics_report_constraints** | [**AnalyticsReportConstraints**](AnalyticsReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**AnalyticsReportAck**](AnalyticsReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## get_obb_analytics_report

> <ObbAnalyticsReport> get_obb_analytics_report(obb_report_id)

Get OBB Analytics Report

Retrieve the report saved by _Generate Balance Analytics_, _Generate Cash Flow Analytics_, or _Generate Payment History_. Requires the report ID generated by the previous call.  Report data can either be retrieved as a JSON document or a PDF file.  To specify the format required, set the _Accept request header_ to either **application/json** or **application/pdf**. If neither is set, the report format will be returned as a JSON document.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CashFlowAnalyticsApi.new
obb_report_id = 'bcab9592-e032-4e7b-b737-0380619a0573' # String | Report ID generated and returned by OBB products

begin
  # Get OBB Analytics Report
  result = api_instance.get_obb_analytics_report(obb_report_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowAnalyticsApi->get_obb_analytics_report: #{e}"
end
```

#### Using the get_obb_analytics_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ObbAnalyticsReport>, Integer, Hash)> get_obb_analytics_report_with_http_info(obb_report_id)

```ruby
begin
  # Get OBB Analytics Report
  data, status_code, headers = api_instance.get_obb_analytics_report_with_http_info(obb_report_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ObbAnalyticsReport>
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowAnalyticsApi->get_obb_analytics_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **obb_report_id** | **String** | Report ID generated and returned by OBB products |  |

### Return type

[**ObbAnalyticsReport**](ObbAnalyticsReport.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/pdf


## get_obb_analytics_report_fcra

> <ObbAnalyticsReport> get_obb_analytics_report_fcra(obb_report_id, purpose)

Get OBB Analytics Report - FCRA

Retrieve the report saved by _Generate Balance Analytics - FCRA_, _Generate Cash Flow Analytics - FCRA_, or _Generate Payment History - FCRA_. Requires the report ID generated by the previous call.  Report data can either be retrieved as a JSON document or a PDF file.  To specify the format required, set the _Accept request header_ to either **application/json** or **application/pdf**. If neither is set, the report format will be returned as a JSON document.  *Note:* this is a premium service, billable per every successful API call for non-testing customers.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CashFlowAnalyticsApi.new
obb_report_id = 'bcab9592-e032-4e7b-b737-0380619a0573' # String | Report ID generated and returned by OBB products
purpose = '3F' # String | 2-digit code from [Permissible Purpose Codes](https://developer.mastercard.com/open-banking-us/documentation/products/lend/report-handling/permissible-purpose-codes/), specifying the reason for retrieving this report. Required for retrieving some reports.

begin
  # Get OBB Analytics Report - FCRA
  result = api_instance.get_obb_analytics_report_fcra(obb_report_id, purpose)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowAnalyticsApi->get_obb_analytics_report_fcra: #{e}"
end
```

#### Using the get_obb_analytics_report_fcra_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ObbAnalyticsReport>, Integer, Hash)> get_obb_analytics_report_fcra_with_http_info(obb_report_id, purpose)

```ruby
begin
  # Get OBB Analytics Report - FCRA
  data, status_code, headers = api_instance.get_obb_analytics_report_fcra_with_http_info(obb_report_id, purpose)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ObbAnalyticsReport>
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowAnalyticsApi->get_obb_analytics_report_fcra_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **obb_report_id** | **String** | Report ID generated and returned by OBB products |  |
| **purpose** | **String** | 2-digit code from [Permissible Purpose Codes](https://developer.mastercard.com/open-banking-us/documentation/products/lend/report-handling/permissible-purpose-codes/), specifying the reason for retrieving this report. Required for retrieving some reports. |  |

### Return type

[**ObbAnalyticsReport**](ObbAnalyticsReport.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/pdf

