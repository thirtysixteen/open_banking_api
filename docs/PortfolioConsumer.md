# OpenBanking::PortfolioConsumer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A consumer ID. See Create Consumer API for how to create a consumer ID. |  |
| **first_name** | **String** | The first name of the account holder |  |
| **last_name** | **String** | The last name of the account holder |  |
| **customer_id** | **Integer** | A customer ID represented as a number. See Add Customer API for how to create a customer ID. |  |
| **ssn** | **String** | A full SSN with or without hyphens |  |
| **birthday** | [**Birthday**](Birthday.md) |  |  |
| **suffix** | **String** | A generational or academic suffix | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PortfolioConsumer.new(
  id: 0bf46322c167b562e6cbed9d40e19a4c,
  first_name: John,
  last_name: Smith,
  customer_id: 1005061234,
  ssn: 999-99-9999,
  birthday: null,
  suffix: PhD
)
```

