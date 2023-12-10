# Sirrend-Docs 
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)  ![GitHub go.mod Go version (subdirectory of monorepo)](https://img.shields.io/github/go-mod/go-version/sirrend/terrap-cli?filename=go.mod)

?> **Important** Terrap is currently in it's alpha stage and in continious development.

?> **Important** Terrap currently supports upgrades to the following version only


Terrap is a CLI utility created by <a href=https://sirrend.com style="color: #3366CC">Sirrend</a> which keeps you up-to-date with the latest provider changes.

## About
By design, Terrap executes `terraform init` under the hood in order to initialize the Terrap workspace.</br>
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

## How to Download
#### Clone sirrend/terrap-cli
```shell
git clone https://github.com/sirrend/terrap-cli
cd terrap-cli

go build -o terrap .

chmod +x terrap
mv terrap /usr/local/bin/
```

#### Brew
```shell
brew install terrap-cli
```

## Constraints
1. Supported Terraform Core versions: `>=0.13`.
2. Every provider which uses `Terraform Core 0.13` or higher.