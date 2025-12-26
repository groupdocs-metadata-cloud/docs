---
id: "extract-metadata-by-possible-tag-name"
url: "metadata/extract-metadata-by-possible-tag-name"
title: "Extract Metadata By Possible Tag Name"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
toc: True
---

This REST API allows to extract metadata properties from the document choosing the properties to extract by approximate or a part of metadata tag name.

This API allows you to specify any part of metadata tag name or tag category name.

## cURL example

The following example demonstrates how to extract metadata creator information from all properties that have particular string phrase in theirs tag names.

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# Place Client Id in $CLIENT_ID and Client Secret in $CLIENT_SECRET.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/metadata" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
    "FileInfo": {
        "FilePath": "documents/input.docx",
        "StorageName": ""
    },
    "SearchCriteria": {
        "TagOptions": {
            "PossibleName": "creator"
        }
    }
}'
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# Place Client Id in $env:CLIENT_ID and Client Secret in $env:CLIENT_SECRET.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to join several documents into one
curl.exe -v "https://api.groupdocs.cloud/v1.0/metadata" `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d "{
    'FileInfo': {
        'FilePath': 'documents\\input.docx',
        'StorageName': ''
    },
    'SearchCriteria': {
        'TagOptions': {
            'PossibleName': 'creator'
        }
    }
}"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
rem First get JSON Web Token
rem Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
rem Place Client Id in %CLIENT_ID% and Client Secret in %CLIENT_SECRET%.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

rem cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/metadata" ^
  -X POST ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{\"FileInfo\":{\"FilePath\":\"documents\\input.docx\",\"StorageName\":\"\"},\"SearchCriteria\":{\"TagOptions\":{\"PossibleName\":\"creator\"}}}"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "properties": [
        {
            "name": "Author",
            "value": "Prokofjev Igor",
            "propertyType": "String",
            "tags": [
                {
                    "name": "Creator",
                    "category": "Person"
                },
                {
                    "name": "PropertyTypeBuiltIn",
                    "category": "Document"
                }
            ]
        },
        {
            "name": "dc:creator",
            "value": "Prokofjev Igor",
            "propertyType": "String",
            "tags": [
                {
                    "name": "Creator",
                    "category": "Person"
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
{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Extract_metadata_by_possible_tag_name.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Extract_metadata_by_possible_tag_name.java >}}
{{< /tab >}}
{{< /tabs >}}
