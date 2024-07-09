# OpenBanking::Consumer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A consumer ID. See Create Consumer API for how to create a consumer ID. |  |
| **first_name** | **String** | The first name of the account holder |  |
| **last_name** | **String** | The last name of the account holder |  |
| **customer_id** | **Integer** | A customer ID represented as a number. See Add Customer API for how to create a customer ID. |  |
| **address** | **String** | A street address |  |
| **city** | **String** | City |  |
| **state** | **String** | State |  |
| **zip** | **String** | A ZIP code |  |
| **phone** | **String** | A phone number (max length 15). |  |
| **ssn** | **String** | Last 4 digits of a SSN |  |
| **birthday** | [**Birthday**](Birthday.md) |  |  |
| **email** | **String** | An email address |  |
| **created_date** | **Integer** | A date in Unix epoch time (in seconds). See: [Handling Epoch Dates and Times](https://developer.mastercard.com/open-banking-us/documentation/codes-and-formats/). |  |
| **suffix** | **String** | A generational or academic suffix | [optional] |
| **end_user** | [**ConsumerEndUser**](ConsumerEndUser.md) |  | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Consumer.new(
  id: 0bf46322c167b562e6cbed9d40e19a4c,
  first_name: John,
  last_name: Smith,
  customer_id: 1005061234,
  address: 434 W Ascension Way Suite #200 Murray UT 84123,
  city: Murray,
  state: UT,
  zip: 84123,
  phone: 1-801-984-4200,
  ssn: 9999,
  birthday: null,
  email: myname@mycompany.com,
  created_date: 1607450357,
  suffix: PhD,
  end_user: null
)
```

