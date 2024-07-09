# OpenBanking::ObbDataAvailability

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **historic_availability_begin_date** | **String** | Begin date for data availability | [optional] |
| **historic_availability_end_date** | **String** | End date for data availability | [optional] |
| **historic_available_days** | **Integer** | Days for which transaction details are available |  |
| **historic_data_availability** | **String** | Description of historic data availability |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ObbDataAvailability.new(
  historic_availability_begin_date: 2022-03-01,
  historic_availability_end_date: 2022-03-30,
  historic_available_days: 30,
  historic_data_availability: Data is available from 2022-03-01 to 2022-03-30
)
```

