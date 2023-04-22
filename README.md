# Terrap
Terrap is a Terraform wrapper which keeps you up-to-date with the latest provider changes.

?> **Important** Terrap is currently in it's alpha stage and in continious development.

### Terrap Use Cases
* Find code (schema) deprecations.
* Find resources / data sources removals.
* Watch attributes deffinition modifications (required, optional, type etc.)
* And more..

## About Terrap
By design, Terrap executes `Terraform init` under the hood in order to initialize the Terrap workspace.
As a direct result of the above, all the components required to initialize the Terraofrm workspace are required by Terrap as well.

For example, if you're using the `AWS_PROFILE` environment variable to configure the **AWS provider**, you need to set it for Terrap as well.

```terraform
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "3.74.3"
    }
  }
}
```

```shell
export AWS_PROFILE="aws_profile"
```