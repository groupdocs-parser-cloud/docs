---
id: "extract-text-from-a-document-inside-a-container"
url: "parser/extract-text-from-a-document-inside-a-container"
title: "Extract Text From a Document Inside a Container"
productName: "GroupDocs.Parser Cloud"
weight: 4
description: ""
keywords: ""
toc: True
---

This REST API allows extracting text from a document placed in a container like ZIP archive, emails, PDF portfolios, etc. by specifying **ContainerItemInfo** parameter

## Resource

The following GroupDocs.Parser Cloud REST API resource has been used in the [Extract Text From a Document Inside a Container](https://apireference.groupdocs.cloud/parser/#/Parse/Text) example.

## cURL example

The following example demonstrates how to extract text from a container item.

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# The credentials are read from environment variables.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v2.0/conversion" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
    "FileInfo": {
        "FilePath": "pdf/PDF with attachements.pdf",
        "StorageName": "",
        "Password": "password"
    },
    "ContainerItemInfo": {
        "RelativePath": "document.pdf",
        "Password": "password"
    }
}'
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# The credentials are read from environment variables.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to join several documents into one
curl.exe -v "https://api.groupdocs.cloud/v2.0/conversion" `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d "{ 'FileInfo': { 'FilePath': 'pdf/PDF with attachements.pdf', 'StorageName': '', 'Password': 'password' }, 'ContainerItemInfo': { 'RelativePath': 'document.pdf', 'Password': 'password' } }"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
:: First get JSON Web Token
:: Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
:: The credentials are read from environment variables.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

:: cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v2.0/conversion" ^
  -X POST ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{\"FileInfo\":{\"FilePath\":\"pdf/PDF with attachements.pdf\",\"StorageName\":\"\",\"Password\":\"password\"},\"ContainerItemInfo\":{\"RelativePath\":\"document.pdf\",\"Password\":\"password\"}}"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "text": "Text inside bookmark 0\r\n\r\n           Page 0 heading\r\nP a g e  T e x t -  P a g e  0\r\nText inside bookmark 1\r\n\r\n           Page 1 heading\r\nP a g e  T e x t -  P a g e  1\r\nText inside bookmark 2\r\n\r\n           Page 2 heading\r\nP a g e  T e x t -  P a g e  2\r\nText inside bookmark 3\r\n\r\n           Page 3 heading\r\nP a g e  T e x t -  P a g e  3\r\nField\r\nRelatedField2 RelatedText2\r\n REGEX TEXT 123\r\nTABLE\r\n    Cell\r\n                         Cell 12\r\n\r\n\r\n\r\n"
}
```

{{< /tab >}}
{{< /tabs >}}

## SDK examples

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-parser-cloud) for a complete list of GroupDocs.Parser Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "/parser/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Extract_Text_Document_Container.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Extract_Text_Document_Container.java >}}
{{< /tab >}}
{{< /tabs >}}
