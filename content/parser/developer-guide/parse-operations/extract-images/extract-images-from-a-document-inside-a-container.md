---
id: "extract-images-from-a-document-inside-a-container"
url: "parser/extract-images-from-a-document-inside-a-container"
title: "Extract Images from a Document Inside a Container"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

This REST API allows extracting images from a document placed in a container like ZIP archive, emails, PDF portfolios, etc. by specifying the **ContainerItemInfo** parameter.

## Resource

The following GroupDocs.Parser Cloud REST API resource has been used in the [Extract images from a document inside a container](https://apireference.groupdocs.cloud/parser/#/Parse/Images) example.

## cURL example

The following example demonstrates how to extract images from a container item.

{{< tabs "example1">}}
{{< tab "Request" >}}

```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&#x26;client_id#xxxx&#x26;client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
   
# cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/parser/text" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer 
<jwt token>" \
-d "{
    "StartPageNumber": 1,
    "CountPagesToExtract": 2,
    "FileInfo": {
        "FilePath": "pdf\PDF with attachements.pdf",
        "StorageName": "",
        "Password": "password"
    },
    "ContainerItemInfo": {
        "RelativePath": "template-document.pdf"
    }
}"
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
                    "path": "parser/images/template-document_pdf/page_1/image_0.jpeg",
                    "downloadUrl": "https://api.groupdocs.cloud/v1.0/parser/storage/file/parser/images/template-document_pdf/page_1/image_0.jpeg"
                }
            ]
        },
        {
            "pageIndex": 2,
            "images": [
                {
                    "path": "parser/images/template-document_pdf/page_2/image_0.jpeg",
                    "downloadUrl": "https://api.groupdocs.cloud/v1.0/parser/storage/file/parser/images/template-document_pdf/page_2/image_0.jpeg"
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
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Extract_Images_Document_Container.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Extract_Images_Document_Container.java >}}
{{< /tab >}}
{{< /tabs >}}
