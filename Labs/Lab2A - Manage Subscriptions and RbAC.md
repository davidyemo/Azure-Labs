This lab focuses on role-based access control (RBAC) in Microsoft Entra ID and Azure. It includes creating and assigning both built-in and custom roles to a group at the management group level, and monitoring activity through the Azure Activity Log. The goal is to enforce principle of least privilege while enabling the IT Helpdesk to operate effectively within the defined boundaries.

Task 1: implement Management Groups
Created a Management Group called projectaz-mg1
Purpose is to organize Azure resources under a unified governance and access control hierarchy. ![logo](L )

Task 2: Review and assign a built in Azure role
Assigned virtual machine contributor to the IT Project administrators group on the Access control (IAM) blade under the role assignments tab.

Task 3: Create a custom RBAC role

Within the projectaz-mg1 management group in the Access control (IAM) blade I added a custom role called customer support request and assigned to the IT Project administrators group.
Image 3

Task 4: Monitor role assignments with the activity log

I monitored role assignments by using the azure activity log to track role assignments, scope changes and custom role creation events to ensure actions performed by the IT project administratirs group adhered to restricted permissions.
Image 5

Tools & Concepts Used
Microsoft Entra ID (Azure AD), Azure Management Groups, Role-Based Access Control (RBAC), Custom Role Definition  and Azure Activity Logs.

✅ Outcome
 Successfully enforced a least privilege model by assigning only the necessary permissions to the IT Helpdesk group, while restricting sensitive operations like registering resource providers.


