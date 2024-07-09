# OpenBanking::CashFlowApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**generate_cash_flow_business_report**](CashFlowApi.md#generate_cash_flow_business_report) | **POST** /decisioning/v2/customers/{customerId}/cashFlowBusiness | Generate Cash Flow Report - Business |
| [**generate_cash_flow_personal_report**](CashFlowApi.md#generate_cash_flow_personal_report) | **POST** /decisioning/v2/customers/{customerId}/cashFlowPersonal | Generate Cash Flow Report - Personal |


## generate_cash_flow_business_report

> <CashFlowReportAck> generate_cash_flow_business_report(customer_id, cash_flow_report_constraints, opts)

Generate Cash Flow Report - Business

Generate a Cash Flow Report (Business) report for all checking and savings under the given customer. This service retrieves up to two years of transaction history for the given account. It then uses this information to generate the CFR report. A consumer is not required to generate this report.  This report is not provided under FCRA rules, and this report is not available in the Finicity Consumer Portal for the borrower to view.  If no account type of checking or savings is found, the service will return HTTP 400 Bad Request.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CashFlowApi.new
customer_id = '1005061234' # String | A customer ID
cash_flow_report_constraints = OpenBanking::CashFlowReportConstraints.new # CashFlowReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate Cash Flow Report - Business
  result = api_instance.generate_cash_flow_business_report(customer_id, cash_flow_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowApi->generate_cash_flow_business_report: #{e}"
end
```

#### Using the generate_cash_flow_business_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CashFlowReportAck>, Integer, Hash)> generate_cash_flow_business_report_with_http_info(customer_id, cash_flow_report_constraints, opts)

```ruby
begin
  # Generate Cash Flow Report - Business
  data, status_code, headers = api_instance.generate_cash_flow_business_report_with_http_info(customer_id, cash_flow_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CashFlowReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowApi->generate_cash_flow_business_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **cash_flow_report_constraints** | [**CashFlowReportConstraints**](CashFlowReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**CashFlowReportAck**](CashFlowReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_cash_flow_personal_report

> <CashFlowReportAck> generate_cash_flow_personal_report(customer_id, cash_flow_report_constraints, opts)

Generate Cash Flow Report - Personal

Generate a Cash Flow Report (Personal) report for all checking and savings under the given customer. This service retrieves up to two years of transaction history for the given account. It then uses this information to generate the CFR report.  This report is provided under FCRA rules, with Finicity acting as the CRA (Consumer Reporting Agency). If an individual account is included in the report - for example, with an individual acting as an personal guarantor on the loan - then this version of the report should be used. In case of an adverse action on the loan where the decision was based on this report, then the borrower can be referred to the [Finicity Consumer Portal](https://consumer.finicityreports.com) where they can view this report and submit a dispute if they feel any information in this report is inaccurate.  Before calling this API, a consumer must be created for the given customer ID (see Consumers APIs).  If no account type of checking or savings is found, the service will return HTTP 400 Bad Request.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::CashFlowApi.new
customer_id = '1005061234' # String | A customer ID
cash_flow_report_constraints = OpenBanking::CashFlowReportConstraints.new # CashFlowReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate Cash Flow Report - Personal
  result = api_instance.generate_cash_flow_personal_report(customer_id, cash_flow_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowApi->generate_cash_flow_personal_report: #{e}"
end
```

#### Using the generate_cash_flow_personal_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CashFlowReportAck>, Integer, Hash)> generate_cash_flow_personal_report_with_http_info(customer_id, cash_flow_report_constraints, opts)

```ruby
begin
  # Generate Cash Flow Report - Personal
  data, status_code, headers = api_instance.generate_cash_flow_personal_report_with_http_info(customer_id, cash_flow_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CashFlowReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling CashFlowApi->generate_cash_flow_personal_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **cash_flow_report_constraints** | [**CashFlowReportConstraints**](CashFlowReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**CashFlowReportAck**](CashFlowReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain

