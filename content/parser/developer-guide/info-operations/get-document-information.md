---
id: "get-document-information"
url: "parser/get-document-information"
title: "Get Document Information"
productName: "GroupDocs.Parser Cloud"
weight: 2
description: ""
keywords: ""
toc: True
---

This REST API allows obtaining basic information about the document. The endpoint accepts the document storage path as input payload. Here is the list of properties that can be obtained for a document:

* Document file extension;
* Document size in bytes;
* Document file format;
* Document page count.

The table below contains the full list of properties.

|Name|Description|Comment
|---|---|---
|FileInfo.FilePath|The path of the document, located in the storage.|Required.
|FileInfo.StorageName|Storage name|It could be omitted for default storage.
|FileInfo.Password|The password to open file|It should be specified only for password-protected documents.
|ContainerItemInfo.RelativePath|The relative path of the container.|Should be specified only for container files like ZIP archives, emails or PDF portfolios.
|ContainerItemInfo.Password|Password for processing password-protected container items.|It should be specified only for password-protected container items.

## Resources

The following GroupDocs.Parser Cloud REST API resource has been used in the [Get Document Information](https://apireference.groupdocs.cloud/parser/#/Info/GetInfo) example.

Resource URI

```html
HTTP POST ~/info
```

## cURL example

The following example demonstrates how to get document information.

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# The client credentials are read from environment variables $CLIENT_ID and $CLIENT_SECRET.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d 'grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET' \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# cURL example to get document information
# The JWT token is read from the environment variable $JWT_TOKEN.
curl -v "https://api.groupdocs.cloud/v1.0/parser/info" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{ "FilePath": "/words/four-pages.docx" }'
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# The client credentials are read from environment variables $env:CLIENT_ID and $env:CLIENT_SECRET.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to get document information
# The JWT token is read from the environment variable $env:JWT_TOKEN.
curl.exe -v "https://api.groupdocs.cloud/v1.0/parser/info" `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d "`n{ 'FilePath': '/words/four-pages.docx' }`n"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
REM First get JSON Web Token
REM Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
REM The client credentials are read from environment variables %CLIENT_ID% and %CLIENT_SECRET%.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

REM cURL example to get document information
REM The JWT token is read from the environment variable %JWT_TOKEN%.
curl -v "https://api.groupdocs.cloud/v1.0/parser/info" ^
  -X POST ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{\"FilePath\": \"/words/four-pages.docx\"}"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "fileType": {
        "fileFormat": "Microsoft Word Open XML Document",
        "extension": ".docx"
    },
    "size": 8651,
    "pageCount": 4
}
```

{{< /tab >}}
{{< /tabs >}}

## SDK examples

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-parser-cloud) for a complete list of GroupDocs.Parser Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "/parser/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Get_Document_Information.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Get_Document_Information.java >}}
{{< /tab >}}
{{< /tabs >}}
