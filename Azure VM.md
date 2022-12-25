# How to deploy Azure Virtual Machine - Windows Server in MAC

### Task 1 - Log into the Azure Portal

1. Log in to the Azure portal using the credentials provided on the lab page. Be sure to use an incognito or private browser window to ensure you're using the lab account rather than your own.

### Task 2 - Create a Virtual Machine

1. In the Azure Portal, navigate to the Virtual machines dashboard.
2. Create a Windows Server 2016 Datacenter - Gen 2 virtual machine with the following settings:
3. Resource group: Select the pre-provisioned group from the dropdown
4. Virtual machine name: acg-firstdeploy
5. Region: Select the same region as the lab-provided resource group
6. Image: Windows Server 2019 Datacenter - Gen 2
7. Size: Leave as the default size
        Username: vmwindowsazure-admin
        Password: Admin123456!

### task 3 - Connect to the Virtual Machine

1. Download the RDP file and connect to the virtual machine.
    Mac Users:

    Make sure you download the latest Windows RDP client to connect to the newly-created virtual machine using the downloadable executable file:
    https://apps.apple.com/app/microsoft-remote-desktop/id1295203466?mt=12

    Note: For the image type, please use: Windows Server 2019 Datacenter - Gen 2.

### Task 4 - Stop and Delete the Virtual Machine

1. Discpnnect from the virtual machine and stop it using the Azure Portal.
2. Delete the virtual machine using the Azure Portal.