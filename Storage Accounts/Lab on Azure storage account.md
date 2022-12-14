# Create a storage account using the Azure portal

1. Sign in to the Azure portal using the same account you used to activate the sandbox.
2. On the resource menu, or from the Home page, select Storage accounts. The Storage accounts pane appears.
3. On the command bar, select Create. The Create a storage account pane appears.
4. On the Basics tab, enter the  values for each setting.
5. Select Next : Advanced. On the Advanced tab, enter the  values for each setting.
6. Select Next : Networking. On the Networking tab, enter the values for each setting.
7. Select Next : Data protection. On the Data protection tab, enter the values for each setting.
8. Select Next : Encryption. Accept the defaults.
9. Select Next : Tags. Here, you can associate key/value pairs with the account for your categorization to determine if a feature is available to selected Azure resources.
10. Select Review + create to validate your options and to ensure all the required fields are selected. If there are issues, this tab will identify them so you can correct them.
11. When validation passes successfully, select Create to deploy the storage account.
12. When deployment is complete, which may take up to two minutes, select Go to resource to view Essential details about your new storage account.

# Create an Azure storage account using the Azure CLI 
 
1. Use the following example command to create a storage account. Remember to replace (name) with your unique storage account name.

    az storage account create \
    --resource-group dbcresource \
    --location westus \
    --sku Standard_LRS \
    --name azdemostorageacc

Descriptions:

1. --name ---) A storage account name. The name will be used to generate the public URL used to access the data in the account. It must be unique across all existing storage account names in Azure. It must be 3 to 24 characters long and can contain only lowercase letters and numbers.
2. --resource-group	Use ---) [sandbox resource group name] to place the storage account into the free sandbox.
3. --location ---)	Select a location near you (see below).
4. --sku ---)	The storage account performance and replication model. Options include Premium_LRS, Standard_GRS, Standard_LRS, Standard_RAGRS, and Standard_ZRS.

