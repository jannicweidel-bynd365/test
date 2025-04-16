---
title: Questions
---

# <a name="faq"></a>Frequently Asked Questions

In this section we address frequently asked questions about BeyondCloudConnector.  

If you have a question that is not listed in this chapter, contact us at 
<a href="mailto:info@beyondit.gmbh?cc=sascha.fischer@beyondit.gmbh&amp;subject=Question about BeyondCloudConnector">info@beyondit.gbmh</a>.  


## <a name="how-to-set-up-user-permissions"></a>I have several new users who should use BeyondCloudConnector. How do I set the user permissions?

You have several options for granting user permissions:  

You can copy the permissions of an existing user for the new user or define all permissions for the dropzone/s and file preview at the same time. For more information, please refer to the chapter [Set Up Users](../Setup/set-up-users.md).  


## <a name="no-connection"></a>BeyondCloudConnector was able to connect to cloud storage in the past, but this no longer works. What should I do?

Verify that the cloud application is set up correctly. The secret key (for Sharepoint setup: [Create and Copy Secret](../Setup/set-up-for-sharepoint.md#create-and-copy-secret)) or the Shared Access Signature in Mircosoft Azure has expired. For more information regarding Azure Files Setup go to [Setup > Set Up Azure Files as Cloud Stoarge > Create Shared Access Signatures](../Setup/set-up-for-azure-files.md#create-sas) and regarding Azure Blob Storage Setup go to [Setup > Set Up Azure Blob Storage as Cloud Storage > Create Shared Access Signatures](../Setup/set-up-for-azure-blob-storage.md#create-sas).  

If the issue persists, contact us: 
<a href="mailto:info@beyondit.gmbh?cc=sascha.fischer@beyondit.gmbh&amp;subject=Connection issue with cloud storage (BeyondCloudConnector)">info@beyondit.gbmh</a>.  


## <a name="license-expired"></a>I get a message that my license has expired. What do I need to do?  

If you wish to continue using BeyondCloudConnector, you must purchase a license or multiple licenses. For more information on current pricing as well as ongoing marketing campaigns or special offers, please visit our website [https://www.beyond-cloudconnector.de/](https://www.beyond-cloudconnector.de/).  

If you do not want to continue using BeyondCloudConnector, you can uninstall the app via the extension management.  


## <a name="which-license-is-best"></a>Which license model is suitable for my company?

We offer different licensing models. 
Licensing is based on the number of users in the system. <u>All users</u> in the system are counted, regardless of whether they have access to BeyondCloudConnector.  

For more information on current pricing, as well as ongoing marketing campaigns or special offers, please visit our website at [https://www.beyond-cloudconnector.de/](https://www.beyond-cloudconnector.de/).


## <a name="new-version"></a>I have been informed that a new version of BeyondCloudConnector is available. How do I update the app?  

The new version of the application is updated automatically with each update from Microsoft. If you do not want to wait for the next update from Microsoft, you can update the application manually. To update the application manually, proceed as described in the section [Update to the latest version of CloudConnector](update-your-cloudconnector-version.md).  


## <a name="which-cloud-storage-is-the-cheapest"></a>Which cloud storage is the cheapest?

By default, an Office 365 subscription includes storage for **SharePoint Online**. 
So you don't have to pay extra for storage. 
The storage size for Sharepoint depends on the licenses in your organization. 
You can see the storage size for Sharepoint in the Sharepoint Admin Center.  

If you select Azure Files or Azure Blob Storage as cloud storage, additional costs will apply depending on the size and characteristics of the storage volume. For more information about associated storage costs, see:  

[Pricing for Sharepoint Online](https://www.microsoft.com/en-us/microsoft-365/sharepoint/compare-sharepoint-plans)  
[Pricing for Azure Files](https://azure.microsoft.com/en-us/pricing/details/storage/files/)  
[Pricing for Azure Blob Storage](https://azure.microsoft.com/en-us/pricing/details/storage/blobs/)  


## <a name="edit-structure"></a>I want to change the folder structure in Sharepoint/Azure Files or Azure Blob Storage. Is there anything I need to consider?  

Yes, you should back up the files before changing the structure. Then delete the data from Business Central and the cloud storage and then rebuild the structure. By changing the folder structure in the cloud storage, the connections between Business Central and the cloud storage are lost, i.e. you need to reimport the files so that the connections between Business Central and the cloud storage are created.  


## <a name="import-files-from-onpremise-to-cloud"></a>I want to migrate file attachments from an OnPremise environment to the cloud. Is this possible and if so how do I do that?  

Yes, this is possible. We have programmed a codeunit especially for this use case, which allows you to export the file attachments of an OnPremise environment, so that you can upload them to the cloud via the CloudConnector. Please note that at the time of the file export, no cloud storage must have been set up in the **Beyond CloudConnector**.  

Download the file export code unit: [Codeunit for exporting files](https://github.com/byndit/BeyondCloudConnector-Example/blob/main/BeyondCC/src/ExportData/ExportfromAttachments.Codeunit.al)  

Export the files and then upload them to Azure Files.  
Then proceed as described in the chapter [Import files from Azure Files](../Setup/set-up-for-azure-files.md#import-files-from-azure-files). Please note that the JSON file must also be uploaded to Azure Files.  

Afterwards, you can also move the files to another cloud storage (for example, Sharepoint or Azure Blob). To do this, proceed as described in the chapter [Move files to another cloud storage](../features/move-files-to-different-storage.md).  

