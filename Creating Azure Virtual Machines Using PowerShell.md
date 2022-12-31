# Creating Azure Virtual Machines Using PowerShell

In this lab we use the Cloud Shell(Azure PowerShell) within the Azure Portal, to create Virtual Machine.


### Task -1 Create a Virtual Machine

1. Identify the existing resource group with 
    a. Get-AzResourceGroup.

2. Create the virtual machine with New-AzVm. Create a virtual network using Azure PowerShell and the following settings:

    a. Resource group: Existing resource group  -- dbcresource
    b. Name: TestVM  -- [, >, /, ?]
    c. Virtual network: MyVnet
    d. Security group: MySecurityGroup
    e. Subnet: MySubnet
    f. Public IP address: MyPubIP
    g. Open ports: 80, 3389

Use the following command as a guide.

new-azvm -ResourceGroupName 'dbcresource' -Name 'azurevm01' -VirtualNetworkName 'MyVNet1' -SubnetName 'MySubnet1' -SecurityGroupName 'MySecurityGroup1' -PublicIpAddress 'myPubIP1' -OpenPorts 80,3389


username - azureuser
pwd - azure123@

### Task-2 Obtain the Public IP Address

1. Get the public IP address using 
    a. Get-AzPublicIPAddress


### Task-3 Delete the Azure VM from powershell

1. Remove a virtual machine
    a. Remove-AzVM -ResourceGroupName "dbcresource" -Name "azurevm01"

Resource

1. https://learn.microsoft.com/en-us/powershell/module/az.compute/new-azvm?view=azps-9.2.0
2. https://learn.microsoft.com/en-us/powershell/module/az.compute/remove-azvm?view=azps-9.2.0