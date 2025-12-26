---
id: "remove-metadata-by-possible-tag-name"
url: "metadata/remove-metadata-by-possible-tag-name"
title: "Remove Metadata By Possible Tag Name"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
toc: True
---

This REST API allows to remove metadata properties from the document choosing the properties to remove by approximate or a part of metadata tag name.

This API allows you to specify any part of metadata tag name or tag category name.

## cURL example

The following example demonstrates how to remove metadata properties that have "creator" phrase in theirs tag names.

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}
```bash
# Get JSON Web Token
# Ensure CLIENT_ID and CLIENT_SECRET env variables are set.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# Example: remove metadata from a document
curl -v "https://api.groupdocs.cloud/v1.0/metadata/remove" \
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
# Get JSON Web Token
# Ensure CLIENT_ID and CLIENT_SECRET environment variables are set.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# Example: remove metadata from a document
curl.exe -v "https://api.groupdocs.cloud/v1.0/metadata/remove" `
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
:: Get JSON Web Token
:: Ensure CLIENT_ID and CLIENT_SECRET environment variables are set.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

:: Example: remove metadata from a document
curl -v "https://api.groupdocs.cloud/v1.0/metadata/remove" ^
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
    "path": "metadata/remove_metadata/documents/input_docx/input.docx",
    "url": "https://api.groupdocs.cloud/v1.0/metadata/storage/file/metadata/remove_metadata/documents/input_docx/input.docx",
    "removedCount": 1
}
```

{{< /tab >}}
{{< /tabs >}}

## SDK examples

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "/metadata/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Remove_Metadata_By_Possible_Tag_Name.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Remove_Metadata_By_Possible_Tag_Name.java >}}
{{< /tab >}}
{{< /tabs >}}
