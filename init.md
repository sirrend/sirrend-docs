# Init 👋 

Init is used to initialize a Terrap workspace in a given directory.</br>
On execution, init runs `terraform init` under the hood and initializes the given context (directory)</br>

?> **Important!** Terrap decides which Terraform version to use **in the following order**:
</br>1. The latest installed Terraform version found locally.
</br>2. If the `TERRAP_TERRAFORM_VERSION` environment variable is set, Terrap will use the version specified as long as it matches the `>=0.13` constraint.
</br>3. If none of the above is applicable, Terrap will download the latest available version.

Init is necessary when you have a predefined set of providers and want to track changes made in subsequent versions.</br>
It is prefered to use `init` in most cases, to make the use of other commands easier.

## Flags
* **--directory [-d]** - Initialize a specific directory, otherwise the directory in context will be initialized.
* **--upgrade [-u]** - Upgrade the Terrap workspace in context (Can be used with -d).


https://user-images.githubusercontent.com/47568615/233799732-40ca73db-6df7-47b7-b0a5-f87c57a7ed7d.mov

