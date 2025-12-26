---
id: "extract-images-by-a-page-number-range"
url: "parser/extract-images-by-a-page-number-range"
title: "Extract Images by a Page Number Range"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

This REST API allows extracting images from specific pages only by setting pages range. This operation supports only documents with pages. You need to specify **StartPageNumber** and **CountPagesToExtract** parameters besides the basic options.

## Resource

The following GroupDocs.Parser Cloud REST API resource has been used in the [Extract images by a page number](https://apireference.groupdocs.cloud/parser/#/Parse/Images) example.

## cURL example

The following example demonstrates how to extract images by a page number range.

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}
```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# Client Id and Client Secret are provided via environment variables $CLIENT_ID and $CLIENT_SECRET.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/parser/text" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
    "StartPageNumber": 1,
    "CountPagesToExtract": 2,
    "FileInfo": {
        "FilePath": "pdf/template-document.pdf",
        "StorageName": ""
    }
}'
```
{{< /tab >}}

{{< tab "Windows PowerShell" >}}
```powershell
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# Client Id and Client Secret are provided via environment variables $env:CLIENT_ID and $env:CLIENT_SECRET.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to join several documents into one
curl.exe -v "https://api.groupdocs.cloud/v1.0/parser/text" `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d "{
    'StartPageNumber': 1,
    'CountPagesToExtract': 2,
    'FileInfo': {
        'FilePath': 'pdf/template-document.pdf',
        'StorageName': ''
    }
}"
```
{{< /tab >}}

{{< tab "Windows CMD" >}}
```cmd
:: First get JSON Web Token
:: Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
:: Client Id and Client Secret are provided via environment variables %CLIENT_ID% and %CLIENT_SECRET%.
curl -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

:: cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/parser/text" ^
  -X POST ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{\"StartPageNumber\":1,\"CountPagesToExtract\":2,\"FileInfo\":{\"FilePath\":\"pdf/template-document.pdf\",\"StorageName\":\"\"}}"
```
{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "pages": [
        {
            "pageIndex": 1,
            "images": [
                {
                    "path": "parser/images/pdf/template-document_pdf/page_1/image_0.jpeg",
                    "downloadUrl": "https://api.groupdocs.cloud/v1.0/parser/storage/file/parser/images/pdf/template-document_pdf/page_1/image_0.jpeg"
                }
            ]
        },
        {
            "pageIndex": 2,
            "images": [
                {
                    "path": "parser/images/pdf/template-document_pdf/page_2/image_0.jpeg",
                    "downloadUrl": "https://api.groupdocs.cloud/v1.0/parser/storage/file/parser/images/pdf/template-document_pdf/page_2/image_0.jpeg"
                }
            ]
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
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Extract_Images_Page_Number.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Extract_Images_Page_Number.java >}}
{{< /tab >}}
{{< /tabs >}}
