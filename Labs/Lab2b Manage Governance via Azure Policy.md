Lab 02b Manage Governance via Azure Policy


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

Task 3: Apply Tagging via an Azure Policy

I removed the previous policy and applied a new policy

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab2b-pic5.png)

Policy Test:
I created another storage account named projectazsotrageaccount this time, the deployment succeeded and the storage account was automatically tagged as expected.

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab2b-pic6.png)

Task 4: Configure and apply a resource lock 
The goal here was to prevent accidental deletions or modifications. I created a lock named: rglock set Lock Type: Delete and scope: Projectaz-rg2

Lock test I attempted to delete the resource group Projectaz-rg2. The deletion failed, as intended. Received error: "Delete resource group az 104-rg2 failed"

![logo](https://github.com/dy1000/Azure-Administrator-AZ-104-Labs/blob/main/Labs/All-Files/Lab2b-pic7.png)

 ✅ Lab Result: Success!
All tasks were completed and verified successfully:
	• Tags were created and enforced.
	• Policies were applied and tested.
	• Resources were protected with a lock.


