# OpenBanking::InstitutionsApi

All URIs are relative to *https://api.finicity.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_certified_institutions**](InstitutionsApi.md#get_certified_institutions) | **GET** /institution/v2/certifiedInstitutions | Get Certified Institutions |
| [**get_certified_institutions_with_rssd**](InstitutionsApi.md#get_certified_institutions_with_rssd) | **GET** /institution/v2/certifiedInstitutions/rssd | Get Certified Institutions With RSSD |
| [**get_institution**](InstitutionsApi.md#get_institution) | **GET** /institution/v2/institutions/{institutionId} | Get Institution by ID |
| [**get_institution_branding**](InstitutionsApi.md#get_institution_branding) | **GET** /institution/v2/institutions/{institutionId}/branding | Get Institution Branding by ID |
| [**get_institutions**](InstitutionsApi.md#get_institutions) | **GET** /institution/v2/institutions | Get Institutions |


## get_certified_institutions

> <CertifiedInstitutions> get_certified_institutions(opts)

Get Certified Institutions

Search for financial institutions by certified product.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::InstitutionsApi.new
opts = {
  search: 'finbank', # String | Search term (financial institution `name` field). Leave empty for all FIs.
  start: 1, # Integer | Index of the page of results to return
  limit: 1, # Integer | Maximum number of results per page
  type: 'voa', # String | A product type: \"transAgg\", \"ach\", \"stateAgg\", \"voi\", \"voa\", \"aha\", \"availBalance\", \"accountOwner\"
  supported_countries: ['inner_example'] # Array<String> | A list of country codes, '*' for all countries.
}

begin
  # Get Certified Institutions
  result = api_instance.get_certified_institutions(opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling InstitutionsApi->get_certified_institutions: #{e}"
end
```

#### Using the get_certified_institutions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CertifiedInstitutions>, Integer, Hash)> get_certified_institutions_with_http_info(opts)

```ruby
begin
  # Get Certified Institutions
  data, status_code, headers = api_instance.get_certified_institutions_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CertifiedInstitutions>
rescue OpenBanking::ApiError => e
  puts "Error when calling InstitutionsApi->get_certified_institutions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **search** | **String** | Search term (financial institution &#x60;name&#x60; field). Leave empty for all FIs. | [optional] |
| **start** | **Integer** | Index of the page of results to return | [optional][default to 1] |
| **limit** | **Integer** | Maximum number of results per page | [optional][default to 25] |
| **type** | **String** | A product type: \&quot;transAgg\&quot;, \&quot;ach\&quot;, \&quot;stateAgg\&quot;, \&quot;voi\&quot;, \&quot;voa\&quot;, \&quot;aha\&quot;, \&quot;availBalance\&quot;, \&quot;accountOwner\&quot; | [optional] |
| **supported_countries** | [**Array&lt;String&gt;**](String.md) | A list of country codes, &#39;*&#39; for all countries. | [optional] |

### Return type

[**CertifiedInstitutions**](CertifiedInstitutions.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_certified_institutions_with_rssd

> <CertifiedInstitutions> get_certified_institutions_with_rssd(opts)

Get Certified Institutions With RSSD

Search for certified financial institutions w/RSSD.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::InstitutionsApi.new
opts = {
  search: 'finbank', # String | Search term (financial institution `name` field). Leave empty for all FIs.
  start: 1, # Integer | Index of the page of results to return
  limit: 1, # Integer | Maximum number of results per page
  type: 'voa', # String | A product type: \"transAgg\", \"ach\", \"stateAgg\", \"voi\", \"voa\", \"aha\", \"availBalance\", \"accountOwner\"
  supported_countries: ['inner_example'] # Array<String> | A list of country codes, '*' for all countries.
}

begin
  # Get Certified Institutions With RSSD
  result = api_instance.get_certified_institutions_with_rssd(opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling InstitutionsApi->get_certified_institutions_with_rssd: #{e}"
end
```

#### Using the get_certified_institutions_with_rssd_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CertifiedInstitutions>, Integer, Hash)> get_certified_institutions_with_rssd_with_http_info(opts)

```ruby
begin
  # Get Certified Institutions With RSSD
  data, status_code, headers = api_instance.get_certified_institutions_with_rssd_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CertifiedInstitutions>
rescue OpenBanking::ApiError => e
  puts "Error when calling InstitutionsApi->get_certified_institutions_with_rssd_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **search** | **String** | Search term (financial institution &#x60;name&#x60; field). Leave empty for all FIs. | [optional] |
| **start** | **Integer** | Index of the page of results to return | [optional][default to 1] |
| **limit** | **Integer** | Maximum number of results per page | [optional][default to 25] |
| **type** | **String** | A product type: \&quot;transAgg\&quot;, \&quot;ach\&quot;, \&quot;stateAgg\&quot;, \&quot;voi\&quot;, \&quot;voa\&quot;, \&quot;aha\&quot;, \&quot;availBalance\&quot;, \&quot;accountOwner\&quot; | [optional] |
| **supported_countries** | [**Array&lt;String&gt;**](String.md) | A list of country codes, &#39;*&#39; for all countries. | [optional] |

### Return type

[**CertifiedInstitutions**](CertifiedInstitutions.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_institution

> <InstitutionWrapper> get_institution(institution_id)

Get Institution by ID

Get financial institution details by ID.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::InstitutionsApi.new
institution_id = 4222 # Integer | The institution ID

begin
  # Get Institution by ID
  result = api_instance.get_institution(institution_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling InstitutionsApi->get_institution: #{e}"
end
```

#### Using the get_institution_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InstitutionWrapper>, Integer, Hash)> get_institution_with_http_info(institution_id)

```ruby
begin
  # Get Institution by ID
  data, status_code, headers = api_instance.get_institution_with_http_info(institution_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InstitutionWrapper>
rescue OpenBanking::ApiError => e
  puts "Error when calling InstitutionsApi->get_institution_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **institution_id** | **Integer** | The institution ID |  |

### Return type

[**InstitutionWrapper**](InstitutionWrapper.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_institution_branding

> <BrandingWrapper> get_institution_branding(institution_id)

Get Institution Branding by ID

Return the branding information for a financial institution.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::InstitutionsApi.new
institution_id = 4222 # Integer | The institution ID

begin
  # Get Institution Branding by ID
  result = api_instance.get_institution_branding(institution_id)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling InstitutionsApi->get_institution_branding: #{e}"
end
```

#### Using the get_institution_branding_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingWrapper>, Integer, Hash)> get_institution_branding_with_http_info(institution_id)

```ruby
begin
  # Get Institution Branding by ID
  data, status_code, headers = api_instance.get_institution_branding_with_http_info(institution_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingWrapper>
rescue OpenBanking::ApiError => e
  puts "Error when calling InstitutionsApi->get_institution_branding_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **institution_id** | **Integer** | The institution ID |  |

### Return type

[**BrandingWrapper**](BrandingWrapper.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain


## get_institutions

> <Institutions> get_institutions(opts)

Get Institutions

Search for financial institutions.  _Supported regions_: ![🇺🇸](https://flagcdn.com/20x15/us.png)

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

api_instance = OpenBanking::InstitutionsApi.new
opts = {
  search: 'finbank', # String | Search term (financial institution `name` field). Leave empty for all FIs.
  start: 1, # Integer | Index of the page of results to return
  limit: 1, # Integer | Maximum number of results per page
  type: 'voa', # String | A product type: \"transAgg\", \"ach\", \"stateAgg\", \"voi\", \"voa\", \"aha\", \"availBalance\", \"accountOwner\"
  supported_countries: ['inner_example'] # Array<String> | A list of country codes, '*' for all countries.
}

begin
  # Get Institutions
  result = api_instance.get_institutions(opts)
  p result
rescue OpenBanking::ApiError => e
  puts "Error when calling InstitutionsApi->get_institutions: #{e}"
end
```

#### Using the get_institutions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Institutions>, Integer, Hash)> get_institutions_with_http_info(opts)

```ruby
begin
  # Get Institutions
  data, status_code, headers = api_instance.get_institutions_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Institutions>
rescue OpenBanking::ApiError => e
  puts "Error when calling InstitutionsApi->get_institutions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **search** | **String** | Search term (financial institution &#x60;name&#x60; field). Leave empty for all FIs. | [optional] |
| **start** | **Integer** | Index of the page of results to return | [optional][default to 1] |
| **limit** | **Integer** | Maximum number of results per page | [optional][default to 25] |
| **type** | **String** | A product type: \&quot;transAgg\&quot;, \&quot;ach\&quot;, \&quot;stateAgg\&quot;, \&quot;voi\&quot;, \&quot;voa\&quot;, \&quot;aha\&quot;, \&quot;availBalance\&quot;, \&quot;accountOwner\&quot; | [optional] |
| **supported_countries** | [**Array&lt;String&gt;**](String.md) | A list of country codes, &#39;*&#39; for all countries. | [optional] |

### Return type

[**Institutions**](Institutions.md)

### Authorization

[FinicityAppToken](../README.md#FinicityAppToken), [FinicityAppKey](../README.md#FinicityAppKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/plain

