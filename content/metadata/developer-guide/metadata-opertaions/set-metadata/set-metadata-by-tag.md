---
id: "set-metadata-by-tag"
url: "metadata/set-metadata-by-tag"
title: "Set Metadata By Tag"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
toc: True
---

This REST API allows to set document metadata new values choosing properties by exact tag and category name.

## cURL example

The following example demonstrates how to set metadata information to all properties with the "Creator" tag name.

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# Kindly place Client Id in CLIENT_ID and Client Secret in CLIENT_SECRET environment variables.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# cURL example to set metadata for a document
curl -v "https://api.groupdocs.cloud/v1.0/metadata/set" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
    "FileInfo": {
        "FilePath": "documents\\input.docx",
        "StorageName": ""
    },
    "Properties": [
        {
            "NewValue": "NewAuthor",
            "Type": "String",
            "SearchCriteria": {
                "TagOptions": {
                    "ExactTag": {
                        "Name": "Creator",
                        "Category": "Person"
                    }
                }
            }
        }
    ]
}'
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# Ensure they are stored in $env:CLIENT_ID and $env:CLIENT_SECRET.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to set metadata for a document
curl.exe -v "https://api.groupdocs.cloud/v1.0/metadata/set" `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d "{
    'FileInfo': {
        'FilePath': 'documents\\input.docx',
        'StorageName': ''
    },
    'Properties': [
        {
            'NewValue': 'NewAuthor',
            'Type': 'String',
            'SearchCriteria': {
                'TagOptions': {
                    'ExactTag': {
                        'Name': 'Creator',
                        'Category': 'Person'
                    }
                }
            }
        }
    ]
}"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
:: First get JSON Web Token
:: Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
:: Ensure they are stored in %CLIENT_ID% and %CLIENT_SECRET%.
curl -v "https://api.groupdocs.cloud/connect/token" ^ 
  -X POST ^ 
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^ 
  -H "Content-Type: application/x-www-form-urlencoded" ^ 
  -H "Accept: application/json"

:: cURL example to set metadata for a document
curl -v "https://api.groupdocs.cloud/v1.0/metadata/set" ^ 
  -X POST ^ 
  -H "Content-Type: application/json" ^ 
  -H "Accept: application/json" ^ 
  -H "Authorization: Bearer %JWT_TOKEN%" ^ 
  -d "{\"FileInfo\":{\"FilePath\":\"documents\\input.docx\",\"StorageName\":\"\"},\"Properties\":[{\"NewValue\":\"NewAuthor\",\"Type\":\"String\",\"SearchCriteria\":{\"TagOptions\":{\"ExactTag\":{\"Name\":\"Creator\",\"Category\":\"Person\"}}}}]}"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "path": "metadata/set_metadata/documents/input_docx/input.docx",
    "url": "https://api.groupdocs.cloud/v1.0/metadata/storage/file/metadata/set_metadata/documents/input_docx/input.docx",
    "setCount": 1
}
```

{{< /tab >}}
{{< /tabs >}}

## SDK examples

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "/metadata/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Set_Metadata_By_Tag.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Set_Metadata_By_Tag.java >}}
{{< /tab >}}
{{< /tabs >}}
