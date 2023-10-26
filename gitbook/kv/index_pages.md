# Get passwords from Azure Keyvault

###### Version 2.4.0

## I. About this document

This page explains how to get password to access some applications.

## II. Steps

Start from this screen, select `Managed resource group`:  
![](imgs/kv-goto-mrg-screen.png "")

Search for `kv` and then select the Key vault:
![](imgs/mrg-search-for-kv.png "")

Select `Access control IAM -> Add -> Add role assignment`:
![](imgs/kv-select-add-role-assignment.png "")

Select `Keyvault Secret Officer -> Next`: 
![](imgs/kv-select-role-kv-sec-officer.png "")

Select `Select members` -> Search for your account name -> Select that displayed account: 
![](imgs/kv-select-member.png "")

Confirm Selected members -> Next:
![](imgs/kv-member-selected.png "")

Select `Review + assign`:
![](imgs/kv-review-assign.png "")

Confirm that `Added Role assignment`:
![](imgs/kv-assign-success.png "")

Refresh page, Select `Secrets` -> Choose the password you want to see (Ex: `digdash-admin-password`):
![](imgs/kv-secret-tab-select.png "")

Select current version:  
![](imgs/kv-secret-select-current.png "")

Now you can show the value or copy it to clipboard:  
![](imgs/kv-copy-to-clipboard.png "")

Please use that value as the password to access applications. 

**Note**:  
- The password stored in Key Vault is the initial password. In the future, if you change the password within the application, the new password **will not** be automatically updated in Azure Key Vault. 

- If you change the value of secret in Azure Key Vault, it **will not** automatically update password in applications. 

---