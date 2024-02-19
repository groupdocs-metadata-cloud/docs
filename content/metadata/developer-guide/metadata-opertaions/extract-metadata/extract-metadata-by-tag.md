---
id: "extract-metadata-by-tag"
url: "metadata/extract-metadata-by-tag"
title: "Extract Metadata By Tag"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
toc: True
---

This REST API allows to extract metadata properties from the document choosing the properties by exact tag and category name.

## cURL example

The following example demonstrates how to extract metadata information from all properties with Created tag.

{{< tabs "example1">}}
{{< tab "Request" >}}

```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications. 
# Kindly place Client Id in client_id and Client Secret in "client_secret" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&client_id#xxxx&client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
  
# cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/metadata" \
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
            "ExactTag": {
                "Name": "Created",
                "Category": "Time"
            }
        }
    }
}"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "properties": [
        {
            "name": "CreateTime",
            "value": "03/22/2016 17:08:00",
            "propertyType": "DateTime",
            "tags": [
                {
                    "name": "Created",
                    "category": "Time"
                },
                {
                    "name": "PropertyTypeBuiltIn",
                    "category": "Document"
                }
            ]
        }
    ]
}
```

{{< /tab >}}
{{< /tabs >}}

## SDK examples

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "/metadata/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Extract_Metadata_By_Tag.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Extract_Metadata_By_Tag.java >}}
{{< /tab >}}
{{< /tabs >}}
