# Azure Cloud Monitor Documentation 

This Azure Cloud Monitor Documentation serves as a guide to create your own workbooks and dashbords to monitor your Azure resources. Some of this templates are adapted from [Panaroma](https://github.com/weixian-zhang/Panorama), [The Ultimate Inventory Dashboard](https://github.com/scautomation/Azure-Inventory-Workbook) and [Azure Public Templates](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/workbooks)

## Contents 
1. [Set up the log analytics workspace](#Set-up-the-log-analytics-workspace)
2. [Enable monitoring for your VM](#enable-monitoring-for-your-VM)
3. [Create Workbooks](#create-workbooks)
4. [Create DashBoards](#Create-dashBoards)


## Set up the log analytics workspace

Before Azure Monitor can collect logs, ensure that the VM is connected to a log analytics workspace (LAW) is connected.
This can be done in multiple ways, including manually thorugh the Azure portal or through Terraform code.

#### Enable the agent manually through Azure portal
Navigate to LAW and create a worspace or use an existing one. Under workspace data sources, click on virtual machines and connect it to the LAW. 

<img src="https://user-images.githubusercontent.com/58519490/124719077-565d0a00-df39-11eb-8882-be2520a01022.png" width="700">

If you have enabled the agent manually in the previous step, skip to the [next step](#enable-monitoring-for-your-VM).

#### Install the agent through terraform 
Refer to the file [here](https://github.com/Mingze28/Cloud-Monitor-Documentation-/blob/master/VM%20infra%20with%20Agent/main.tf) for the infrastructure as code for the virtual machine and agent.
<img src="https://user-images.githubusercontent.com/54704393/124894949-b07bcf00-e00e-11eb-945e-88f6eb095ae6.png" width="600">

## Enable monitoring for your VM
Navigate to Azure Monitor, under Insights, Virtual Machines and enable the virtual machines you want to monitor.
<img src="https://user-images.githubusercontent.com/54704393/124569677-bb046000-de78-11eb-8fef-a29bf7cb8930.png" width ="700">

Ensure your VMs are connected properly by running a heartbeats query under Azure logs.
<img src="https://user-images.githubusercontent.com/54704393/124570134-2cdca980-de79-11eb-8f78-446637880881.png" width="700">

## Create Workbooks
- Copy the workbook file and paste it to Azure workbook. Make sure your file is in json format. You can find some workbook templates under [Panoroma](https://github.com/weixian-zhang/Panorama/tree/master/Workbooks), [The Ultimate Inventory Dashboard](https://github.com/scautomation/Azure-Inventory-Workbook) and [Azure Public Templates](https://portal.azure.com/#blade/Microsoft_Azure_Monitoring/AzureMonitoringBrowseBlade/workbooks).
<img src="https://user-images.githubusercontent.com/54704393/124572186-091a6300-de7b-11eb-9878-c3226b33b0cf.png" width="700">

- Adding additional filters

Filters can help you focus on specific areas. To add filters for subscriptions:
  1. Add parameters for your workbook
  <img src ="https://user-images.githubusercontent.com/54704393/124579000-51d51a80-de81-11eb-97ad-e2572a961e38.png" width="700">

  2. Add a new subscription selection field to help you filter out unneeded subscription 
  <img src="https://user-images.githubusercontent.com/54704393/124579227-8052f580-de81-11eb-9311-1e57f1dfae99.png" width="700">
  
  3. Change your workbook query settings to your own parameters
  <img src="https://user-images.githubusercontent.com/54704393/124579938-31f22680-de82-11eb-8135-d96698cb15e5.png" width="700">
 
## Create dashboards

- Dashboards can be created by pinning your log/metric query result or workbooks to your dashboard.
  <img src ="https://user-images.githubusercontent.com/54704393/124864404-6af9da80-dfeb-11eb-99ba-5d37b5b97322.png" width="700">
- Tiles can be resized or moved in the dashboard
  <img src ="https://user-images.githubusercontent.com/54704393/124864734-02f7c400-dfec-11eb-99d8-930d9825277b.png" width="700">
















