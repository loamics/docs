# APIM - API Management

###### Version 1.1.3

## 1. Access to APIM Developer Portal UI

First get the URL in the deployment outputs info of your Azure Managed Application

![apimdevportal_url](imgs/apim_dev_url.png "")

Don't forget to allow your Personal Public IP thanks to the NSG Rule. 
Then go to the URL, no need to authenticate

![apimdevportal_ui](imgs/apim_dev_ui.png "")

Click on `API` tab, then select `Algo Library Catalog API` for example:  
![apimdevportal_ui](imgs/apim_dev_api_tab.png "")


Select `Get all algorithms` and click `Try it`:  
![apimdevportal_ui](imgs/apim_dev_api_get_all_algo.png "")

If you see this error, it means you should provide `Ocp-Apim-Subscription-Key` in the Header:  
![apimdevportal_ui](imgs/apim_dev_api_missing_ocp_key.png "")

See the next section to get `Ocp-Apim-Subscription-Key`

## 2. How to get Ocp-Apim-Subscription-Key of APIM

2.1/ Go to [Azure Portal](https://portal.azure.com)

2.2/ Locate and go to your Managed Application

![managed_app](imgs/managed_app.png "")

2.3/ Locate and go to the Managed resource group  

![managed_rg](imgs/managed-resource-group.png "")

2.4/ Filter `apim` and select the `API Management service` resource type  

![apim](imgs/apim_rs_azure_portal.png "")

2.5/ Select `Subscription` tab then try to Copy the primary/secondary key  

![apim_ocp](imgs/apim_rs_get_ocp_key.png "")  

![apim_ocp2](imgs/apim_rs_copy_key.png "")  

2.6/ Paste the `Ocp-Apim-Subscription-Key` to this field and click `Send` to make the request

![apim_get_all_algo](imgs/apim_dev_api_get_all_algo_w_ocp_key.png "")  

If everything OK, you will get the Respone 200 status:  
![apim_get_all_algo_200](imgs/apim_dev_api_get_all_algo_200.png "")  



---