# OpenBanking::AppRegistrationApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_app_registration_status**](AppRegistrationApi.md#get_app_registration_status) | **GET** /aggregation/v2/partners/applications | Get App Registration Status |
| [**get_applications**](AppRegistrationApi.md#get_applications) | **GET** /applications | Get applications details. |
| [**get_registered_institutions**](AppRegistrationApi.md#get_registered_institutions) | **GET** /applications/{application_id}/institutions | Get the application registration status with the financial institutions. |
| [**migrate_institution_login_accounts**](AppRegistrationApi.md#migrate_institution_login_accounts) | **PUT** /aggregation/v2/customers/{customerId}/institutionLogins/{institutionLoginId}/migration | Migrate Institution Login Accounts |
| [**modify_app_registration**](AppRegistrationApi.md#modify_app_registration) | **PUT** /aggregation/v1/partners/applications/{preAppId} | Modify App Registration |
| [**register_app**](AppRegistrationApi.md#register_app) | **POST** /aggregation/v1/partners/applications | Register App |
| [**set_customer_app_id**](AppRegistrationApi.md#set_customer_app_id) | **PUT** /aggregation/v1/customers/{customerId}/applications/{applicationId} | Set Customer App ID |


## get_app_registration_status

> <AppStatuses> get_app_registration_status(opts)

Get App Registration Status

Get the status of your application registration(s).  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AppRegistrationApi.new
opts = {
  pre_app_id: '2581', # String | The application registration tracking ID
  application_id: '123456789', # String | The application ID
  status: 'P', # String | Look up app registration requests by status
  app_name: 'Awesome Budget App', # String | Look up app registration requests by app name
  submitted_date: 1607450357, # Integer | Look up app registration requests by the date they were submitted
  modified_date: 1607450357, # Integer | Look up app registration requests by the date the request was updated. This can be used to determine when a request was updated to \"A\" or \"R\".
  page: 1, # Integer | Index of the page of results to return
  page_size: 20 # Integer | Maximum number of results per page
}

begin
  # Get App Registration Status
  result = api_instance.get_app_registration_status(opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->get_app_registration_status: #{e}"
end
```

#### Using the get_app_registration_status_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AppStatuses>, Integer, Hash)> get_app_registration_status_with_http_info(opts)

```ruby
begin
  # Get App Registration Status
  data, status_code, headers = api_instance.get_app_registration_status_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AppStatuses>
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->get_app_registration_status_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pre_app_id** | **String** | The application registration tracking ID | [optional] |
| **application_id** | **String** | The application ID | [optional] |
| **status** | **String** | Look up app registration requests by status | [optional] |
| **app_name** | **String** | Look up app registration requests by app name | [optional] |
| **submitted_date** | **Integer** | Look up app registration requests by the date they were submitted | [optional] |
| **modified_date** | **Integer** | Look up app registration requests by the date the request was updated. This can be used to determine when a request was updated to \&quot;A\&quot; or \&quot;R\&quot;. | [optional] |
| **page** | **Integer** | Index of the page of results to return | [optional][default to 1] |
| **page_size** | **Integer** | Maximum number of results per page | [optional][default to 1] |

### Return type

[**AppStatuses**](AppStatuses.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_applications

> <ApplicationResponse> get_applications(opts)

Get applications details.

This endpoint returns the status of the submitted application and provides additional details.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AppRegistrationApi.new
opts = {
  start: 1, # Integer | Index of the page of results to return
  limit: 20, # Integer | Maximum number of results per page
  pre_app_id: 13, # Integer | The identifier is provided by Mastercard at the first stage of application registration.
  application_id: '00278431-b712-4f30-a044-b611f25e533d', # String | The identifier is generated after the pre-app is approved. Pre-app is the first stage of application registration. Partner first submits an application registration request, then a Pre-app Id is generated for it, and if all the details are correct, the sales team will approve it, and then an application will be registered with the Application Id and associated with the Pre-app. This Application Id is utilized throughout the lifespan of an application.
  name: 'Mvelopes', # String | The application name provided by the partner.
  status: 'P' # String | The application registration status with Mastercard. 'A'=Active , 'P'=Pending , 'D'=Deleted , 'R'=Rejected.
}

begin
  # Get applications details.
  result = api_instance.get_applications(opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->get_applications: #{e}"
end
```

#### Using the get_applications_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApplicationResponse>, Integer, Hash)> get_applications_with_http_info(opts)

```ruby
begin
  # Get applications details.
  data, status_code, headers = api_instance.get_applications_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApplicationResponse>
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->get_applications_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **start** | **Integer** | Index of the page of results to return | [optional][default to 1] |
| **limit** | **Integer** | Maximum number of results per page | [optional][default to 50] |
| **pre_app_id** | **Integer** | The identifier is provided by Mastercard at the first stage of application registration. | [optional] |
| **application_id** | **String** | The identifier is generated after the pre-app is approved. Pre-app is the first stage of application registration. Partner first submits an application registration request, then a Pre-app Id is generated for it, and if all the details are correct, the sales team will approve it, and then an application will be registered with the Application Id and associated with the Pre-app. This Application Id is utilized throughout the lifespan of an application. | [optional] |
| **name** | **String** | The application name provided by the partner. | [optional] |
| **status** | **String** | The application registration status with Mastercard. &#39;A&#39;&#x3D;Active , &#39;P&#39;&#x3D;Pending , &#39;D&#39;&#x3D;Deleted , &#39;R&#39;&#x3D;Rejected. | [optional] |

### Return type

[**ApplicationResponse**](ApplicationResponse.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_registered_institutions

> <InstitutionResponse> get_registered_institutions(application_id, opts)

Get the application registration status with the financial institutions.

The registration status of the approved application against the financial institutions.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AppRegistrationApi.new
application_id = '234dsfdsf-535fdgdtrtr-546464564' # String | The identifier is generated after the pre-app is approved. Pre-app is the first stage of application registration. Partner first submits an application registration request, then a Pre-app Id is generated for it, and if all the details are correct, the sales team will approve it, and then an application will be registered with the Application Id and associated with the Pre-app. This Application Id is utilized throughout the lifespan of an application.
opts = {
  start: 1, # Integer | Index of the page of results to return
  limit: 25, # Integer | Maximum number of results per page
  institution_id: 170716 # Integer | The financial institution id at Mastercard.
}

begin
  # Get the application registration status with the financial institutions.
  result = api_instance.get_registered_institutions(application_id, opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->get_registered_institutions: #{e}"
end
```

#### Using the get_registered_institutions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InstitutionResponse>, Integer, Hash)> get_registered_institutions_with_http_info(application_id, opts)

```ruby
begin
  # Get the application registration status with the financial institutions.
  data, status_code, headers = api_instance.get_registered_institutions_with_http_info(application_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InstitutionResponse>
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->get_registered_institutions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **application_id** | **String** | The identifier is generated after the pre-app is approved. Pre-app is the first stage of application registration. Partner first submits an application registration request, then a Pre-app Id is generated for it, and if all the details are correct, the sales team will approve it, and then an application will be registered with the Application Id and associated with the Pre-app. This Application Id is utilized throughout the lifespan of an application. |  |
| **start** | **Integer** | Index of the page of results to return | [optional][default to 1] |
| **limit** | **Integer** | Maximum number of results per page | [optional][default to 25] |
| **institution_id** | **Integer** | The financial institution id at Mastercard. | [optional] |

### Return type

[**InstitutionResponse**](InstitutionResponse.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## migrate_institution_login_accounts

> <CustomerAccounts> migrate_institution_login_accounts(customer_id, institution_login_id)

Migrate Institution Login Accounts

The `institutionLoginId` parameter uses Finicity's internal FI mapping to move accounts from the current FI legacy connection to the new OAuth FI connection.  This API returns a list of accounts for the given institution login ID.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AppRegistrationApi.new
customer_id = '1005061234' # String | A customer ID
institution_login_id = '1007302745' # String | The institution login ID

begin
  # Migrate Institution Login Accounts
  result = api_instance.migrate_institution_login_accounts(customer_id, institution_login_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->migrate_institution_login_accounts: #{e}"
end
```

#### Using the migrate_institution_login_accounts_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerAccounts>, Integer, Hash)> migrate_institution_login_accounts_with_http_info(customer_id, institution_login_id)

```ruby
begin
  # Migrate Institution Login Accounts
  data, status_code, headers = api_instance.migrate_institution_login_accounts_with_http_info(customer_id, institution_login_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerAccounts>
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->migrate_institution_login_accounts_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **institution_login_id** | **String** | The institution login ID |  |

### Return type

[**CustomerAccounts**](CustomerAccounts.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## modify_app_registration

> <RegisteredApplication> modify_app_registration(pre_app_id, application)

Modify App Registration

Update a registered application.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AppRegistrationApi.new
pre_app_id = '2581' # String | The application registration tracking ID
application = OpenBanking::Application.new({app_description: 'The app that makes your budgeting experience awesome', app_name: 'Awesome Budget App', app_url: 'https://www.finicity.com/', owner_address_line1: '434 W Ascension Way', owner_address_line2: 'Suite #200', owner_city: 'Murray', owner_country: 'USA', owner_name: 'Finicity', owner_postal_code: '84123', owner_state: 'UT', image: 'PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9Im5vIj8+CjxzdmcgICAKICAgeG1sbnM6c3ZnPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIKICAgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIgogICB2ZXJzaW9uPSIxLjEiCiAgIHZpZXdCb3g9IjAgMCAwIDAiCiAgIGhlaWdodD0iMCIKICAgd2lkdGg9IjAiPgogICAgPGcvPgo8L3N2Zz4K'}) # Application | 

begin
  # Modify App Registration
  result = api_instance.modify_app_registration(pre_app_id, application)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->modify_app_registration: #{e}"
end
```

#### Using the modify_app_registration_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RegisteredApplication>, Integer, Hash)> modify_app_registration_with_http_info(pre_app_id, application)

```ruby
begin
  # Modify App Registration
  data, status_code, headers = api_instance.modify_app_registration_with_http_info(pre_app_id, application)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RegisteredApplication>
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->modify_app_registration_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **pre_app_id** | **String** | The application registration tracking ID |  |
| **application** | [**Application**](Application.md) |  |  |

### Return type

[**RegisteredApplication**](RegisteredApplication.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## register_app

> <RegisteredApplication> register_app(application)

Register App

Register a new application to access financial institutions using OAuth connections.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AppRegistrationApi.new
application = OpenBanking::Application.new({app_description: 'The app that makes your budgeting experience awesome', app_name: 'Awesome Budget App', app_url: 'https://www.finicity.com/', owner_address_line1: '434 W Ascension Way', owner_address_line2: 'Suite #200', owner_city: 'Murray', owner_country: 'USA', owner_name: 'Finicity', owner_postal_code: '84123', owner_state: 'UT', image: 'PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9Im5vIj8+CjxzdmcgICAKICAgeG1sbnM6c3ZnPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIKICAgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIgogICB2ZXJzaW9uPSIxLjEiCiAgIHZpZXdCb3g9IjAgMCAwIDAiCiAgIGhlaWdodD0iMCIKICAgd2lkdGg9IjAiPgogICAgPGcvPgo8L3N2Zz4K'}) # Application | 

begin
  # Register App
  result = api_instance.register_app(application)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->register_app: #{e}"
end
```

#### Using the register_app_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RegisteredApplication>, Integer, Hash)> register_app_with_http_info(application)

```ruby
begin
  # Register App
  data, status_code, headers = api_instance.register_app_with_http_info(application)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RegisteredApplication>
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->register_app_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **application** | [**Application**](Application.md) |  |  |

### Return type

[**RegisteredApplication**](RegisteredApplication.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, text/plain


## set_customer_app_id

> set_customer_app_id(customer_id, application_id)

Set Customer App ID

If you have multiple applications for a single client, and you want to register their applications to access financial institutions using OAuth connections, then use this API to assign applications to an existing customer.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::AppRegistrationApi.new
customer_id = '1005061234' # String | A customer ID
application_id = '123456789' # String | The application ID

begin
  # Set Customer App ID
  api_instance.set_customer_app_id(customer_id, application_id)
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->set_customer_app_id: #{e}"
end
```

#### Using the set_customer_app_id_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> set_customer_app_id_with_http_info(customer_id, application_id)

```ruby
begin
  # Set Customer App ID
  data, status_code, headers = api_instance.set_customer_app_id_with_http_info(customer_id, application_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue OpenBanking::ApiError => e
  puts "Error when calling AppRegistrationApi->set_customer_app_id_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** | A customer ID |  |
| **application_id** | **String** | The application ID |  |

### Return type

nil (empty response body)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain

