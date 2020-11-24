---
id: "set-metadata-by-property-name-match-regex"
url: "metadata/set-metadata-by-property-name-match-regex"
title: "Set Metadata By Property Name Match Regex"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
---






# Introduction #

This REST API allows to set document metadata new values choosing properties with names matching the specified regular expression.

## cURL Example ##

The following example demonstrates how to set metadata information to all properties that match regular expression "^NameOfApp.*".


 Request

```html 

* First get JSON Web Token
* Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&client_id#xxxx&client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
   
* cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/metadata/set" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d "{
    "FileInfo": {
        "FilePath": "documents\\input.docx",
        "StorageName": ""
    },
    "Properties": [
        {
            "NewValue": "microsoft word office",
            "Type": "String",
            "SearchCriteria": {
                "NameOptions": {
                    "Value": "^NameOfApp.*",
                    "MatchOptions": {
                        "IsRegex": true
                    }
                }
            }
        }
    ]
}"

 ```


 Response

```html 

{
    "path": "metadata/set_metadata/documents/input_docx/input.docx",
    "url": "https://api.groupdocs.cloud/v1.0/metadata/storage/file/metadata/set_metadata/documents/input_docx/input.docx",
    "setCount": 1
}

 ```



# SDKs #

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "metadata/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

## Set Metadata By Property Name Match Regex ##


 C#



{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Set_Metadata_By_Property_Name_Match_Regex.cs >}}





 Java




{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Set_Metadata_By_Property_Name_Match_Regex.java >}}




