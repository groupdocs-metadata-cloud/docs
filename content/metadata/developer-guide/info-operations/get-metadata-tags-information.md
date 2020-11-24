---
id: "get-metadata-tags-information"
url: "metadata/get-metadata-tags-information"
title: "Get Metadata Tags Information"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
---





# Introduction #

This REST API allows to obtain tags and properties information from document metadata. Endpoint accepts document storage path as input payload.

Operation traverses whole metadata tree packages and retrieve properties within the package. 

The table below contains the full list of properties.


|#
|---
Name
|#
Description
|#
Comment

|FileInfo.FilePath|The path of the document, located in the storage.|Required.
|FileInfo.StorageName|Storage name|Could be omitted for default storage.

## Resource URI ##

```html 

HTTP POST ~/metadata/tags

 ```

[Swagger UI](https://apireference.groupdocs.cloud/metadata/#/Info/Tags) lets you call this REST API directly from the browser. 

## cURL Example ##


 Request
* First get JSON Web Token
* Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&client_id#xxxx&client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
   
* cURL example to get document information
curl -v "https://api.groupdocs.cloud/v1.0/metadata/info/tags" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ FilePath: '/documents/input.docx' }"


 Response
{
    "rootPackage": {
        "packageName": "Root",
        "packageProperties": [],
        "innerPackages": [
            {
                "packageName": "FileFormat",
                "packageProperties": [
                    {
                        "name": "FileFormat",
                        "value": null,
                        "propertyType": "Empty",
                        "accessLevel": "Read",
                        "tags": [
                            {
                                "name": "FileFormat",
                                "category": "Content"
                            }
                        ]
                    },
                    {
                        "name": "MimeType",
                        "value": null,
                        "propertyType": "Empty",
                        "accessLevel": "Read",
                        "tags": [
                            {
                                "name": "FileFormat",
                                "category": "Content"
                            }
                        ]
                    },
                    {
                        "name": "WordProcessingFileFormat",
                        "value": null,
                        "propertyType": "Empty",
                        "accessLevel": "Read",
                        "tags": [
                            {
                                "name": "FileFormat",
                                "category": "Content"
                            }
                        ]
                    }
                ],
                "innerPackages": []
            },
...            
        ]
    }
}



# SDKs #

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "metadata/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.


## Get Metadata Tags Information ##


 C#



{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Get_Metadata_Tags_Information.cs >}}





 Java




{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Get_Metadata_Tags_Information.java >}}




