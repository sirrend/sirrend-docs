---
title: Open Issue
layout: default
parent: Terrap
grand_parent: Docs
nav_order: 4.7
has_children: false
---
# Open-Issue
To report any issues or suggest new features, you can use this command to easily open a feature-request or a bug directly in the `sirrend/terrap-cli` GitHub repository.

Example: `terrap open-issue -t "awesome" -d "I love this tool!" -f`

In order to use this command, you'll need to create a GitHub token.
If you don't have one already, please follow the instructions mentioned <a href=https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token style="color: #3366CC">here</a>.

## Flags
* **[-t] title** - Issue's title
* **[-d] description** - Issue's description, make it as clear as possible.
* **[-f] feature** - Use this flag to specify this is a feature request.
* **--token** - The GitHub token to use (for security reasons, you better use the GH_TOKEN environment variable).

## Environment Variables
**GH-TOKEN** - Use this to set the GitHub api token to be used to open the issue.