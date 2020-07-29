---
id: "working-with-storage"
url: "metadata/working-with-storage"
title: "Working With Storage"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
---






# Storage existence API #

This API intended for checking the existence of cloud storage with a given name from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).
|---|---

## API Explorer ##

[GroupDocs.Metadata Cloud API Reference](https://apireference.groupdocs.cloud/metadata/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/metadata/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.
|---|---|---|---

### Request parameters ###

|#
|---
Parameter
|#
Description

|
**storageName**
|
Storage name


## cURL Example ##



 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v1.0/metadata/storage/MyStorage/exist" -H  "accept: application/json" -H  "authorization: Bearer  [Access Token]"
    
 ```


 Response

```html 
{
  "exists": true
}
 ```




## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-metadata-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-metadata-cloud), it hides the [Storage existence](https://apireference.groupdocs.cloud/metadata/#/Storage/StorageExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###



 C#




{{< gist groupdocscloud 90da27f305908428852e34cf1ed77ad0 Metadata_CSharp_Storage_Exist.cs >}}





 Java




{{< gist groupdocscloud 499959a7260c4903f836012226cb2dac Metadata_Java_Storage_Exist.java >}}







# Storage object existence API #

This API intended for checking the existence of a file or folder in [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).
|---|---

## API Explorer ##

[GroupDocs.Metadata Cloud API Reference](https://apireference.groupdocs.cloud/metadata/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/metadata/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.
|---|---|---|---

### Request parameters ###

|#
|---
Parameter
|#
Description

|

**path**
|

Path of the file or folder

Required. Can be passed as a query string parameter or as part of the URL

|
storageName
|
Name of the storage. If not set, then default storage used

|

versionId
|

File version id


## cURL Example ##



 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v1.0/metadata/storage/exist/metadatadocs?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
 ```


 Response

```html 
{
  "exists": true,
  "isFolder": true
}
 ```




## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-metadata-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-metadata-cloud), it hides the [Storage Object existence](https://apireference.groupdocs.cloud/metadata/#/Storage/ObjectExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###



 C#




{{< gist groupdocscloud 90da27f305908428852e34cf1ed77ad0 Metadata_CSharp_Object_Exists.cs >}}





 Java




{{< gist groupdocscloud 499959a7260c4903f836012226cb2dac Metadata_Java_Object_Exists.java >}}







# Storage Space Usage API #

This API intended for getting total and used space of the[ GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)
|---|---

## API Explorer ##

[GroupDocs.Metadata Cloud API Reference](https://apireference.groupdocs.cloud/metadata/#/) lets you try out [storage space usage API](https://apireference.groupdocs.cloud/metadata/#/Storage/GetDiscUsage) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.
|---|---|---|---

### Request parameters ###

|#
|---
Parameter
|#
Description

|
storageName
|
Name of the storage. If not set, then default storage used


## cURL Example ##



 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v1.0/metadata/storage/disc?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
 ```


 Response

```html 
{
  "usedSize": 31032368,
  "totalSize": 3221225472
}
 ```




## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-metadata-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-metadata-cloud), it hides the [storage space usage API](https://apireference.groupdocs.cloud/metadata/#/Storage/GetDiscUsage) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###



 C#




{{< gist groupdocscloud 90da27f305908428852e34cf1ed77ad0 Metadata_CSharp_Get_Disc_Usage.cs >}}





 Java




{{< gist groupdocscloud 499959a7260c4903f836012226cb2dac Metadata_Java_Get_Disc_Usage.java >}}







# Storage File Versions API #

This API intended for getting the list of file versions, stored in the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)
|---|---

## API Explorer ##

[GroupDocs.Metadata Cloud API Reference](https://apireference.groupdocs.cloud/metadata/#/) lets you try out [Storage File Versions API](https://apireference.groupdocs.cloud/metadata/#/Storage/GetFileVersions) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.
|---|---|---|---

##### Request parameters #####

|#
|---
Parameter
|#
Description

|

**path**
|

Path of the file including file name and extension e.g. /Folder1/file.ext

Required. Can be passed as a query string parameter or as part of the URL

|
storageName
|
Name of the storage. If not set, then default storage used


## cURL Example ##



 Request

```html 
curl -X GET "https://api.groupdocs.cloud/v1.0/metadata/storage/version/one-page.docx?storageName#MyStorage" -H  "accept: application/json" -H  "authorization: Bearer [Access Token]"
 ```


 Response

```html 
{
  "value": [
    {
      "versionId": "null",
      "isLatest": true,
      "name": "one-page.docx",
      "isFolder": false,
      "modifiedDate": "2018-08-16T19:45:05+00:00",
      "size": 347612,
      "path": "/one-page.docx"
    }
  ]
}
 ```




## SDKs ##

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-metadata-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-metadata-cloud), it hides the [Storage File Versions API](https://apireference.groupdocs.cloud/metadata/#/Storage/GetFileVersions) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.
|---|---|---|---|---|---

### SDK Examples ###



 C#




{{< gist groupdocscloud 90da27f305908428852e34cf1ed77ad0 Metadata_CSharp_Get_File_Versions.cs >}}





 Java




{{< gist groupdocscloud 499959a7260c4903f836012226cb2dac Metadata_Java_Get_File_Versions.java >}}




