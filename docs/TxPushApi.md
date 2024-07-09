# OpenBanking::TxPushApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_tx_push_test_transaction**](TxPushApi.md#create_tx_push_test_transaction) | **POST** /aggregation/v1/customers/{customerId}/accounts/{accountId}/transactions | Create TxPush Test Transaction |
| [**delete_tx_push_subscription**](TxPushApi.md#delete_tx_push_subscription) | **DELETE** /aggregation/v1/customers/{customerId}/subscriptions/{subscriptionId} | Delete TxPush Subscription |
| [**disable_tx_push_notifications**](TxPushApi.md#disable_tx_push_notifications) | **DELETE** /aggregation/v1/customers/{customerId}/accounts/{accountId}/txpush | Disable TxPush Notifications |
| [**subscribe_to_tx_push_notifications**](TxPushApi.md#subscribe_to_tx_push_notifications) | **POST** /aggregation/v1/customers/{customerId}/accounts/{accountId}/txpush | Subscribe to TxPush Notifications |


## create_tx_push_test_transaction

> <CreatedTestTxPushTransaction> create_tx_push_test_transaction(customer_id, account_id, test_tx_push_transaction)

Create TxPush Test Transaction

Inject a transaction into the transaction list for a testing account. This allows an app to trigger TxPush notifications for the account in order to test the app's TxPush Listener service. This causes the platform to send one transaction event and one account event (showing that the account balance has changed). This service is only supported for testing accounts.  For additional details on this process, see [TxPush Listener Service](https://developer.mastercard.com/open-banking-us/documentation/products/manage/tx-push/#setting-up-the-txpush-listener-service).  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::TxPushApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID
test_tx_push_transaction = OpenBanking::TestTxPushTransaction.new({amount: -4.25, description: 'a testing transaction description', transaction_date: 1607450357}) # TestTxPushTransaction | 

begin
  # Create TxPush Test Transaction
  result = api_instance.create_tx_push_test_transaction(customer_id, account_id, test_tx_push_transaction)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling TxPushApi->create_tx_push_test_transaction: #{e}"
end
```

#### Using the create_tx_push_test_transaction_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreatedTestTxPushTransaction>, Integer, Hash)> create_tx_push_test_transaction_with_http_info(customer_id, account_id, test_tx_push_transaction)

```ruby
begin
  # Create TxPush Test Transaction
  data, status_code, headers = api_instance.create_tx_push_test_transaction_with_http_info(customer_id, account_id, test_tx_push_transaction)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreatedTestTxPushTransaction>
rescue OpenBanking::ApiError => e
  puts "Error when calling TxPushApi->create_tx_push_test_transaction_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |
| **test_tx_push_transaction** | [**TestTxPushTransaction**](TestTxPushTransaction.md) |  |  |

### Return type

[**CreatedTestTxPushTransaction**](CreatedTestTxPushTransaction.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## delete_tx_push_subscription

> delete_tx_push_subscription(customer_id, subscription_id)

Delete TxPush Subscription

Delete a specific subscription to TxPush notifications for the given account. This could be individual deleting the account or transactions events. No more events will be sent for that specific subscription.  For additional details on this process, see [TxPush Listener Service](https://developer.mastercard.com/open-banking-us/documentation/products/manage/tx-push/#setting-up-the-txpush-listener-service).  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::TxPushApi.new
customer_id = '1005061234' # String | A customer ID
subscription_id = 17554874 # Integer | The subscription ID

begin
  # Delete TxPush Subscription
  api_instance.delete_tx_push_subscription(customer_id, subscription_id)
rescue OpenBanking::ApiError => e
  puts "Error when calling TxPushApi->delete_tx_push_subscription: #{e}"
end
```

#### Using the delete_tx_push_subscription_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_tx_push_subscription_with_http_info(customer_id, subscription_id)

```ruby
begin
  # Delete TxPush Subscription
  data, status_code, headers = api_instance.delete_tx_push_subscription_with_http_info(customer_id, subscription_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling TxPushApi->delete_tx_push_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **subscription_id** | **Integer** | The subscription ID |  |

### Return type

nil (empty response body)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## disable_tx_push_notifications

> disable_tx_push_notifications(customer_id, account_id)

Disable TxPush Notifications

Delete all TxPush subscriptions with their notifications for the given account. No more notifications will be sent for account or transaction events.  For additional details on this process, see [TxPush Listener Service](https://developer.mastercard.com/open-banking-us/documentation/products/manage/tx-push/#setting-up-the-txpush-listener-service).  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::TxPushApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID

begin
  # Disable TxPush Notifications
  api_instance.disable_tx_push_notifications(customer_id, account_id)
rescue OpenBanking::ApiError => e
  puts "Error when calling TxPushApi->disable_tx_push_notifications: #{e}"
end
```

#### Using the disable_tx_push_notifications_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> disable_tx_push_notifications_with_http_info(customer_id, account_id)

```ruby
begin
  # Disable TxPush Notifications
  data, status_code, headers = api_instance.disable_tx_push_notifications_with_http_info(customer_id, account_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling TxPushApi->disable_tx_push_notifications_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |

### Return type

nil (empty response body)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## subscribe_to_tx_push_notifications

> <TxPushSubscriptions> subscribe_to_tx_push_notifications(customer_id, account_id, tx_push_subscription_parameters)

Subscribe to TxPush Notifications

Register a client app's TxPush Listener to receive TxPush notifications related to the given account.  Each call to this service will return two records, one with class account and one with class transaction. Account events are sent when values change in the account's fields (such as `balance` or `interestRate`). Transaction events are sent whenever a new transaction is posted for the account. For institutions that do not provide TxPush services, notifications are sent as soon as Finicity finds a new transaction or new account data through regular aggregation processes.  The listener's URL must be secure (HTTPS) for any real-world account. In addition, the client's TxPush Listener will need to be verified. HTTP and HTTPS connections are only allowed on the standard ports 80 (HTTP) and 443 (HTTPS). The use of other ports will result with the call failing.  For additional details on this process, see [TxPush Listener Service](https://developer.mastercard.com/open-banking-us/documentation/products/manage/tx-push/#setting-up-the-txpush-listener-service).  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::TxPushApi.new
customer_id = '1005061234' # String | A customer ID
account_id = '5011648377' # String | The account ID
tx_push_subscription_parameters = OpenBanking::TxPushSubscriptionParameters.new({callback_url: 'https://www.mydomain.com/txpush/listener'}) # TxPushSubscriptionParameters | 

begin
  # Subscribe to TxPush Notifications
  result = api_instance.subscribe_to_tx_push_notifications(customer_id, account_id, tx_push_subscription_parameters)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling TxPushApi->subscribe_to_tx_push_notifications: #{e}"
end
```

#### Using the subscribe_to_tx_push_notifications_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TxPushSubscriptions>, Integer, Hash)> subscribe_to_tx_push_notifications_with_http_info(customer_id, account_id, tx_push_subscription_parameters)

```ruby
begin
  # Subscribe to TxPush Notifications
  data, status_code, headers = api_instance.subscribe_to_tx_push_notifications_with_http_info(customer_id, account_id, tx_push_subscription_parameters)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TxPushSubscriptions>
rescue OpenBanking::ApiError => e
  puts "Error when calling TxPushApi->subscribe_to_tx_push_notifications_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **account_id** | **String** | The account ID |  |
| **tx_push_subscription_parameters** | [**TxPushSubscriptionParameters**](TxPushSubscriptionParameters.md) |  |  |

### Return type

[**TxPushSubscriptions**](TxPushSubscriptions.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain

