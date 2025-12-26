---
id: "extract-text-from-the-whole-document"
url: "parser/extract-text-from-the-whole-document"
title: "Extract Text From The Whole Document"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

This REST API allows extracting text from the whole document by default. You need to specify only the file information parameters.

## Resource

The following GroupDocs.Parser Cloud REST API resource has been used in the [extract text from the whole document](https://apireference.groupdocs.cloud/parser/#/Parse/Text) example.

## cURL example

The following example demonstrates how to extract text from the whole document.

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

# Join several documents into one (example)
curl -v "https://api.groupdocs.cloud/v1.0/parser/text" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
        "FileInfo": {
            "FilePath": "words/docx/document.docx"
        }
      }'
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
# Get JSON Web Token
# Set environment variables CLIENT_ID, CLIENT_SECRET, JWT_TOKEN in the session.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# Join several documents into one (example)
curl.exe -v "https://api.groupdocs.cloud/v1.0/parser/text" `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d "{
        'FileInfo': {
            'FilePath': 'words/docx/document.docx'
        }
      }"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
:: Get JSON Web Token
:: Ensure CLIENT_ID and CLIENT_SECRET are defined in the environment.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

:: Join several documents into one (example)
curl -v "https://api.groupdocs.cloud/v1.0/parser/text" ^
  -X POST ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{\"FileInfo\":{\"FilePath\":\"words\\docx\\document.docx\"}}"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "text": "First Page\r\r\f"
}
```

{{< /tab >}}
{{< /tabs >}}

## SDK examples

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-parser-cloud) for a complete list of GroupDocs.Parser Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "/parser/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Extract_Text_Whole_Document.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Extract_Text_Whole_Document.java >}}
{{< /tab >}}
{{< /tabs >}}
