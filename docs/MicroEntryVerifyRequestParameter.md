# OpenBanking::MicroEntryVerifyRequestParameter

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **partner_id** | **String** | Your Partner ID displayed in the [Developer Dashboard](https://developer.mastercard.com/account/log-in) | [optional] |
| **customer_id** | **String** | A customer ID. See Add Customer API for how to create a customer ID. | [optional] |
| **redirect_uri** | **String** | The URL that customers will be redirected to after completing Finicity Connect. Required unless Connect is embedded inside our application (iframe). | [optional] |
| **webhook** | **String** | The publicly available URL you want to be notified with events as the user progresses through the application. See [Connect Webhook Event](https://developer.mastercard.com/open-banking-us/documentation/webhooks/webhooks-connect/) for event details. | [optional] |
| **webhook_content_type** | **String** | The content type the webhook events will be sent in. Supported types: \&quot;application/json\&quot; and \&quot;application/xml\&quot;. | [optional][default to &#39;application/json&#39;] |
| **webhook_data** | **Object** | Allows additional identifiable information to be inserted into the payload of connect webhook events. See: [Custom Webhooks](https://developer.mastercard.com/open-banking-us/documentation/webhooks/webhooks-custom/). | [optional] |
| **webhook_headers** | **Object** | Allows additional identifiable information to be included as headers of connect webhook event. See: [Custom Webhooks](https://developer.mastercard.com/open-banking-us/documentation/webhooks/webhooks-custom/). | [optional] |
| **experience** | **String** | The &#x60;experience&#x60; field allows you to customize: * Brand: color and logo * Icon: displayed on the \&quot;Share your data\&quot; page * Popular institutions: displayed on the Bank Search page * Report: the credit decisioning report to send when Connect completes. * MVS modules: financial, payroll, paystub  Note: the Finicity sales engineers (SE) help you set up a default experience for your company. For each additional experience you create thereafter, they&#39;ll give you a unique ID. See [Configure the Connect Experience](https://developer.mastercard.com/open-banking-us/documentation/connect/configure-connect-experience/).  Experience values options: * \&quot;default\&quot;: your default experience (must be defined) * GUID: the code for a different experience * Not defined: If you don&#39;t pass the experience parameter, then Connect&#39;s out of the box default experience (add accounts but no branding) is used, and the MVS modules will not run. | [optional] |
| **account_id** | **String** | An account ID | [optional] |

## Example

```ruby
require 'open_banking'

instance = OpenBanking::MicroEntryVerifyRequestParameter.new(
  partner_id: 1234583871234,
  customer_id: 1005061234,
  redirect_uri: https://www.finicity.com/connect/,
  webhook: https://webhook.site/8d4421a7-d1d1-4f01-bb08-5370aff0321b,
  webhook_content_type: application/json,
  webhook_data: null,
  webhook_headers: null,
  experience: default,
  account_id: 5011648377
)
```

