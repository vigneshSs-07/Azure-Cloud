# Hands-On how to Access and Use the Azure Cloud Shell

1. Azure CLI and Azure PowerShell are command-line tools that enable you to create and manage Azure resources. Both are cross-platform, installable on Windows, macOS, and Linux.

### Azure CLI

1. Cross-platform command-line interface, installable on Windows, macOS, Linux
2. Runs in Windows PowerShell, Cmd, or Bash and other Unix shells.
3. Azure CLI syntax is similar to that of Bash scripting. If you work primarily with Linux systems, Azure CLI feels more natural.

### Azure PowerShell

1. Cross-platform PowerShell module, runs on Windows, macOS, Linux
2. Requires Windows PowerShell or PowerShell
3. Azure PowerShell is a PowerShell module. If you work primarily with Windows systems, Azure PowerShell is a natural fit. Commands follow a verb-noun naming scheme and data is returned as objects.

### Difference between Azure CLI (BASH) and Azure Powershell

Command	                        Azure CLI	            Azure PowerShell

Find Version	                az --version	    Get-InstalledModule -Name Az
Get Help	                    az --help	        Get-Help
View Command Help	            az vm --help	    Get-Help -Name New-AzVM

List VM	                        az vm list	        Get-AzVM

Create Azure Virtual Machine	
Azure CLI
1. az vm create --resource-group myResourceGroup --name myVM --image UbuntuLTS --admin-username azureuser --admin-password '<Password>'	
Azure PowerShell
2. New-AzVM -ResourceGroupName <ResourceGroupName> -Name myVM -Image UbuntuLTS -Credential (Get-Credential)

Create Azure Storage Account	
1. Azure CLI
az storage account create --name <StorageAccountName> --resource-group <ResourceGroupName> --location eastus --sku Standard_LRS --kind StorageV2	
2. Azure PowerShell
New-AzStorageAccount -Name <StorageAccountName> -ResourceGroupName <ResourceGroupName> -Location eastus -SkuName Standard_LRS -Kind StorageV2

### Task 1 - When setting up the Azure Cloud Shell:

1. In the Azure Portal, click the Cloud Shell icon (>_) in the top right corner of the screen.
2. In the Cloud Shell welcome menu, click PowerShell.
3. In the storage menu, click Show advanced settings.
4. Use the lab-provided subscription. Use the existing resource group. Use Central US for the location. Create a new, uniquely named Storage account and a new, uniquely named File Share.Click Create storage.


### Task 2 - Configure Cloud Shell

1. Execute Azure CLI Commands in the Cloud Shell

Use Azure CLI commands to list the resource groups, storage accounts, virtual machines, and all resources available in our Azure subscription.
Note the output.

*Commands:*

    az group list
    az storage account list
    az vm list

2. Create a Virtual Machine Using the Azure CLI. Create a virtual machine in the cloud shell, using the actual name of your lab resource group for the resource-group.
Verify the creation of the virtual machine.

*Commands:* # Azure Bash

    az vm create --name demoLAB --resource-group dbcresource  --image UbuntuLTS --admin-username azureuser --generate-ssh-keys

3. Run PowerShell Cmdlets in the Cloud Shell.Run PowerShell cmdlets to list resource groups, storage accounts, virtual machines, and all resources available in the lab.

*Commands:*  # Powershell

    Get-AzResourceGroup       
    Get-AzStorageAccount
    Get-AzVM
    Get-AzResource | ft

4. Remove the Virtual Machine.Use a cmdlet to remove the virtual machine, providing the names of the virtual machine and resource group for the -Name and -ResourceGroupName parameters, respectively.Verify that the virtual machine has been deleted.

*Commands:*

    Remove-AzVM -Name demoLAB -ResourceGroupName dbcresource

###### Helpful Links

1. Azure CLI Overview: https://docs.microsoft.com/en-us/cli/azure/?view=a
2. Azure CLI Reference: https://docs.microsoft.com/en-us/cli/azure/reference-index?view=azure-cli-latest
3. Azure PowerShell Overview: https://docs.microsoft.com/en-us/powershell/azure/overview?view=azps-1.6.0
4. Quickstart for Bash in Azure Cloud Shell: https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart
5. Quickstart for PowerShell in Azure Cloud Shell: https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart-powershell










