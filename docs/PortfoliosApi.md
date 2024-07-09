# OpenBanking::PortfoliosApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_portfolio_by_consumer**](PortfoliosApi.md#get_portfolio_by_consumer) | **GET** /decisioning/v1/consumers/{consumerId}/portfolios/{portfolioId} | Get Portfolio by Consumer |
| [**get_portfolio_by_customer**](PortfoliosApi.md#get_portfolio_by_customer) | **GET** /decisioning/v1/customers/{customerId}/portfolios/{portfolioId} | Get Portfolio by Customer |


## get_portfolio_by_consumer

> <PortfolioWithConsumerSummary> get_portfolio_by_consumer(consumer_id, portfolio_id)

Get Portfolio by Consumer

Return a portfolio of most recently generated reports for each report type for a given consumer. If there are multiple reports that were generated for a report type (VOA, VOI, etc.), only the most recently generated report for the type will be returned.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::PortfoliosApi.new
consumer_id = '0bf46322c167b562e6cbed9d40e19a4c' # String | The consumer ID
portfolio_id = 'y4zsgccj4xpw-6-port' # String | A portfolio ID with the portfolio version number. Using the portfolio number without a version number will return the most recently generated reports.

begin
  # Get Portfolio by Consumer
  result = api_instance.get_portfolio_by_consumer(consumer_id, portfolio_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PortfoliosApi->get_portfolio_by_consumer: #{e}"
end
```

#### Using the get_portfolio_by_consumer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PortfolioWithConsumerSummary>, Integer, Hash)> get_portfolio_by_consumer_with_http_info(consumer_id, portfolio_id)

```ruby
begin
  # Get Portfolio by Consumer
  data, status_code, headers = api_instance.get_portfolio_by_consumer_with_http_info(consumer_id, portfolio_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PortfolioWithConsumerSummary>
rescue OpenBanking::ApiError => e
  puts "Error when calling PortfoliosApi->get_portfolio_by_consumer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **consumer_id** | **String** | The consumer ID |  |
| **portfolio_id** | **String** | A portfolio ID with the portfolio version number. Using the portfolio number without a version number will return the most recently generated reports. |  |

### Return type

[**PortfolioWithConsumerSummary**](PortfolioWithConsumerSummary.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_portfolio_by_customer

> <PortfolioSummary> get_portfolio_by_customer(customer_id, portfolio_id)

Get Portfolio by Customer

Return a portfolio of most recently generated reports for each report type for the given customer. If there are multiple reports that were generated for a report type (VOA, VOI, etc.), only the most recently generated report for the type will be returned.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png) 

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

api_instance = OpenBanking::PortfoliosApi.new
customer_id = '1005061234' # String | A customer ID
portfolio_id = 'y4zsgccj4xpw-6-port' # String | A portfolio ID with the portfolio version number. Using the portfolio number without a version number will return the most recently generated reports.

begin
  # Get Portfolio by Customer
  result = api_instance.get_portfolio_by_customer(customer_id, portfolio_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling PortfoliosApi->get_portfolio_by_customer: #{e}"
end
```

#### Using the get_portfolio_by_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PortfolioSummary>, Integer, Hash)> get_portfolio_by_customer_with_http_info(customer_id, portfolio_id)

```ruby
begin
  # Get Portfolio by Customer
  data, status_code, headers = api_instance.get_portfolio_by_customer_with_http_info(customer_id, portfolio_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PortfolioSummary>
rescue OpenBanking::ApiError => e
  puts "Error when calling PortfoliosApi->get_portfolio_by_customer_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **portfolio_id** | **String** | A portfolio ID with the portfolio version number. Using the portfolio number without a version number will return the most recently generated reports. |  |

### Return type

[**PortfolioSummary**](PortfolioSummary.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain

