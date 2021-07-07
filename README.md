# Azure Cloud Monitor Documentation 

This Azure Cloud Monitor Documentation serves as a guide to create your own workbooks and dashbords to monitor your Azure resources. Some of this templates are adapted from [Panaroma](https://github.com/weixian-zhang/Panorama), [The Ultimate Inventory Dashboard](https://github.com/scautomation/Azure-Inventory-Workbook) and [Azure Public Templates](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/workbooks)

## Contents 
1. [Set up an agent for your VM](#set-up-an-agent-for-your-vm)
2. [Enable monitoring for your VM](#enable-monitoring-for-your-VM)
3. [Create Workbooks](#create-workbooks)
4. [Create DashBoards](#Create-dashBoards)


## Set up an agent for your VM

Here are some of the prerequisites that you need to check before you start

### 1. Install the monitor agent extension for your Virtual Machines

#### Install the agent manually through Azure portal
<img src="https://user-images.githubusercontent.com/58519490/124719077-565d0a00-df39-11eb-8882-be2520a01022.png" width="700">

#### Install the agent through terraform

### 2. Enable monitoring for your VM
![image](https://user-images.githubusercontent.com/54704393/124569677-bb046000-de78-11eb-8fef-a29bf7cb8930.png)

#### Ensure your VMs are sending heartbeat to Azure log
![image](https://user-images.githubusercontent.com/54704393/124570134-2cdca980-de79-11eb-8f78-446637880881.png)

<!-- ### 2. Change the workbook template's subscription id to your own.
![image](https://user-images.githubusercontent.com/54704393/124571175-23a00c80-de7a-11eb-880b-e1913187c699.png)
You will need to change the template's subscription to your own one. Next, we will show you how you can copy the template 
to make your own monitor workbook -->

### 3. Create Workbooks
- Copy the workbook file and paste it to Azure workbook. Make sure your file is in json format. You can find some workbook templates through this link: https://github.com/weixian-zhang/Panorama/tree/master/Workbooks
![image](https://user-images.githubusercontent.com/54704393/124572186-091a6300-de7b-11eb-9878-c3226b33b0cf.png)

- Add additional filters 
The filters can help you focus on specific area you are interested in. 
  - Add parameters for your workbook
  ![image](https://user-images.githubusercontent.com/54704393/124579000-51d51a80-de81-11eb-97ad-e2572a961e38.png)

  - Add a new subscription selection field to help you filter out unneeded subscription 
  ![image](https://user-images.githubusercontent.com/54704393/124579227-8052f580-de81-11eb-9311-1e57f1dfae99.png)
  
  - Change your workbook query settings to your own parameters
  ![image](https://user-images.githubusercontent.com/54704393/124579938-31f22680-de82-11eb-8135-d96698cb15e5.png)
 
### 4. Create dashboards















