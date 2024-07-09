# OpenBanking::ThirdPartyAccessProof

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **signature** | **String** | The digital signature for the \&quot;receipt\&quot; portion of the access key | [optional] |
| **key_id** | **String** | The Finicity key identifier is used to sign the access key | [optional] |
| **timestamp** | **Time** | A date-time with time zone | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::ThirdPartyAccessProof.new(
  signature: JTdCyTIyY3VzdG9tZXJJZCUyMiUzQSUyMjU0NTQ1MTQwMDI5NTU2MjkzNDMlMjIlMkMlMjJwYXJ0bmVySWQlMjIlM0ElMjIyNDQ1NTgzOTIyNTM2JTIyJTJDJTIycHJvZHVjdHMlMjIlM0ElNUIlN0IlMjJhY2Nlc3NQZXJpb2QlMjIlM0ElN0IlMjJlbmRUaW1lJTIyJTNBJTIyMjAyMy0xMS0yOVQwNiUzQTA2JTNBMjBaJTIyJTJDJTIyc3RhcnRUaW1lJTIyJTNBJTIyMjAyMi0xMS0yOVQwNiUzQTA2JTNBMjBaJTIyJTJDJTIydHlwZSUyMiUzQSUyMnRpbWVmcmFtZSUyMiU3RCUyQyUyMmFjY291bnRJZCUyMiUzQSUyMjQ2MzM0MTU3NDM5NjAzNzQwMjQlMjIlMkMlMjJwcm9kdWN0JTIyJTNBJTIybW9uZXlUcmFuc2ZlckRldGFpbHMlMjIlN0QlMkMlN0IlMjJhY2Nlc3NQZXJpb2QlMjIlM0ElN0IlMjJlbmRUaW1lJTIyJTNBJTIyMjAyMy0xMC0yOVQwNiUzQTA2JTNBMjBaJTIyJTJDJTIyc3RhcnRUaW1lJTIyJTNBJTIyMjAyMi0xMS0yOVQwNiUzQTA2JTNBMjBaJTIyJTJDJTIydHlwZSUyMiUzQSUyMnRpbWVmcmFtZSUyMiU3RCUyQyUyMmFjY291bnRJZCUyMiUzQSUyMjQ2MzM0MTU3NDM5NjAzNzQwMjQlMjIlMkMlMjJwcm9kdWN0JTIyJTNBJTIybW9uZXlUcmFuc2ZlckRldGFpbHMlMjIlN0QlNUQlMkMlMjJwcm9maWxlJTIyJTNBMyUyQyUyMnByb3ZlbmFuY2UlMjIlM0FudWxsJTJDJTIycmVjZWlwdElkJTIyJTNBJTIyY3JfNHBmSTNyMVg4YU9IckREd3J3QzAxTkhDeE9YbFcxJTIyJTJDJTIycmVjZWlwdFZlcnNpb24lMjIlM0ExJTJDJTIydGltZXN0YW1wJTIyJTNBJTIyMjAyMi0xMS0yOVQxOCUzQTM1JTNBMDhaJTIyJTJDJTIydmVyc2lvbiUyMiUzQSUyMjElRjYlN9U&#x3D;,
  key_id: 867-530-900,
  timestamp: 2022-03-10T06:06:20.042584549Z
)
```

