# OpenBanking::PaymentHistoryApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**generate_payment_history**](PaymentHistoryApi.md#generate_payment_history) | **POST** /analytics/payment-history/v1/customer/{customerId} | Generate Payment History |
| [**generate_payment_history_fcra**](PaymentHistoryApi.md#generate_payment_history_fcra) | **POST** /analytics/payment-history/v1/customer/{customerId}/fcra | Generate Payment History - FCRA |
| [**get_obb_analytics_report**](PaymentHistoryApi.md#get_obb_analytics_report) | **GET** /analytics/data/v1/{obb_report_id} | Get OBB Analytics Report |
| [**get_obb_analytics_report_fcra**](PaymentHistoryApi.md#get_obb_analytics_report_fcra) | **GET** /analytics/data/v1/{obb_report_id}/fcra | Get OBB Analytics Report - FCRA |


## generate_payment_history

> <ObbAnalyticsReportAck> generate_payment_history(customer_id, opts)

Generate Payment History

Payment history report analyzes up to 12-months of transactions and predicts the probability that a SMB will experience a payment risk event, such as NSF/Overdraft or missed recurring payments, in the near future when making a payment. The Risk Score provided in the report is a 2-digit ranking with four levels of risk going from low to high.  Some of the highlights of calculated risk present in the report include: * Risk Score representing the likelihood of a missed payment   based on analysis of permissioned open-banking data  * Monthly average balance for all accounts by month in the requested   time period  * Total deposit amount by month for all accounts in the requested time   period  * Total withdrawal amounts by month for all accounts in the requested   time period  * Number of NSF counts and aggregate amount per month in the requested   time period  * Recurring loan payment amounts per month in the requested time period * Insurance payment amount per month in the requested time period * Tax payment amounts per month in the requested time period  This version of the API is intended for piloting and integration testing your application with the Payment History product. It does not adhere to FCRA requirements, and should not be used for production/lending purposes. See _Generate Payment History - FCRA_ for the FCRA compliant version of this API.  *Note:* this is a premium service, billable per every successful API call for non-testing customers.  A successful call to this API will generate analytics and store a report within Finicity. The report can be retrieved via _Get OBB Analytics Report_ (operation: _GetObbAnalyticsReport_). *Note:* this is a premium service, billable per every successful API call for non-testing customers.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::PaymentHistoryApi.new
customer_id = '1005061234' # String | A customer ID
opts = {
  reference_number: 'abc123' # String | Partner-provided reference number to correlate reports.
}

begin
  # Generate Payment History
  result = api_instance.generate_payment_history(customer_id, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentHistoryApi->generate_payment_history: #{e}"
end
```

#### Using the generate_payment_history_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ObbAnalyticsReportAck>, Integer, Hash)> generate_payment_history_with_http_info(customer_id, opts)

```ruby
begin
  # Generate Payment History
  data, status_code, headers = api_instance.generate_payment_history_with_http_info(customer_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ObbAnalyticsReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentHistoryApi->generate_payment_history_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **reference_number** | **String** | Partner-provided reference number to correlate reports. | [optional] |

### Return type

[**ObbAnalyticsReportAck**](ObbAnalyticsReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## generate_payment_history_fcra

> <ObbAnalyticsReportAck> generate_payment_history_fcra(customer_id, opts)

Generate Payment History - FCRA

Payment history report analyzes up to 12-months of transactions and predicts the probability that a SMB will experience a payment risk event, such as NSF/Overdraft or missed recurring payments, in the near future when making a payment. The Risk Score provided in the report is a 2-digit ranking with four levels of risk going from low to high.  Some of the highlights of calculated risk present in the report include: * Risk Score representing the likelihood of a missed payment   based on analysis of permissioned open-banking data  * Monthly average balance for all accounts by month in the requested   time period  * Total deposit amount by month for all accounts in the requested time   period  * Total withdrawal amounts by month for all accounts in the requested   time period  * Number of NSF counts and aggregate amount per month in the requested   time period  * Recurring loan payment amounts per month in the requested time period * Insurance payment amount per month in the requested time period * Tax payment amounts per month in the requested time period  This version of the API is intended for production use. It maintains and  enforces all compliance with FCRA rules and requirements.   *Note:* this is a premium service, billable per every successful API call for non-testing customers.  A successful call to this API will generate analytics and store a report within Finicity. The report can be retrieved via _Get OBB Analytics Report - FCRA_  (operation: _GetObbAnalyticsReportFcra_).  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::PaymentHistoryApi.new
customer_id = '1005061234' # String | A customer ID
opts = {
  reference_number: 'abc123' # String | Partner-provided reference number to correlate reports.
}

begin
  # Generate Payment History - FCRA
  result = api_instance.generate_payment_history_fcra(customer_id, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentHistoryApi->generate_payment_history_fcra: #{e}"
end
```

#### Using the generate_payment_history_fcra_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ObbAnalyticsReportAck>, Integer, Hash)> generate_payment_history_fcra_with_http_info(customer_id, opts)

```ruby
begin
  # Generate Payment History - FCRA
  data, status_code, headers = api_instance.generate_payment_history_fcra_with_http_info(customer_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ObbAnalyticsReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentHistoryApi->generate_payment_history_fcra_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **reference_number** | **String** | Partner-provided reference number to correlate reports. | [optional] |

### Return type

[**ObbAnalyticsReportAck**](ObbAnalyticsReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


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

api_instance = OpenBanking::PaymentHistoryApi.new
obb_report_id = 'bcab9592-e032-4e7b-b737-0380619a0573' # String | Report ID generated and returned by OBB products

begin
  # Get OBB Analytics Report
  result = api_instance.get_obb_analytics_report(obb_report_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentHistoryApi->get_obb_analytics_report: #{e}"
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
  puts "Error when calling PaymentHistoryApi->get_obb_analytics_report_with_http_info: #{e}"
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

api_instance = OpenBanking::PaymentHistoryApi.new
obb_report_id = 'bcab9592-e032-4e7b-b737-0380619a0573' # String | Report ID generated and returned by OBB products
purpose = '3F' # String | 2-digit code from [Permissible Purpose Codes](https://developer.mastercard.com/open-banking-us/documentation/products/lend/report-handling/permissible-purpose-codes/), specifying the reason for retrieving this report. Required for retrieving some reports.

begin
  # Get OBB Analytics Report - FCRA
  result = api_instance.get_obb_analytics_report_fcra(obb_report_id, purpose)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PaymentHistoryApi->get_obb_analytics_report_fcra: #{e}"
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
  puts "Error when calling PaymentHistoryApi->get_obb_analytics_report_fcra_with_http_info: #{e}"
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

