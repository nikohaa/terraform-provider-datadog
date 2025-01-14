---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "datadog_integration_aws_log_collection Resource - terraform-provider-datadog"
subcategory: ""
description: |-
  Provides a Datadog - Amazon Web Services integration log collection resource. This can be used to manage which AWS services logs are collected from for an account.
---

# datadog_integration_aws_log_collection (Resource)

Provides a Datadog - Amazon Web Services integration log collection resource. This can be used to manage which AWS services logs are collected from for an account.

## Example Usage

```terraform
# Create a new Datadog - Amazon Web Services integration log collection
resource "datadog_integration_aws_log_collection" "main" {
  account_id = "1234567890"
  services   = ["lambda"]
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **account_id** (String) Your AWS Account ID without dashes. If your account is a GovCloud or China account, specify the `access_key_id` here.
- **services** (List of String) A list of services to collect logs from. See the [api docs](https://docs.datadoghq.com/api/v1/aws-logs-integration/#get-list-of-aws-log-ready-services) for more details on which services are supported.

### Read-Only

- **id** (String) The ID of this resource.

## Import

Import is supported using the following syntax:

```shell
# Amazon Web Services log collection integrations can be imported using the `account ID`.
terraform import datadog_integration_aws_log_collection.test 1234567890
```
