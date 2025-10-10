Manage Azure resources by using Azure Resource Manager Templates

This lab focused on deploying and managing Azure resources using through ARM templates, PowerShell, CLI, and Bicep.

Task 1: Create an Azure Resource Manager Template

Created a managed disk in the Azure portal. Managed disks are storage designed to be used with virtual machines. Once the disk is deployed I exported a template that I can use in other deployments.
Managed Disk created with 32 Gib created.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab3-pic1.png?raw=true)

Task 2: Edit Azure Resource Manager template and then redeploy the template

In the custom deployment I downloaded the template and parameter json files on to my local drive and edited the files and redeployed the temoate.

As shown in the image below two disks are now showing after deployment.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab3-pic2.png?raw=true)

Task 3: Configure the Cloud Shell and deploy a template with PowerShell

Deployed template using Powershell. As shown below command is completed and provisioning state succeeded.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab3-pic3.png?raw=true)

Task 4: Deploy a template with the CLI 

Deployed template In the Cloudshell in the Bash scripting language. As shown below command is completed and provisioning state succeeded.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab3-pic4.png?raw=true)

Task 5: Deploy a resource by using Azure Bicep

Used a Bicep file to deploy a managed disk in the cloudshell in a bash session. As shown below command is completed and provisioning state succeeded.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab3-pic5.png?raw=true)



