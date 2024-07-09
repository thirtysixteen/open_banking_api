# OpenBanking::PortfolioWithConsumerSummary

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **portfolio_id** | **String** | A unique identifier that will be consistent across all reports created for the same customer |  |
| **reports** | [**Array&lt;PortfolioReport&gt;**](PortfolioReport.md) | A list of reports in the portfolio |  |
| **consumer** | [**PortfolioConsumer**](PortfolioConsumer.md) |  |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PortfolioWithConsumerSummary.new(
  portfolio_id: y4zsgccj4xpw-6-port,
  reports: null,
  consumer: null
)
```

