## V. Update IP whitelist 

### 1. Prerequisites

From PaaS version v1.1.3, Azure Application Gateway is applied as the below diagram:  

![appgw_diagram](imgs/appgw_diagram_v1.1.3.png "")

Since Azure Application Gateway supported only TLS 1.2, client web browser should enable support for TLS 1.2 also.

### 2. In case you want to update IP whitelist for above services

2.1/ Go to [Azure Portal](https://portal.azure.com)

2.2/ Locate and go to your Managed Application

![managed_app](imgs/managed_app.png "")

2.3/ Locate and go to the Managed resource group

![managed_rg](imgs/managed-resource-group.png "")

2.4/ Filter `appgw` and select the Network Security Group resource type:  
![appgw_nsg](imgs/appgw-nsg-v1.1.3.png "")

2.5/ Select `Inbound security rules` then you can update IP in the `Allow_Whitelist` rule

![appgw_nsg](imgs/appgw_update_whitelist_ip.png "")

When the rule is updated, you can test the connection.  

If you have issues when updating the rule, maybe you don't have enough permission, you should contact Publisher for support.  

### 3. In case you want to update IP whitelist for SFTP server and SSH server

Azure Application doesn't apply for SSH and SFTP server. They manage whitelist IP in the separate Network security group (NSG)

3.1/ Go to [Azure Portal](https://portal.azure.com)

3.2/ Locate and go to your Managed Application

![managed_app](imgs/managed_app.png "")

3.3/ Locate and go to the Managed resource group

![managed_rg](imgs/managed-resource-group.png "")

3.4/ Filter `sftp` and select the Network Security Group resource type:  
![sftp_nsg](imgs/sftp-nsg-v1.1.3.png "")

3.5/ Select `Inbound security rules` then you can update IP in the `Allow_Whitelist` rule

When the rule is updated, you can test the connection.

You can filter `ssh` to do the same way with SSH server's Network security group.
