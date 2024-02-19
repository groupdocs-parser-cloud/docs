---
id: "get-template"
url: "parser/get-template"
title: "Get Template"
productName: "GroupDocs.Parser Cloud"
weight: 2
description: ""
keywords: ""
toc: True
---

This REST API provides the functionality to retrieve templates that are used in Parse endpoint. Simply get the API response and use it as a template parameter in Parse by the Template method. The table below contains the full list of properties.

|Name|Description|Comment
|---|---|---
|TemplatePath|The path of the template, located in the storage.|**Required.**
|FileInfo.StorageName|Storage name|It could be omitted for default storage.

## Resource

The following GroupDocs.Parser Cloud REST API resource has been used in the [Get Template](https://apireference.groupdocs.cloud/parser/#/Template/GetTemplate) example.

## cURL example

The following example demonstrates how to Get a Template.

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
curl -v "https://api.groupdocs.cloud/v1.0/parser/template" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer 
<jwt token>" \
-d "{
    "TemplatePath": "templates/template_1.json"
}"
```

{{< /tab >}}
{{< tab "Response" >}}

Response will contain raw json template

```json
{
    "fields": [
        {
            "fieldName": "Address",
            "fieldPosition": {
                "fieldPositionType": "Fixed",
                "rectangle": {
                    "position": {
                        "x": 13.0,
                        "y": 35.0
                    },
                    "size": {
                        "height": 10.0,
                        "width": 100.0
                    }
                },
                "matchCase": false,
                "isLeftLinked": false,
                "isRightLinked": false,
                "isTopLinked": false,
                "isBottomLinked": false,
                "autoScale": false
            }
        },
        {
            "fieldName": "Company",
            "fieldPosition": {
                "fieldPositionType": "Linked",
                "matchCase": false,
                "linkedFieldName": "Address",
                "isLeftLinked": false,
                "isRightLinked": false,
                "isTopLinked": false,
                "isBottomLinked": true,
                "searchArea": {
                    "height": 15.0,
                    "width": 100.0
                },
                "autoScale": true
            }
        }
    ],
    "tables": [
        {
            "tableName": "Totals",
            "detectorParameters": {
                "rectangle": {
                    "position": {
                        "x": 300.0,
                        "y": 385.0
                    },
                    "size": {
                        "height": 220.0,
                        "width": 65.0
                    }
                }
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
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Get_Template.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Get_Template.java >}}
{{< /tab >}}
{{< /tabs >}}
