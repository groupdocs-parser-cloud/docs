---
id: "extract-text-from-the-whole-document"
url: "parser/extract-text-from-the-whole-document"
title: "Extract Text From The Whole Document"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
---






## Introduction ##

This REST API allows extracting text from the whole document by default. You need to specify only the file information parameters.

### Resource ###

The following GroupDocs.Parser Cloud REST API resource has been used in the [extract text from the whole document](https://apireference.groupdocs.cloud/parser/#/Parse/Text) example.

### cURL Example ###

The following example demonstrates how to extract text from the whole document.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# Kindly place Client Id in "client_id" and Client Secret in "client_secret" argument.
curl -v "https://api.groupdocs.cloud/connect/token" \
-X POST \
-d "grant_type#client_credentials&#x26;client_id#xxxx&#x26;client_secret#xxxx" \
-H "Content-Type: application/x-www-form-urlencoded" \
-H "Accept: application/json"
  
$ cURL example to join several documents into one
curl -v "https://api.groupdocs.cloud/v1.0/parser/text" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer 
<jwt token>" \
-d "{
        "FileInfo": {
            "FilePath": "words\docx\document.docx",
    }
}"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
    "text": "First Page\r\r\f"
}
```

{{< /tab >}}
{{< /tabs >}}

### SDKs ###

Using an SDK (API client) is the quickest way for a developer to speed up the development. An SDK takes care of a lot of low-level details of making requests and handling responses and lets you focus on writing code specific to your particular project. Check out our [GitHub repository](https://github.com/groupdocs-parser-cloud) for a complete list of GroupDocs.Parser Cloud SDKs along with working examples, to get you started in no time. Please check [Available SDKs]({{< ref "parser/getting-started/available-sdks.md" >}}) article to learn how to add an SDK to your project.

#### Extract Text From The Whole Document Examples ####

{{< tabs tabTotal="2" tabID="2" tabName1="C#" tabName2="Java" >}}
{{< tab tabNum="1" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Extract_Text_Whole_Document.cs >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Extract_Text_Whole_Document.java >}}
{{< /tab >}}
{{< /tabs >}}
