---
title: Init
layout: default
parent: Terrap
grand_parent: Docs
nav_order: 4.2
has_children: false
---
# Init 👋 

Init is used to initialize a Terrap workspace in a given directory.
On execution, init runs `terraform init` under the hood and initializes the given context (directory)

{: .important }
>Terrap decides which Terraform version to use **in the following order**:
>1. The latest installed Terraform version found locally.
>2. If the `TERRAP_TERRAFORM_VERSION` environment variable is set, Terrap will use the version specified as long as it matches the `>=0.13` constraint.
>3. If none of the above is applicable, Terrap will download the latest available version.

Init is necessary when you have a predefined set of providers and want to track changes made in subsequent versions.
It is prefered to use `init` in most cases, to make the use of other commands easier.

<video width="615" height="290" loop autoplay>
  <source src="images/init.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Flags
* **[-d] directory** - Initialize a specific directory, otherwise the directory in context will be initialized.
* **[-u] upgrade** - Upgrade the Terrap workspace in context (Can be used with -d).

## Environment Variables
**TERRAP_TERRAFORM_VERSION** - To specify the version of Terraform that Terrap should use, set this environment variable with the constraint: `>=0.13`.