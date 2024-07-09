# OpenBanking::CertifiedInstitution

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | The ID of a financial institution, represented as a number |  |
| **rssd** | **Integer** | The RSSD ID is a unique identifier assigned to financial institutions by the Federal Reserve. While the length of the RSSD ID varies by institution, it cannot exceed 10 numerical digits. | [optional] |
| **name** | **String** | The name of the institution |  |
| **trans_agg** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Transaction Aggregation product \&quot;false\&quot;: The institution is decertified for the Transaction Aggregation product |  |
| **ach** | **Boolean** | \&quot;true\&quot;: The institution is certified for the ACH product \&quot;false\&quot;: The institution is decertified for the ACH product |  |
| **state_agg** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Statement Aggregation product \&quot;false\&quot;: The institution is decertified for the Statement Aggregation product |  |
| **voi** | **Boolean** | \&quot;true\&quot;: The institution is certified for the VOI product \&quot;false\&quot;: The institution is decertified for the VOI product |  |
| **voa** | **Boolean** | \&quot;true\&quot;: The institution is certified for the VOA product \&quot;false\&quot;: The institution is decertified for the VOA product |  |
| **aha** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Account History Aggregation product \&quot;false\&quot;: The institution is decertified for the Account History Aggregation product |  |
| **avail_balance** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Account Balance Check (ABC) product \&quot;false\&quot;: The institution is decertified for the Account Balance Check (ABC) product |  |
| **account_owner** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Account Owner product \&quot;false\&quot;: The institution is decertified for the Account Owner product |  |
| **student_loan_data** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Student Loan Data product  \&quot;false\&quot;: The institution is decertified for the Student Loan Data product |  |
| **loan_payment_details** | **Boolean** | \&quot;true\&quot;: The institution is certified for the Loan Payment Detail product  \&quot;false\&quot;: The institution is decertified for the Loan Payment Detail product |  |
| **child_institutions** | [**Array&lt;ChildInstitution&gt;**](ChildInstitution.md) | An array of child financial institutions | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::CertifiedInstitution.new(
  id: 4222,
  rssd: 490535,
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
  child_institutions: null
)
```

