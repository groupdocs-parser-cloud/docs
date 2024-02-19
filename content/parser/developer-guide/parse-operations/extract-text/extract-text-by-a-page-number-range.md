---
id: "extract-text-by-a-page-number-range"
url: "parser/extract-text-by-a-page-number-range"
title: "Extract Text by a Page Number Range"
productName: "GroupDocs.Parser Cloud"
weight: 2
description: ""
keywords: ""
toc: True
---

This REST API allows extracting text from specific pages only by setting pages range. You need to specify **StartPageNumber** and **CountPagesToExtract** parameters besides the basic options.

## Resource

The following GroupDocs.Parser Cloud REST API resource has been used in the [Extract text by a page number](https://apireference.groupdocs.cloud/parser/#/Parse/Text) example.

## cURL example

The following example demonstrates how to extract text by a page number range.

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
    "StartPageNumber": 0,
    "CountPagesToExtract": 4,
    "FileInfo": {
        "FilePath": "pdf\pages-document.pdf",
        "StorageName": ""
    }
}"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "pages": [
        {
            "pageIndex": 0,
            "text": "Text inside bookmark 0\r\n\r\n           Page 0 heading\r\nP a g e  T e x t -  P a g e  0\r\n"
        },
        {
            "pageIndex": 1,
            "text": "Text inside bookmark 1\r\n\r\n           Page 1 heading\r\nP a g e  T e x t -  P a g e  1\r\n"
        },
        {
            "pageIndex": 2,
            "text": "Text inside bookmark 2\r\n\r\n           Page 2 heading\r\nP a g e  T e x t -  P a g e  2\r\n"
        },
        {
            "pageIndex": 3,
            "text": "Text inside bookmark 3\r\n\r\n           Page 3 heading\r\nP a g e  T e x t -  P a g e  3\r\n"
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
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Extract_Text_Page_Number.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Extract_Text_Page_Number.java >}}
{{< /tab >}}
{{< /tabs >}}
