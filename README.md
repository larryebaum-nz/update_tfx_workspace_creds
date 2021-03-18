# update_tfx_workspace_creds
Update TFX Workspace Credentials with new Doormat values

These lines can be added to a users shell init script to quickly fetch the list of workspaces within a TFE or TFC organization. While this could also be used, with slight modification to count workspaces, the intent here is to push updated cloud credentials to environment variables within the workspace.

## Environment

Set variables within the init script (unless already set, in which case just modify to match your variables). Should you have multiple organizations, simply duplicate each entry with a different name to match and be sure to include a unique token per organization.

* `TFH_token` - Set to the TFC/TFE token for a specific organization
* `TFH_org` - Set to the TFC/TFE organization name

##  Output

```
$ TFEpushAWSkeys
ERRO[0000] New Doormat CLI recommended: v2.10
==> Refreshing Doormat Credentials
==> Successfully refreshed Doormat credentials!
terraform-aws-basic-instance
INFO[0000] Getting Creds for TFC/TFE
INFO[0002] Creds pushed to "terraform-aws-basic-instance"
INFO[0002] Done
hashicat-aws
INFO[0001] Getting Creds for TFC/TFE
INFO[0003] Creds pushed to "hashicat-aws"
INFO[0003] Done
...
```
## To Do
* Variablize the doormat account name within the alias command.
