---
title: About
---

<!-- Brief Feature Description -->

<!-- Beschreibung Produkt -->
Beyond CloudConnector is a Microsoft Dynamics 365 Business Central extension for connecting Sharepoint, Azure Files and Azure BLOB Storage. 
This extension allows you to store and link additional files, chaotically or structured, directly from Business Central to your own Microsoft Cloud, 
so that the corresponding files can be accessed quickly and easily from just one application. Depending on the connection, stored files in the Cloud can be 
previewed or downloaded directly in the web client.  

## <a name="storage-locations"></a>Storage Locations

The following storage options are included in this extension:  

+ **Azure Blob Storage**  
    “Azure Blob storage is Microsoft's object storage solution for the cloud. Blob storage is optimized for storing massive amounts of unstructured data. Unstructured data is data that doesn't adhere to a particular data model or definition, such as text or binary data.“  
    
    You can get more information on the official site of Microsoft:  
    [What is Azure Blob Storage? | Microsoft Docs](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-overview)

+ **Azure Files**  
    “Azure Files offers fully managed file shares in the cloud that are accessible via the industry standard Server Message Block (SMB) protocol, Network File System (NFS) protocol, and Azure Files REST API. Azure file shares can be mounted concurrently by cloud or on-premises deployments. SMB Azure file shares are accessible from Windows, Linux, and macOS clients. NFS Azure file shares are accessible from Linux or macOS clients. Additionally, SMB Azure file shares can be cached on Windows servers with Azure File Sync for fast access near where the data is being used.“  

    You can get more information on the official site of Microsoft:  
    [What is Azure Files? | Microsoft Docs](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-introduction)

+ **Sharepoint**  
    “Organizations use Microsoft SharePoint to create websites. You can use it as a secure place to store, organize, share, and access information from any device. All you need is a web browser, such as Microsoft Edge, Internet Explorer, Chrome, or Firefox.“

    You can get more information on the official site of Microsoft:  
    [Was ist SharePoint? - Office-Support (microsoft.com)](https://support.microsoft.com/en-us/office/what-is-sharepoint-97b915e6-651b-43b2-827d-fb25777f446f)

With these 3 connection options, files can be conveniently stored in a separate cloud storage at your own discretion. On the one hand, this has the advantage that the actual database does not increase unnecessarily in size and, on the other hand, that the
files have a central storage location and can be accessed immediately from anywhere with all devices. If multiple cloud services are available, it is up to you to assign the corresponding storage to a specific entity, so that in the end the service you prioritize can be used. All this can be defined and set up in Business Central.  

<!-- General Notes -->

<!-- :::caution -->
Moving or deleting data in the cloud storage must be prevented under all circumstances, as there is a link to Business Central and corresponding links become irreparable and thus unusable. Administrators have the option to delete files that are no longer linked from the data sets. This is the case, for example, if a file has been removed from the cloud storage but is still linked in Business Central.  
<!-- ::: -->

<!-- :::info   -->  
The **Cloud File Search** function becomes slower with each additional search criterion, since each term must again search the data sets including all metadata and temporarily store the partial result in the database.  
<!-- ::: -->