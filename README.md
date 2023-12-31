# Terraform-gcp-Service-account
# Terraform Google Cloud Service Account Module

## Table of Contents

- [Introduction](#introduction)
- [Usage](#usage)
- [Module Inputs](#module-inputs)
- [Module Outputs](#module-outputs)
- [License](#license)
## Introduction

This Terraform module creates a Google Cloud Service Account with configurable options. It is designed to be used in conjunction with other infrastructure modules.

## Usage
To use this module, you should have Terraform installed and configured for GCP. This module provides the necessary Terraform configuration for creating GCP resources, and you can customize the inputs as needed. Below is an example of how to use this module:
## Example: _service-account_
```hcl
module "service-account" {
  source                             = "git::https://github.com/cypik/terraform-gcp-Service-account.git?ref=v1.0.0"
  name                               = "app"
  environment                        = "test"
  key_algorithm                      = "KEY_ALG_RSA_2048"
  public_key_type                    = "TYPE_X509_PEM_FILE"
  private_key_type                   = "TYPE_GOOGLE_CREDENTIALS_FILE"
  members                            = []
}
```
This example demonstrates how to create various GCP resources using the provided modules. Adjust the input values to suit your specific requirements.

## Module Inputs
- `name`: The name of the service account.
- `environment`: The environment for the service account.
- `project_id`: The Google Cloud project ID.
- `service_account_key_enabled`: Enable Google service account key creation.
- `key_algorithm`: The algorithm used for the key.
- `public_key_type`: The type of public key file to generate.
- `private_key_type`: The type of private key file to generate.
- `members`: List of members to grant access to the service account.

## Module Outputs
- `account_email`: The email address of the created service account.
- `service_account_key`: The key for the created service account.
- `id` : The iam  id of the service account.
- `account_id` : An identifier for the resource with format.
- `account_name` : The fully-qualified name of the service account.
- `account_unique_id` : The unique id of the service account.
- `key_id` : An identifier for the  key_id resource with format.
- `key_name` : The name used for this key pair.
- `public_key` : The public key, base64 encoded.
- `private_key` : The private key in JSON format, base64 encoded.
- `valid_after` : The key can be used after this timestamp.
- `valid_before` : The key can be used before this timestamp.
- `etag` : The etag of the service account IAM policy.

## Examples
For detailed examples on how to use this module, please refer to the [Examples](https://github.com/cypik/terraform-gcp-Service-account/tree/master/example) directory within this repository.

## Author
Your Name
Replace **'[License Name]'** and **'[Your Name]'** with the appropriate license and your information. Feel free to expand this README with additional details or usage instructions as needed for your specific use case.
## License
This Terraform module is provided under the **'[License Name]'** License. Please see the [LICENSE](https://github.com/cypik/terraform-gcp-Service-account/blob/master/LICENSE) file for more details.
