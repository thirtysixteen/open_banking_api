# OpenBanking::BalanceAnalyticsMetrics

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **available_balance** | **Float** | Available Balance | [optional] |
| **available_balance_date** | **String** | Available Balance date | [optional] |
| **average_daily_balance_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Average daily ending balance each month over the report time period | [optional] |
| **average_daily_balance_for_the_report_time_period** | **Float** | Average Daily Balance | [optional] |
| **average_weekday_balance_for_the_report_time_period** | **Float** | Average Weekday Balance | [optional] |
| **count_daily_negative_balances_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndCount&gt;**](ObbDateRangeAndCount.md) | Number of negative daily ending balances each month over the report time period | [optional] |
| **current_running_balance** | **Float** | Current Running Balance Date | [optional] |
| **current_running_balance_date** | **String** | Current Running Balance date | [optional] |
| **daily_balances_by_weekday_for_the_report_time_period** | [**Array&lt;ObbDailyBalance&gt;**](ObbDailyBalance.md) | Daily balance of the account during weekdays over the length of the report | [optional] |
| **daily_balances_for_the_report_time_period** | [**Array&lt;ObbDailyBalance&gt;**](ObbDailyBalance.md) | Daily balance of the account over the length of the report | [optional] |
| **historic_number_of_weeks_average_balance_increasing** | [**ObbNumWeeksAverageBalanceIncreasing**](ObbNumWeeksAverageBalanceIncreasing.md) |  | [optional] |
| **maximum_daily_balance_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Maximum daily ending balance each month over the report time period | [optional] |
| **maximum_running_balance_for_the_report_time_period** | **Float** | Maximum Running Balance | [optional] |
| **minimum_daily_balance_by_month_for_the_report_time_period** | [**Array&lt;ObbDateRangeAndAmount&gt;**](ObbDateRangeAndAmount.md) | Minimum daily ending balance each month over the report time period | [optional] |
| **minimum_running_balance_for_the_report_time_period** | **Float** | Minimum Running Balance | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::BalanceAnalyticsMetrics.new(
  available_balance: 1000.01,
  available_balance_date: 2022-02-18T02:34:00-07:00,
  average_daily_balance_by_month_for_the_report_time_period: null,
  average_daily_balance_for_the_report_time_period: -10442.53,
  average_weekday_balance_for_the_report_time_period: -10442.53,
  count_daily_negative_balances_by_month_for_the_report_time_period: null,
  current_running_balance: 1000.01,
  current_running_balance_date: 2022-02-10T05:00:00-07:00,
  daily_balances_by_weekday_for_the_report_time_period: [{&quot;date&quot;:&quot;2022-03-23&quot;,&quot;dayOfWeek&quot;:&quot;Monday&quot;,&quot;endingBalance&quot;:21527.3}],
  daily_balances_for_the_report_time_period: [{&quot;date&quot;:&quot;2022-03-22&quot;,&quot;dayOfWeek&quot;:&quot;Sunday&quot;,&quot;endingBalance&quot;:21527.3}],
  historic_number_of_weeks_average_balance_increasing: null,
  maximum_daily_balance_by_month_for_the_report_time_period: null,
  maximum_running_balance_for_the_report_time_period: -28749.44,
  minimum_daily_balance_by_month_for_the_report_time_period: null,
  minimum_running_balance_for_the_report_time_period: -28749.44
)
```

