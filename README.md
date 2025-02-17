Azure VM Project: End-to-End Lifecycle Management
This project demonstrates the full lifecycle of managing a Virtual Machine (VM) in Microsoft Azure using both the Azure Portal and Azure CLI/PowerShell. The project covers the following key steps:

Steps Completed:
Create a VM Using Azure Portal

Created a Virtual Machine via the Azure Portal.
Recreate the VM Using PowerShell/Azure CLI

Recreated the VM using Azure CLI with the necessary parameters.
Set Up Auto-Shutdown

Configured auto-shutdown for the VM to save costs.
Backup the VM

Created a Recovery Services Vault and applied a backup policy to the VM.
Delete the Resource Group

Deleted the resource group and all associated resources.

Technologies Used
Azure Portal
Azure CLI
PowerShell
Azure Recovery Services Vault
Azure Virtual Machines

Future Steps
Once the resource group deletion is completed, the project can be reviewed and further enhanced with additional features like automation for VM scaling or other Azure services.

Key Commands Used
Create VM Using Azure CLI:

bash
az vm create --resource-group MyNewResourceGroup --name VM2 --image UbuntuLTS --size Standard_B1s --admin-username azureuser --admin-password 'Password123!'
Enable Backup Protection:

bash
az backup protection enable-for-vm --resource-group MyNewResourceGroup --vault-name MyBackupVault --vm VM2 --policy-name EnhancedPolicy
Auto-Shutdown:

bash
az vm auto-shutdown --resource-group MyNewResourceGroup --name VM2 --time 2200
Delete Resource Group:

bash
az group delete --name MyNewResourceGroup --yes --no-wait
