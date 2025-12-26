---
id: "get-metadata-tags-information"
url: "metadata/get-metadata-tags-information"
title: "Get Metadata Tags Information"
productName: "GroupDocs.Metadata Cloud"
description: ""
keywords: ""
toc: True
---

This REST API allows to obtain tags and properties information from document metadata. Endpoint accepts document storage path as input payload.

Operation traverses whole metadata tree packages and retrieve properties within the package.

The table below contains the full list of properties.

|Name|Description|Comment
|---|---|---
|FileInfo.FilePath|The path of the document, located in the storage.|Required.
|FileInfo.StorageName|Storage name|Could be omitted for default storage.

## Resource URI

```html
HTTP POST ~/metadata/tags
```

[Swagger UI](https://apireference.groupdocs.cloud/metadata/#/Info/Tags) lets you call this REST API directly from the browser.

## cURL example

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
# Get JSON Web Token
# Ensure CLIENT_ID and CLIENT_SECRET are set as environment variables.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# Get document information (metadata tags)
curl -v "https://api.groupdocs.cloud/v1.0/metadata/info/tags" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{ "FilePath": "/documents/input.docx" }'
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
# Get JSON Web Token
# Ensure CLIENT_ID and CLIENT_SECRET are set as environment variables.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# Get document information (metadata tags)
curl.exe -v "https://api.groupdocs.cloud/v1.0/metadata/info/tags" `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d '{ "FilePath": "/documents/input.docx" }'
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
rem Get JSON Web Token
rem Ensure CLIENT_ID and CLIENT_SECRET are set as environment variables.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

rem Get document information (metadata tags)
curl -v "https://api.groupdocs.cloud/v1.0/metadata/info/tags" ^
  -X POST ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{ \"FilePath\": \"/documents/input.docx\" }"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
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
```

{{< /tab >}}
{{< /tabs >}}

## SDK examples

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-metadata-cloud) for a complete list of GroupDocs.Metadata Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "/metadata/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 3c211b41ef72c2070064a8ad93f14fdc Metadata_CSharp_Get_Metadata_Tags_Information.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud b613728b13cd4a7c5e1d585361108181 Metadata_Java_Get_Metadata_Tags_Information.java >}}
{{< /tab >}}
{{< /tabs >}}
