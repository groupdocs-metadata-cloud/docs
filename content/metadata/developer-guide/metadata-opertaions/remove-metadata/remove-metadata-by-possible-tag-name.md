---
id: "remove-metadata-by-possible-tag-name"
url: "metadata/remove-metadata-by-possible-tag-name"
title: "Remove Metadata By Possible Tag Name"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
---






## Introduction ##

This REST API allows to remove metadata properties from the document choosing the properties to remove by approximate or a part of metadata tag name.

This API allows you to specify any part of metadata tag name or tag category name.

### cURL Example ###

The following example demonstrates how to remove metadata properties that have "creator" phrase in theirs tag names.

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
curl -v "https://api.groupdocs.cloud/v1.0/metadata/remove" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d "{
    "FileInfo": {
        "FilePath": "documents\\input.docx",
        "StorageName": ""
    },
    "SearchCriteria": {
        "TagOptions": {
            "PossibleName": "creator"
        }
    }
}"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
    "path": "metadata/remove_metadata/documents/input_docx/input.docx",
    "url": "https://api.groupdocs.cloud/v1.0/metadata/storage/file/metadata/remove_metadata/documents/input_docx/input.docx",
    "removedCount": 1
}
```

{{< /tab >}}
{{< /tabs >}}

## SDKs ##

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "metadata/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

### Remove Metadata By Possible Tag Name ###

{{< tabs tabTotal="2" tabID="2" tabName1="C#" tabName2="Java" >}}
{{< tab tabNum="1" >}}
{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Remove_Metadata_By_Possible_Tag_Name.cs >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Remove_Metadata_By_Possible_Tag_Name.java >}}
{{< /tab >}}
{{< /tabs >}}
