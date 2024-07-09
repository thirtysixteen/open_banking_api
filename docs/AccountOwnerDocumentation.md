# OpenBanking::AccountOwnerDocumentation

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tax_id** | **String** | Country specific tax ID associated with the customer. * **United Stated**: Social Security number (SSN) or Taxpayer Identification Number (TIN)    * Format: 123-45-7890  * **Canada**: Social Insurance Number (SIM) or Numero d&#39;assurance sociale (NAS)    * Format: 123-456-789 | [optional] |
| **tax_id_country** | **String** | Country code is Iso3166-1 Alpha-2 code and Alpha 3 standard (max length 3). | [optional] |
| **government_id** | **String** | A federal or state issued identification number in alphanumeric characters. * **United States**:    * Passport: 6-9 digits.    * US Visa: 8 digits.    * Driver&#39;s license: 1-19 digits * **Canada**:    * Passport: 8 digits    * Driver: 6-9 digits | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::AccountOwnerDocumentation.new(
  tax_id: 123-45-7890,
  tax_id_country: USA,
  government_id: 123456789
)
```

