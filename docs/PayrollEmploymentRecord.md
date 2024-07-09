# OpenBanking::PayrollEmploymentRecord

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **employer_name** | **String** | Name of the employer as stated by the employer in the payroll system |  |
| **legal_entity_id** | **String** | Employer identification number (EIN) | [optional] |
| **original_hire_date** | **Integer** | The original hired date of an employee at the company | [optional] |
| **latest_hire_date** | **Integer** | If an employee leaves the company and returns later, then the employer states the latest hire date at the company | [optional] |
| **latest_pay_period_end_date** | **Integer** | The most recent pay period’s end date. | [optional] |
| **latest_pay_date** | **Integer** | The most recent pay date from an employer | [optional] |
| **days_since_last_pay** | **Integer** | The number of days since an employee was last paid | [optional] |
| **number_pay_cadence_without_pay** | **Integer** | The number of pay cadences an employee has not been paid; determined by the pay frequency | [optional] |
| **employment_end_date** | **Integer** | The date an employee ended their employment at the company | [optional] |
| **employment_duration** | **String** | The length of time an employee has been employed with that employer in ISO 8601 format (e.g. P1Y6M0D) | [optional] |
| **employer_address** | [**Array&lt;PayrollEmployerAddress&gt;**](PayrollEmployerAddress.md) | Array of addresses | [optional] |
| **employment_status_code** | **String** | &#39;Status codes: &#x60;A&#x60; - Active, &#x60;NLE&#x60; - No Longer Employed, &#x60;L&#x60; - Leave, &#x60;O&#x60; - Other&#39;, &#x60;I&#x60; - Inactive, &#x60;U&#x60; - Unknown&#39; |  |
| **employment_status_name** | **String** | &#39;Status name: &#x60;Active&#x60;, &#x60;No Longer Employed&#x60;, &#x60;Leave&#x60; or &#x60;Other&#x60;, &#x60;Inactive&#x60;, or &#x60;Unknown&#x60;&#39; |  |
| **derived_employment_status** | **Boolean** | Describes the employment status - it will be true if it is not directly stated by the employer, and false otherwise | [optional] |
| **work_level_code** | **String** | The abbreviate code for the employment level names (workLevelName) that we receive from the employer | [optional] |
| **work_level_name** | **String** | The employment level name is whatever we receive from the employer, such as full time, part time, temp, contractor, and more | [optional] |
| **work_level_status** | **String** | The categorized work level status. Enumerations are:  * &#x60;Temporary&#x60;  * &#x60;Seasonal&#x60;  * &#x60;Retired&#x60;  * &#x60;Student&#x60;  * &#x60;Full Time&#x60;  * &#x60;Part Time&#x60;  * &#x60;Unspecified&#x60;  This is a new field, currently enabled only for testing reports. It will be added for all reports in August 2021.  |  |
| **position_title** | **String** | Employee job title | [optional] |
| **position_duration** | **String** | The length of time an employee has been employed at their current or latest position for this employment in ISO 8601 format (eg P1Y6M0D) | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::PayrollEmploymentRecord.new(
  employer_name: ACME INC,
  legal_entity_id: 752760000,
  original_hire_date: 1527832800,
  latest_hire_date: 1527832800,
  latest_pay_period_end_date: 1596175201,
  latest_pay_date: 1596175200,
  days_since_last_pay: 10,
  number_pay_cadence_without_pay: 1,
  employment_end_date: 1527832800,
  employment_duration: P1Y6M0D,
  employer_address: null,
  employment_status_code: A,
  employment_status_name: Active,
  derived_employment_status: true,
  work_level_code: FT,
  work_level_name: Full Time-Regular,
  work_level_status: Full Time,
  position_title: Shift Supervisor,
  position_duration: P1Y6M0D
)
```

