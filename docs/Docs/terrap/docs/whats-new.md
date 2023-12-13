---
title: What's-New
layout: default
parent: Terrap
grand_parent: Docs
nav_order: 4.5
has_children: false
---
# What's-New

Whats-New was design to show only the new resources / data sources in the following version.
You would use `whats-new` if you want to check whether upgrading to the next version would be beneficial for your use case.

<video width="814" height="535" loop autoplay>
  <source src="images/whats-new.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Flags
### Fixed Providers
* **[-f] fixed-providers** - A comma separated list of fixed providers written in the following format: `<provider>:<version>`.
If this flag is used, all other in-context providers are ignored.
Example:
```shell
terrap scan --fixed-providers hashicorp/aws:3.74.3,hashicorp:google:3.90.1
```

### Filtering Options
* **[-p] provider** - Show only provider block changes.
* **[-d] data-sources** - Display only changed data-sources
* **[-r] resources** - Show only resources changes.

### Print Options
* **[-j] json** - Print the scaned output as json.
```json
{
	"aws_s3_bucket": [
		"A new 'object_lock_enabled' attribute is now available"
	],
	"aws_s3_bucket_accelerate_configuration": [
		"A new resource named aws_s3_bucket_accelerate_configuration is now available"
	],
	"aws_s3_bucket_acl": [
		"A new resource named aws_s3_bucket_acl is now available"
	],
	"aws_s3_bucket_cors_configuration": [
		"A new resource named aws_s3_bucket_cors_configuration is now available"
	],
}
```
* **[-n] no-messages** - Don't print any message other than pure command output.
* **--no-not-supported-message** - Don't print if providers are not supported.