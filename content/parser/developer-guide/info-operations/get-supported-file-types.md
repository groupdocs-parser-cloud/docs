---
id: "get-supported-file-types"
url: "parser/get-supported-file-types"
title: "Get Supported File Types"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

This REST API allows getting a list of all [file formats supported]({{< ref "/parser/getting-started/supported-document-formats.md" >}}) by GroupDocs.Parser Cloud product.

## Resources

The following GroupDocs.Parser Cloud REST API resource has been used in the [get supported file types](https://apireference.groupdocs.cloud/parser/#/Info/GetSupportedFileFormats) example.

```html
HTTP POST ~~/formats
```

## cURL example

The following example demonstrates how to get supported file types.

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# The environment variables CLIENT_ID and CLIENT_SECRET must be set.
curl -v 'https://api.groupdocs.cloud/connect/token' \
  -X POST \
  -d 'grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET' \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -H 'Accept: application/json'

# cURL example to get document information
curl -v 'https://api.groupdocs.cloud/v1.0/parser/formats' \
  -X GET \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H "Authorization: Bearer $JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
# First get JSON Web Token
# Ensure environment variables CLIENT_ID and CLIENT_SECRET are set.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to get document information
curl.exe -v "https://api.groupdocs.cloud/v1.0/parser/formats" `
  -X GET `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
rem First get JSON Web Token
rem Ensure environment variables CLIENT_ID and CLIENT_SECRET are set.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

rem cURL example to get document information
curl -v "https://api.groupdocs.cloud/v1.0/parser/formats" ^
  -X GET ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
  "formats": [    
    {
      "extension": ".doc",
      "fileFormat": "Microsoft Word Document"
    },
    {
      "extension": ".docm",
      "fileFormat": "Word Open XML Macro-Enabled Document"
    },
    {
      "extension": ".docx",
      "fileFormat": "Microsoft Word Open XML Document"
    },
    ...
    {
      "extension": ".xlsx",
      "fileFormat": "Microsoft Excel Open XML Spreadsheet"
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
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Get_Document_File_Types.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Get_Document_File_Types.java >}}
{{< /tab >}}
{{< /tabs >}}
