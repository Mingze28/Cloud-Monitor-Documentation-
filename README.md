# Azure Workbook Usage Guide 

This Github repository is to demonstrate how to create your own monitor workbook by using azure workbook templates.

## Prerequisites

Here are some of the prerequisites that you need to check before you start

### 1. Install the monitor agent extension for your Virtual Machines

#### Install the agent manually through Azure portal
![image](https://user-images.githubusercontent.com/54704393/124568898-01a58a80-de78-11eb-8707-6edbedb28b3a.png)

#### Install the agent through terraform
![image](https://user-images.githubusercontent.com/54704393/124569312-6b259900-de78-11eb-9ab3-177587abb519.png)

#### Enable Azure monitor for VMs
![image](https://user-images.githubusercontent.com/54704393/124569677-bb046000-de78-11eb-8fef-a29bf7cb8930.png)

#### Ensure your VMs are sending heartbeat to Azure log
![image](https://user-images.githubusercontent.com/54704393/124570134-2cdca980-de79-11eb-8f78-446637880881.png)

### 2. Change the workbook template's subscription id to your own.
![image](https://user-images.githubusercontent.com/54704393/124571175-23a00c80-de7a-11eb-880b-e1913187c699.png)
You will need to change the template's subscription to your own one. Next, we will show you how you can copy the template 
to make your own monitor workbook

## Create workbook through Gallery Template
1. Copy the workbook file and paste it to Azure workbook. Make sure your file is in json format. You can find some workbook templates through this link: https://github.com/weixian-zhang/Panorama/tree/master/Workbooks
![image](https://user-images.githubusercontent.com/54704393/124572186-091a6300-de7b-11eb-9878-c3226b33b0cf.png)

2. Add additional filters 
The filters can help you focus on specific area you are interested in. 
  - Add parameters for your workbook
  ![image](https://user-images.githubusercontent.com/54704393/124579000-51d51a80-de81-11eb-97ad-e2572a961e38.png)

  - Add a new subscription selection field to help you filter out unneeded subscription 
  ![image](https://user-images.githubusercontent.com/54704393/124579227-8052f580-de81-11eb-9311-1e57f1dfae99.png)
  
  - Change your workbook query settings to your own parameters
  ![image](https://user-images.githubusercontent.com/54704393/124579938-31f22680-de82-11eb-8135-d96698cb15e5.png)
 
















