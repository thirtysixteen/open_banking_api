# OpenBanking::Institution

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The ID of a financial institution, represented as a number |  |
| **name** | **String** | The name of the institution | [optional] |
| **trans_agg** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Transaction Aggregation product \&quot;false\&quot;: The institution is decertified for the Transaction Aggregation product |  |
| **ach** | **Boolean** | \&quot;true\&quot;: The institution is certified for the ACH product \&quot;false\&quot;: The institution is decertified for the ACH product |  |
| **state_agg** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Statement Aggregation product \&quot;false\&quot;: The institution is decertified for the Statement Aggregation product |  |
| **voi** | **Boolean** | \&quot;true\&quot;: The institution is certified for the VOI product \&quot;false\&quot;: The institution is decertified for the VOI product |  |
| **voa** | **Boolean** | \&quot;true\&quot;: The institution is certified for the VOA product \&quot;false\&quot;: The institution is decertified for the VOA product |  |
| **aha** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Account History Aggregation product \&quot;false\&quot;: The institution is decertified for the Account History Aggregation product |  |
| **avail_balance** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Account Balance Check (ABC) product \&quot;false\&quot;: The institution is decertified for the Account Balance Check (ABC) product |  |
| **account_owner** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Account Owner product \&quot;false\&quot;: The institution is decertified for the Account Owner product |  |
| **student_loan_data** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Student Loan Data product  \&quot;false\&quot;: The institution is decertified for the Student Loan Data product | [optional] |
| **loan_payment_details** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Loan Payment Detail product  \&quot;false\&quot;: The institution is decertified for the Loan Payment Detail product | [optional] |
| **account_type_description** | **String** | Values: Banking, Investments, Credit Cards/Accounts, Workplace Retirement, Mortgages and Loans, Insurance | [optional] |
| **phone** | **String** | A phone number (max length 15). | [optional] |
| **url_home_app** | **String** | The URL of the institution&#39;s primary home page | [optional] |
| **url_logon_app** | **String** | The URL of the institution&#39;s login page | [optional] |
| **oauth_enabled** | **Boolean** | \&quot;true\&quot;: The institution is an OAuth connection  \&quot;false\&quot;: The institution isn&#39;t an OAuth connection |  |
| **url_forgot_password** | **String** | Institution&#39;s forgot password page | [optional] |
| **url_online_registration** | **String** | Institution&#39;s signup page | [optional] |
| **_class** | **String** | Institution&#39;s class | [optional] |
| **special_text** | **String** | Special instructions given to customers for login | [optional] |
| **time_zone** | **String** | The time zone of the institution. | [optional] |
| **special_instructions** | **Array&lt;String&gt;** | Instructions given to the customer before they are sent to the institution website to login for OAuth institutions.  Note: this helps the customer to provide the proper permission for data needed for the application. | [optional] |
| **special_instutions_title** | **String** | The title of the special instructions, if one exists or is required. | [optional] |
| **address** | [**InstitutionAddress**](InstitutionAddress.md) |  | [optional] |
| **currency** | **String** | A currency code |  |
| **email** | **String** | An email address | [optional] |
| **status** | **String** | Status for the institution: \&quot;online\&quot;, \&quot;offline\&quot;, \&quot;maintenance\&quot;, \&quot;testing\&quot; |  |
| **new_institution_id** | **Integer** | The ID of a financial institution, represented as a number | [optional] |
| **branding** | [**Branding**](Branding.md) |  | [optional] |
| **oauth_institution_id** | **Integer** | The ID of a financial institution, represented as a number | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::Institution.new(
  id: 4222,
  name: FinBank,
  trans_agg: true,
  ach: true,
  state_agg: false,
  voi: true,
  voa: true,
  aha: false,
  avail_balance: false,
  account_owner: true,
  student_loan_data: true,
  loan_payment_details: true,
  account_type_description: Workplace Retirement,
  phone: 1-801-984-4200,
  url_home_app: https://www.example.com/home,
  url_logon_app: https://www.example.com/login,
  oauth_enabled: true,
  url_forgot_password: https://www.example.com/forgotPassword.do,
  url_online_registration: https://www.example.com/signup,
  _class: retirement,
  special_text: Please enter your Principal Financial - Retirement (Personal) Username and Password.,
  time_zone: America/Denver,
  special_instructions: [&quot;Account details&quot;,&quot;Balances and transactions&quot;,&quot;Personal and account ownership info&quot;],
  special_instutions_title: Special OAuth Login Instructions,
  address: null,
  currency: USD,
  email: myname@mycompany.com,
  status: online,
  new_institution_id: 4222,
  branding: null,
  oauth_institution_id: 4222
)
```

