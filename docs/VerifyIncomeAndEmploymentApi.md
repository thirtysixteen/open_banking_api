# OpenBanking::VerifyIncomeAndEmploymentApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**generate_pay_statement_report**](VerifyIncomeAndEmploymentApi.md#generate_pay_statement_report) | **POST** /decisioning/v2/customers/{customerId}/payStatement | Generate Pay Statement Report |
| [**generate_voe_payroll_report**](VerifyIncomeAndEmploymentApi.md#generate_voe_payroll_report) | **POST** /decisioning/v2/customers/{customerId}/voePayroll | Generate VOE - Payroll Report |
| [**generate_voe_transactions_report**](VerifyIncomeAndEmploymentApi.md#generate_voe_transactions_report) | **POST** /decisioning/v2/customers/{customerId}/voeTransactions | Generate VOE - Transactions Report |
| [**generate_voi_report**](VerifyIncomeAndEmploymentApi.md#generate_voi_report) | **POST** /decisioning/v2/customers/{customerId}/voi | Generate VOI Report |
| [**generate_voie_paystub_report**](VerifyIncomeAndEmploymentApi.md#generate_voie_paystub_report) | **POST** /decisioning/v2/customers/{customerId}/voieTxVerify/withStatement | Generate VOIE - Paystub Report |
| [**generate_voie_paystub_with_tx_verify_report**](VerifyIncomeAndEmploymentApi.md#generate_voie_paystub_with_tx_verify_report) | **POST** /decisioning/v2/customers/{customerId}/voieTxVerify/withInterview | Generate VOIE - Paystub (with TXVerify) Report |
| [**refresh_voie_payroll_report**](VerifyIncomeAndEmploymentApi.md#refresh_voie_payroll_report) | **POST** /decisioning/v2/customers/{customerId}/voiePayroll | Generate VOIE - Payroll Report |


## generate_pay_statement_report

> <PayStatementReportAck> generate_pay_statement_report(customer_id, pay_statement_report_constraints, opts)

Generate Pay Statement Report

Generate Pay Statement Extraction Report for the given customer. This service accepts asset IDs of the stored pay statements to generate a Pay Statement Extraction Report.  This is a premium service. The billing rate is the variable rate for Pay Statement Extraction Report under the current subscription plan. The billable event is the successful generation of a Pay Statement Extraction Report.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::VerifyIncomeAndEmploymentApi.new
customer_id = '1005061234' # String | A customer ID
pay_statement_report_constraints = OpenBanking::PayStatementReportConstraints.new({paystatement_report: OpenBanking::PayStatementData.new({asset_ids: ['097545c5-1c2a-4f20-a5ef-77f0820344c9-2018601178']})}) # PayStatementReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate Pay Statement Report
  result = api_instance.generate_pay_statement_report(customer_id, pay_statement_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_pay_statement_report: #{e}"
end
```

#### Using the generate_pay_statement_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayStatementReportAck>, Integer, Hash)> generate_pay_statement_report_with_http_info(customer_id, pay_statement_report_constraints, opts)

```ruby
begin
  # Generate Pay Statement Report
  data, status_code, headers = api_instance.generate_pay_statement_report_with_http_info(customer_id, pay_statement_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayStatementReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_pay_statement_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **pay_statement_report_constraints** | [**PayStatementReportConstraints**](PayStatementReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**PayStatementReportAck**](PayStatementReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_voe_payroll_report

> <PayrollReportAck> generate_voe_payroll_report(customer_id, payroll_report_constraints, opts)

Generate VOE - Payroll Report

Generate or refresh a VOE - Payroll report. Often used as a complementary report to the VOIE-Payroll report to fulfill the pre-close VOE requirements. It retrieves the customer's employment details and employment status through the payroll source without any income information.  This is a premium service. The billable event is the successful generation of a VOE - Payroll report.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::VerifyIncomeAndEmploymentApi.new
customer_id = '1005061234' # String | A customer ID
payroll_report_constraints = OpenBanking::PayrollReportConstraints.new({payroll_data: OpenBanking::PayrollData.new({ssn: '999999999', dob: 1607450357})}) # PayrollReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate VOE - Payroll Report
  result = api_instance.generate_voe_payroll_report(customer_id, payroll_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_voe_payroll_report: #{e}"
end
```

#### Using the generate_voe_payroll_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayrollReportAck>, Integer, Hash)> generate_voe_payroll_report_with_http_info(customer_id, payroll_report_constraints, opts)

```ruby
begin
  # Generate VOE - Payroll Report
  data, status_code, headers = api_instance.generate_voe_payroll_report_with_http_info(customer_id, payroll_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayrollReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_voe_payroll_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **payroll_report_constraints** | [**PayrollReportConstraints**](PayrollReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**PayrollReportAck**](PayrollReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_voe_transactions_report

> <VOETransactionsReportAck> generate_voe_transactions_report(customer_id, voe_transactions_report_constraints, opts)

Generate VOE - Transactions Report

Premium Service: A billable event when the API response is successful.  MVS-Direct integration developers only.  Used as a complimentary report to the VOA with Income and VOIE - Paystub (with TXVerify) reports and used to fulfill the pre-close VOE requirements.  Retrieve the latest credit transaction information from the borrower's connected bank accounts and groups them into income streams so that you can view their payment history to ensure a direct deport was made within the expected cadence. The report displays transaction descriptions without any dollar amounts so that income re-verification isn't necessary.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::VerifyIncomeAndEmploymentApi.new
customer_id = '1005061234' # String | A customer ID
voe_transactions_report_constraints = OpenBanking::VOETransactionsReportConstraints.new # VOETransactionsReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate VOE - Transactions Report
  result = api_instance.generate_voe_transactions_report(customer_id, voe_transactions_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_voe_transactions_report: #{e}"
end
```

#### Using the generate_voe_transactions_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<VOETransactionsReportAck>, Integer, Hash)> generate_voe_transactions_report_with_http_info(customer_id, voe_transactions_report_constraints, opts)

```ruby
begin
  # Generate VOE - Transactions Report
  data, status_code, headers = api_instance.generate_voe_transactions_report_with_http_info(customer_id, voe_transactions_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <VOETransactionsReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_voe_transactions_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **voe_transactions_report_constraints** | [**VOETransactionsReportConstraints**](VOETransactionsReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**VOETransactionsReportAck**](VOETransactionsReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_voi_report

> <VOIReportAck> generate_voi_report(customer_id, voi_report_constraints, opts)

Generate VOI Report

Generate a Verification of Income (VOI) report for all checking, savings, and money market accounts for the given customer. This service retrieves up to two years of transaction history for each account and uses this information to generate the VOI report.  This is a premium service. The billing rate is the variable rate for Verification of Income under the current subscription plan. The billable event is the successful generation of a VOI report.  If no account of type checking, savings, or money market is found, the service will return HTTP 400 Bad Request.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::VerifyIncomeAndEmploymentApi.new
customer_id = '1005061234' # String | A customer ID
voi_report_constraints = OpenBanking::VOIReportConstraints.new # VOIReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate VOI Report
  result = api_instance.generate_voi_report(customer_id, voi_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_voi_report: #{e}"
end
```

#### Using the generate_voi_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<VOIReportAck>, Integer, Hash)> generate_voi_report_with_http_info(customer_id, voi_report_constraints, opts)

```ruby
begin
  # Generate VOI Report
  data, status_code, headers = api_instance.generate_voi_report_with_http_info(customer_id, voi_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <VOIReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_voi_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **voi_report_constraints** | [**VOIReportConstraints**](VOIReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**VOIReportAck**](VOIReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_voie_paystub_report

> <VOIEPaystubReportAck> generate_voie_paystub_report(customer_id, voie_report_constraints, opts)

Generate VOIE - Paystub Report

Generate a VOIE - Paystub report. This service uses the provided paystub(s), which are passed into the request body as asset IDs (generated using the Store Customer Pay Statement API) to generate the VOIE - Paystub report with digitized paystub details.  This is a premium service. The billing rate is the variable rate for VOIE - Paystub under the current subscription plan. The billable event is the successful generation of a VOIE - Paystub Report.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::VerifyIncomeAndEmploymentApi.new
customer_id = '1005061234' # String | A customer ID
voie_report_constraints = OpenBanking::VOIEReportConstraints.new({voie_with_statement_data: OpenBanking::VOIEWithStatementData.new({asset_ids: ['097545c5-1c2a-4f20-a5ef-77f0820344c9-2018601178']})}) # VOIEReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate VOIE - Paystub Report
  result = api_instance.generate_voie_paystub_report(customer_id, voie_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_voie_paystub_report: #{e}"
end
```

#### Using the generate_voie_paystub_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<VOIEPaystubReportAck>, Integer, Hash)> generate_voie_paystub_report_with_http_info(customer_id, voie_report_constraints, opts)

```ruby
begin
  # Generate VOIE - Paystub Report
  data, status_code, headers = api_instance.generate_voie_paystub_report_with_http_info(customer_id, voie_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <VOIEPaystubReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_voie_paystub_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **voie_report_constraints** | [**VOIEReportConstraints**](VOIEReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**VOIEPaystubReportAck**](VOIEPaystubReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## generate_voie_paystub_with_tx_verify_report

> <VOIEPaystubWithTXVerifyReportAck> generate_voie_paystub_with_tx_verify_report(customer_id, voie_with_tx_verify_report_constraints, opts)

Generate VOIE - Paystub (with TXVerify) Report

Generate a VOIE - Paystub (with TXVerify) report for all checking and savings under the given customer. This service retrieves up to two years of transaction history for the given accounts. It then uses this information as well as the provided paystub(s), which are passed into the request body as asset IDs (generated using the Store Customer Pay Statement API) to generate the VOIE - Paystub (with TXVerify) report.  Note: if you are using this API to refresh the bank transactions, use the same asset ID from the first report. A new paystub is not required unless the paystub is too old for underwriting requirements. Using the same asset ID that was on the original report and the previously extracted details will be used to speed up report generation response time.  This is a premium service. The billing rate is the variable rate for VOIE TXVerify under the current subscription plan. The billable event is the successful generation of a VOIE TXVerify Report.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::VerifyIncomeAndEmploymentApi.new
customer_id = '1005061234' # String | A customer ID
voie_with_tx_verify_report_constraints = OpenBanking::VOIEWithTXVerifyReportConstraints.new({voie_with_interview_data: OpenBanking::VOIEWithInterviewData.new({tx_verify_interview: [OpenBanking::TxVerifyInterview.new({asset_id: '097545c5-1c2a-4f20-a5ef-77f0820344c9-2018601178'})]})}) # VOIEWithTXVerifyReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate VOIE - Paystub (with TXVerify) Report
  result = api_instance.generate_voie_paystub_with_tx_verify_report(customer_id, voie_with_tx_verify_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_voie_paystub_with_tx_verify_report: #{e}"
end
```

#### Using the generate_voie_paystub_with_tx_verify_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<VOIEPaystubWithTXVerifyReportAck>, Integer, Hash)> generate_voie_paystub_with_tx_verify_report_with_http_info(customer_id, voie_with_tx_verify_report_constraints, opts)

```ruby
begin
  # Generate VOIE - Paystub (with TXVerify) Report
  data, status_code, headers = api_instance.generate_voie_paystub_with_tx_verify_report_with_http_info(customer_id, voie_with_tx_verify_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <VOIEPaystubWithTXVerifyReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->generate_voie_paystub_with_tx_verify_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **voie_with_tx_verify_report_constraints** | [**VOIEWithTXVerifyReportConstraints**](VOIEWithTXVerifyReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**VOIEPaystubWithTXVerifyReportAck**](VOIEPaystubWithTXVerifyReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## refresh_voie_payroll_report

> <PayrollReportAck> refresh_voie_payroll_report(customer_id, payroll_report_constraints, opts)

Generate VOIE - Payroll Report

Generate or refresh a VOIE - Payroll report. For clients using the product via a consumer permissioning experience via Connect, the original VOIE - Payroll report generates when the consumer completes the Connect experience, and this API is only used for future report refreshes without reengaging the consumer.  This is a premium service. The billable event is the successful generation of a VOIE - Payroll report.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::VerifyIncomeAndEmploymentApi.new
customer_id = '1005061234' # String | A customer ID
payroll_report_constraints = OpenBanking::PayrollReportConstraints.new({payroll_data: OpenBanking::PayrollData.new({ssn: '999999999', dob: 1607450357})}) # PayrollReportConstraints | 
opts = {
  callback_url: 'https://finicity-test/webhook' # String | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code.
}

begin
  # Generate VOIE - Payroll Report
  result = api_instance.refresh_voie_payroll_report(customer_id, payroll_report_constraints, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->refresh_voie_payroll_report: #{e}"
end
```

#### Using the refresh_voie_payroll_report_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayrollReportAck>, Integer, Hash)> refresh_voie_payroll_report_with_http_info(customer_id, payroll_report_constraints, opts)

```ruby
begin
  # Generate VOIE - Payroll Report
  data, status_code, headers = api_instance.refresh_voie_payroll_report_with_http_info(customer_id, payroll_report_constraints, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayrollReportAck>
rescue OpenBanking::ApiError => e
  puts "Error when calling VerifyIncomeAndEmploymentApi->refresh_voie_payroll_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **payroll_report_constraints** | [**PayrollReportConstraints**](PayrollReportConstraints.md) |  |  |
| **callback_url** | **String** | A Report Listener URL to receive notifications. The webhook must respond to the Finicity API with a 2xx HTTP status code. | [optional] |

### Return type

[**PayrollReportAck**](PayrollReportAck.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain

