This lab is focused on managing governance in Azure using tags, Azure policies, and resource locks. Below are the steps I followed, along with test results and outcomes.

Task 1: Create and Assign Tags via the Azure Portal

I began by creating a resource group named: Projectaz-rg2

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab2b-pic1.png)

Next, I added a resource tag to the resource group:
Tag Name: cost center and Tag Value: 000

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab2b-pic2.png)

Task 2: Enforce the Resource Tag via an Azure Policy
To enforce tagging I assigned the built-in policy called 'require a tag and its value on resources', Scope Resource Group – Projectaz-rg2 and Enabled Policy Enforcement.
Tag Name: cost center and Tag Value: 000

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab2b-pic3.png)

Policy Test:
I attempted to create a storage account called projectstorageacc The deployment failed as expected because the tag cost center with the required value 000 was not included in the resource definition.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab2b-pic4.png)
