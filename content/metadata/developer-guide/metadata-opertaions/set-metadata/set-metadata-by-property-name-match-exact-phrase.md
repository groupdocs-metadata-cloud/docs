---
id: "set-metadata-by-property-name-match-exact-phrase"
url: "metadata/set-metadata-by-property-name-match-exact-phrase"
title: "Set Metadata By Property Name Match Exact Phrase"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
---






## Introduction ##

This REST API allows to set document metadata new values choosing properties with specified name.

### cURL Example ###

The following example demonstrates how to set metadata information to all properties with the exact same name as specified.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
# First get JSON Web Token
# Please get your App Key and App SID from https://dashboard.groupdocs.cloud/#/apps. 
# Kindly place App Key in "client_secret" and App SID in "client_id" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&client_id#xxxx&client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
   
# cURL example to join several documents into one
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
                    "Value": "NameOfApplication",
                    "MatchOptions": {
                        "ExactPhrase": true
                    }
                }
            }
        }
    ]
}"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
    "path": "metadata/set_metadata/documents/input_docx/input.docx",
    "url": "https://api.groupdocs.cloud/v1.0/metadata/storage/file/metadata/set_metadata/documents/input_docx/input.docx",
    "setCount": 1
}
```

{{< /tab >}}
{{< /tabs >}}

## SDKs ##

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "metadata/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

### Set Metadata By Property Name Match Exact Phrase ###

{{< tabs tabTotal="2" tabID="2" tabName1="C#" tabName2="Java" >}}
{{< tab tabNum="1" >}}
{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Set_Metadata_By_Property_Name_Match_Exact_Phrase.cs >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Set_Metadata_By_Property_Name_Match_Exact_Phrase.java >}}
{{< /tab >}}
{{< /tabs >}}
