# Destroy
Use this command in order to clean all Terrap data from a given directory.

It will delete:
* The `.terraform` folder.
* The `.terraform.lock.hcl` file.
* The `.terrap.json` configuration file.

## Flags
* **[-d] directory** - Use this flag to specify which Terrap workspace to destroy.</br>
If not specified, will destroy the workspace in the current directory.