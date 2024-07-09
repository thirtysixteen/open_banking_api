# Building

From the [Quick Start Guide](https://developer.mastercard.com/open-banking-us/documentation/quick-start-guide/#5-generate-an-api-client-library).

I've added the `openbanking-us.yaml` file to the repository. The file was downloaded from the Mastercard Developer website. Periodically, we will need to check for updates to this file and regenerate the client library.

## OpenAPI Generator

Install the OpenAPI Generator CLI:

```sh
npm install @openapitools/openapi-generator-cli -g
```

Generate the Ruby client:

```sh
rm -rf docs lib spec
openapi-generator-cli generate -g ruby -i openbanking-us.yaml -c openapi_config.yaml
```
