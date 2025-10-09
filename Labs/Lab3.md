<img width="2599" height="135" alt="image" src="https://github.com/user-attachments/assets/52a01c9d-5a93-42a7-9da1-c7c885b2644f" />Manage Azure resources by using Azure Resource Manager Templates

Task 1: Create an Azure Resource Manager Template

I created a managed disk in the Azure portal. Managed disks are storage designed to be used with virtual machines. Once the disk is deployed I exported a template that I can use in other deployments.
Managed Disk created with 32 Gib created.

![logo]()

Task 2: Edit Azure Resource Manager template and then redeploy the template

In the custom deployment I downloaded the template and parameter json files on to my local drive and edited the files and redeployed the temoate.

As you can see in the image below two disks are now showing after deployment.

![logo]()

Task 3: Configure the Cloud Shell and deploy a template with PowerShell

Deployed template using Powershell. As shown below command is completed and provisioning state succeeded.

![logo]()

Task 4: Deploy a template with the CLI 

Deployed template In the Cloudshell in the Bash scripting language. As shown below command is completed and provisioning state succeeded.

![logo]()

Task 5: Deploy a resource by using Azure Bicep

Used a Bicep file to deploy a managed disk in the cloudshell in a bash session. As shown below command is completed and provisioning state succeeded.

![logo]()



