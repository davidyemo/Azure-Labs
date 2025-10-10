Task 1: Use a Template to Provision an Infrastructure

Deployed a virtual machine and virtual network in Azure using a custom ARM template and parameter file to create a test environment for backup and recovery.

Task 2: Create and Configure a Recovery Services Vault

Created a Recovery Services vault  `rvs-az104` in the same region as the VM, reviewed its backup configuration (geo-redundant storage) and confirmed that soft delete was enabled for protection.

![logo]()

Task 3: Configure Azure Virtual Machine-Level Backup

Set up VM level backup by creating a new daily backup policy, applying it to the virtual machine, and initiating the first backup process.

![logo]()



Task 4: Monitor Azure Backup

Donfigured the Recovery Services vault to archive logs and metrics to it, and reviewed the VM backup job details.

![logo]()

Task 5: Enable Virtual Machine Replication

Configured VM replication to a secondary region by creating another Recovery Services vault, enabling replication for the VM, and verifying that synchronization completed successfully.

![logo]()

![logo]()

![logo]()
