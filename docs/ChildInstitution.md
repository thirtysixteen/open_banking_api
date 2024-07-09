# OpenBanking::ChildInstitution

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rssd** | **Integer** | The RSSD ID is a unique identifier assigned to financial institutions by the Federal Reserve. While the length of the RSSD ID varies by institution, it cannot exceed 10 numerical digits. |  |
| **parent_rssd** | **Integer** | The RSSD ID is a unique identifier assigned to financial institutions by the Federal Reserve. While the length of the RSSD ID varies by institution, it cannot exceed 10 numerical digits. |  |
| **name** | **String** | The name of the institution |  |
| **institution_id** | **Integer** | The ID of a financial institution, represented as a number |  |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ChildInstitution.new(
  rssd: 490535,
  parent_rssd: 490535,
  name: FinBank,
  institution_id: 4222
)
```

