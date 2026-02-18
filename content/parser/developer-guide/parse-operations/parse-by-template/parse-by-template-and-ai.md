---
id: "parse-by-ai"
url: "parser/parse-by-template-and-ai"
title: "Parse by Template And AI"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

This REST API allows us to extract document's fields defined in a template object passed as a method parameter by using LLM.

The following example demonstrates how to extract data from a source document by a user-defined template and modern well updated LLM.

## Resource

The following GroupDocs.Parser Cloud REST API resource has been used in the [AI Parse](https://reference.groupdocs.cloud/parser/#/Parse/AIParse) example.

## cURL example

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}
```bash
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# The client credentials are taken from environment variables.
curl -v "https://api.groupdocs.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=$CLIENT_ID&client_secret=$CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"

# cURL example to parse a document using LLM
curl -v "https://api.groupdocs.cloud/v1.0/parser/aiparse" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer $JWT_TOKEN" \
  -d '{
    "FileInfo": {
        "FilePath": "Invoice.xlsx"
    },
    "Template": {
                "InvoiceNum": "",
                "Date":  "",
                "Email": ""
            }
}'
```
{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
# First get JSON Web Token
# Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
# The client credentials are taken from environment variables.
curl.exe -v "https://api.groupdocs.cloud/connect/token" `
  -X POST `
  -d "grant_type=client_credentials&client_id=$env:CLIENT_ID&client_secret=$env:CLIENT_SECRET" `
  -H "Content-Type: application/x-www-form-urlencoded" `
  -H "Accept: application/json"

# cURL example to parse a document using LLM
curl.exe -v "https://api.groupdocs.cloud/v1.0/parser/aiparse" `
  -X POST `
  -H "Content-Type: application/json" `
  -H "Accept: application/json" `
  -H "Authorization: Bearer $env:JWT_TOKEN" `
  -d '{
    "FileInfo": {
        "FilePath": "Invoice.xlsx"
    },
    "Template": {
                "InvoiceNum": "",
                "Date":  "",
                "Email": ""
            }
}'
```
{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
REM First get JSON Web Token
REM Please get your Client Id and Client Secret from https://dashboard.groupdocs.cloud/applications.
REM The client credentials are taken from environment variables.
curl.exe -v "https://api.groupdocs.cloud/connect/token" ^
  -X POST ^
  -d "grant_type=client_credentials&client_id=%CLIENT_ID%&client_secret=%CLIENT_SECRET%" ^
  -H "Content-Type: application/x-www-form-urlencoded" ^
  -H "Accept: application/json"

REM cURL example to parse a document using LLM
curl.exe -v "https://api.groupdocs.cloud/v1.0/parser/aiparse" ^
  -X POST ^
  -H "Content-Type: application/json" ^
  -H "Accept: application/json" ^
  -H "Authorization: Bearer %JWT_TOKEN%" ^
  -d "{\"FileInfo\":{\"FilePath\":\"Invoice.xlsx\"},\"Template\":{\"InvoiceNum\":\"\",\"Date\":\"\",\"Email\":\"\"}}"
```
{{< /tab >}}
{{< tab "Response" >}}

```json
{
    "InvoiceNum": "IL220303/36",
    "Date":  "01/22/2025 00:00:00",
    "Email": "purchase@aspose.com"
}
```

{{< /tab >}}
{{< /tabs >}}

## SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Parser API](https://apireference.groupdocs.cloud/parser/#/Parse) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example2">}}
{{< tab "C#" >}}
```csharp
  string MyAppKey = ""; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  string MyAppSid = ""; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud
    
  var configuration = new Configuration(MyAppSid, MyAppKey);    
  var apiInstance = new ParseApi(configuration);
  var options = new AIParseOptions
  {
      FileInfo = "Invoice.xlsx",
      Template = new
      {
          InvoiceNum = "",
          Date = "",
          Email = ""
      }
  };
  var request = new AIParseRequest(options);
  var result = ParseApi.AIParse(request);
```
{{< /tab >}}
{{< tab "Java" >}}
```java
  // For complete examples and data files, please go to https://github.com/groupdocs-parser-cloud/groupdocs-parser-cloud-java-samples
  String MyAppKey = ""; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud
  String MyAppSid = ""; // Get AppKey and AppSID from https://dashboard.groupdocs.cloud
    
  Configuration configuration = new Configuration(MyAppSid, MyAppKey);
  ParseApi apiInstance = new ParseApi(configuration);
  AIParseOptions options = new AIParseOptions();
  FileInfo fileInfo = new FileInfo();
  fileInfo.setFilePath("Invoice.xlsx");
  options.setFileInfo(fileInfo);
  AIParseTemplate template = new AIParseTemplate();
  options.setTemplate(template);
  AIParseRequest request = new AIParseRequest(options);

  Object result = parseApi.aIParse(request);
```
{{< /tab >}}
{{< /tabs >}}
