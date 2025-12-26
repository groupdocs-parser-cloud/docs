---
id: "get-container-items-information"
url: "parser/get-container-items-information"
title: "Get Container Items Information"
productName: "GroupDocs.Parser Cloud"
weight: 3
description: ""
keywords: ""
toc: True
---

This REST API endpoint allows retrieving container items (relative paths) from ZIP archives, documents that contain other attached documents like emails, PDF portfolios, MS Outlook storages. The table below contains the full list of properties.

|Name|Description|Comment
|---|---|---
|FileInfo.FilePath|The path of the document, located in the storage.|Required.
|FileInfo.StorageName|Storage name|It could be omitted for default storage.
|FileInfo.Password|The password to open file|It should be specified only for password-protected documents.
|ContainerItemInfo.RelativePath|The relative path of the container.|Should be specified only for container files like ZIP archives, emails or PDF portfolios.
|ContainerItemInfo.Password|Password for processing password-protected container items.|It should be specified only for password-protected container items.

## Resources

The following GroupDocs.Parser Cloud REST API resource has been used in the [get container items information](https://apireference.groupdocs.cloud/parser/#/Info/Container) example.

```html
HTTP POST ~/container
```

## cURL example

The following example demonstrates how to get document information.

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# The credentials are read from environment variables: $CLIENT_ID and $CLIENT_SECRET.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d 'grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET' \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# cURL example to join several documents into one
# The JWT token is taken from the $JWT_TOKEN environment variable.
curl -v "https://api.groupdocs.cloud/v1.0/parser/container" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
    "FileInfo": {
        "FilePath": "containers/archive/docx.zip",
        "StorageName": ""
    }
}'
```

{{< /tab >}}
{{< tab "Windows PowerShell" >}}

```powershell
# First get JSON Web Token
# Credentials are read from environment variables: $env:CLIENT_ID and $env:CLIENT_SECRET.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to join several documents into one
# The JWT token is taken from the $env:JWT_TOKEN environment variable.
curl.exe -v "https://api.groupdocs.cloud/v1.0/parser/container" `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d "{ 'FileInfo': { 'FilePath': 'containers\archive\docx.zip', 'StorageName': '' } }"
```

{{< /tab >}}
{{< tab "Windows CMD" >}}

```cmd
:: First get JSON Web Token
:: Credentials are read from environment variables: %CLIENT_ID% and %CLIENT_SECRET%.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

:: cURL example to join several documents into one
:: The JWT token is taken from the %JWT_TOKEN% environment variable.
curl -v "https://api.groupdocs.cloud/v1.0/parser/container" ^
  -X POST ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{\"FileInfo\":{\"FilePath\":\"containers\\archive\\docx.zip\",\"StorageName\":\"\"}}"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "containerItems": [
        {
            "name": "four-pages.docx",
            "filePath": "four-pages.docx",
            "directory": "",
            "metadata": {
                "date": "05.03.2019 19:00:00",
                "crc": "213F4CD9"
            }
        },
        {
            "name": "one-page.docx",
            "filePath": "one-page.docx",
            "directory": "",
            "metadata": {
                "date": "05.03.2019 19:00:00",
                "crc": "4927C5D6"
            }
        }
    ]
}
```

{{< /tab >}}
{{< /tabs >}}

## SDK examples

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-parser-cloud) for a complete list of GroupDocs.Parser Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "/parser/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Get_Container_Information.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Get_Container_Information.java >}}
{{< /tab >}}
{{< /tabs >}}
