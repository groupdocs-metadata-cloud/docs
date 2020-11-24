---
id: "get-supported-file-types"
url: "metadata/get-supported-file-types"
title: "Get Supported File Types"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
---





# Introduction #

This REST API allows to get list of all [file formats supported ]({{< ref "metadata/developer-guide/info-operations/get-supported-file-types.md" >}})by GroupDocs.Metadata Cloud product.

## Resource URI ##

```html 

HTTP POST ~/formats

 ```

[Swagger UI](https://apireference.groupdocs.cloud/metadata/#/Info/GetSupportedFileFormats) lets you call this REST API directly from the browser.

## cURL Example ##



 Request

```html 

* First get JSON Web Token
* Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&client_id#xxxx&client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
  
* cURL example to get document information
curl -v "https://api.groupdocs.cloud/v1.0/metadata/formats" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

 ```


 Response

```html 

{
  "formats": [ 
    {
      "extension": ".doc",
      "fileFormat": "Microsoft Word 97 - 2007 Document"
    },
    {
      "extension": ".docm",
      "fileFormat": "Office Open XML WordprocessingML Macro-Enabled Document"
    },
    {
      "extension": ".docx",
      "fileFormat": "Office Open XML WordprocessingML Document"
    },
   ...
    {
      "extension": ".xlsx",
      "fileFormat": "OOXML 2007-2010"
    }
  ]
}

 ```



# SDKs #

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "metadata/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

## SDK Examples ##


 C#



{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Get_Supported_File_Types.cs >}}





 Java




{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Get_Supported_File_Types.java >}}




