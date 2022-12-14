# Create a storage account to use with Azure Data Lake Storage Gen2

1. Data Lake Storage capabilities are supported in the following types of storage accounts:
2. Standard general-purpose v2
3. Premium block blob
4. You can choose between these two types of accounts in the Basics tab of the Create a storage account page.
    a. To create a standard general-purpose v2 account, select Standard.
    b. To create a premium block blob account, select Premium. Then, in the Premium account type dropdown list, select Block blobs.

### Enable the hierarchical namespace

5. Unlock Data Lake Storage capabilities by selecting the enable hierarchical namespace setting in the Advanced tab of the Create storage account page.

# Create an Azure storage account with Azure Data Lake Storage Gen2 using the Azure CLI 

1. # Create the storage account
    a. az storage account create --name my-storage-account-name --resource-group my-resource-group --sku Standard_LRS --kind StorageV2 --hierarchical-namespace true


https://learn.microsoft.com/en-us/training/modules/upload-data-to-azure-data-lake-storage/2-create-azure-data-lake?ns-enrollment-type=learningpath&ns-enrollment-id=learn.data-ai.data-processing-with-azure-adls
https://learn.microsoft.com/en-us/training/modules/upload-data-to-azure-data-lake-storage/3-upload-data-using-explorer?ns-enrollment-type=learningpath&ns-enrollment-id=learn.data-ai.data-processing-with-azure-adls