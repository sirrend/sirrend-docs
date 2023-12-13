---
title: Terrap QuickStart
layout: default
parent: Terrap
grand_parent: Docs
nav_order: 4.1
has_children: false
---
# Quick Start

## Download
### Clone sirrend/terrap-cli
```shell
git clone https://github.com/sirrend/terrap-cli
cd terrap-cli

go build -o terrap .

chmod +x terrap
mv terrap /usr/local/bin/
```

### Brew
```shell
brew install terrap-cli
```

Validate terrap is working by executing `terrap`.

## Initialize my First Workspace
1. Navigate to the local Terraform folder you want to work with.
`cd terraform/folder/path`

2. Initialize a new Terrap workspace where you would run `terraform apply` with `terrap init` -> <a href="https://sirrend.github.io/terrap-docs/init">init</a>.

{: .important }    
>As Terrap runs `terraform init` under the hood, it would need every configuration component you normally use when executing `terraform init`.
>
>It can be an ENV_VAR, the `.aws/credentials` file, etc.


3. Scan your workspace with: `terrap scan`