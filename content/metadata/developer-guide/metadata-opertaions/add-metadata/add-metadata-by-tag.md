---
id: "add-metadata-by-tag"
url: "metadata/add-metadata-by-tag"
title: "Add Metadata By Tag"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
toc: True
---

This REST API allows to add metadata properties to the document choosing the right place to add by exact tag and category name.

## cURL example

The following example demonstrates how to add metadata date and time information in all properties that have specified tag.

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
# Get JWT token
curl -v 'https://api.groupdocs.cloud/connect/token' \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -H 'Accept: application/json'

# Join several documents into one
curl -v 'https://api.groupdocs.cloud/v1.0/metadata/add' \
  -X POST \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
    "FileInfo": {
        "FilePath": "documents/input.docx",
        "StorageName": ""
    },
    "Properties": [
        {
            "Value": "02-12-2020 04:41:10",
            "Type": "DateTime",
            "SearchCriteria": {
                "TagOptions": {
                    "ExactTag": {
                        "Name": "Printed",
                        "Category": "Time"
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
# Get JWT token
curl.exe -v 'https://api.groupdocs.cloud/connect/token' `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H 'Content-Type: application/x-www-form-urlencoded' `
  -H 'Accept: application/json'

# Join several documents into one
curl.exe -v 'https://api.groupdocs.cloud/v1.0/metadata/add' `
  -X POST `
  -H 'Content-Type: application/json' `
  -H 'Accept: application/json' `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d '{
    ''FileInfo'': {
        ''FilePath'': ''documents\\input.docx'',
        ''StorageName'': ''''
    },
    ''Properties'': [
        {
            ''Value'': ''02-12-2020 04:41:10'',
            ''Type'': ''DateTime'',
            ''SearchCriteria'': {
                ''TagOptions'': {
                    ''ExactTag'': {
                        ''Name'': ''Printed'',
                        ''Category'': ''Time''
                    }
                }
            }
        }
    ]
}'
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
:: Get JWT token
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

:: Join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/metadata/add" ^
  -X POST ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{\"FileInfo\":{\"FilePath\":\"documents\\input.docx\",\"StorageName\":\"\"},\"Properties\":[{\"Value\":\"02-12-2020 04:41:10\",\"Type\":\"DateTime\",\"SearchCriteria\":{\"TagOptions\":{\"ExactTag\":{\"Name\":\"Printed\",\"Category\":\"Time\"}}}}]}"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "path": "metadata/add_metadata/documents/input_docx/input.docx",
    "url": "https://api.groupdocs.cloud/v1.0/metadata/storage/file/metadata/add_metadata/documents/input_docx/input.docx",
    "addedCount": 1
}
```

{{< /tab >}}
{{< /tabs >}}

## SDK examples

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "/metadata/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Add_Metadata_By_Tag.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Add_Metadata_By_Tag.java >}}
{{< /tab >}}
{{< /tabs >}}
