---
id: "working-with-files"
url: "parser/working-with-files"
title: "Working With Files"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

## Download File API

This API allows you to download a file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

### API Explorer

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Download a File API](https://apireference.groupdocs.cloud/parser/#/File/DownloadFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|**Path**|Path of the file including file name and extension e.g. /Folder1/file.ext</br>Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|versionId|File version id

### cURL example

{{< tabs "example1">}}
{{< tab "Request" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/parser/storage/file/one-page.docx?storageName#MyStorage" \
-H  "accept: multipart/form-data" \
-H  "authorization: Bearer [Access Token]"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [File API](https://apireference.groupdocs.cloud/parser/#/) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Download_File.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Download_File.java >}}
{{< /tab >}}
{{< /tabs >}}

## Upload File API

This API allows you to upload files to the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### API Explorer

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Upload a File API](https://apireference.groupdocs.cloud/parser/#/File/UploadFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Request Body parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext</br>Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|File|File content

### cURL example

{{< tabs "example3">}}
{{< tab "Request" >}}

```bash
curl -X POST "https://api.groupdocs.cloud/v1.0/parser/storage/file/parserdocs%2Fone-page2.docx?storageName#MyStorage" \
-H  "accept: application/json" \
-H  "authorization: Bearer [Access Token]"
```

{{< /tab >}}
{{< tab "Response" >}}
Http status code: 200 (Returns OK and list of errors, which is empty if success.)

```json
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2019-02-27T06:10:08.884Z"
      }
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [File API](https://apireference.groupdocs.cloud/parser/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "example4">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Upload_File.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Upload_File.java >}}
{{< /tab >}}
{{< /tabs >}}

## Delete File API

This API allows you to delete a specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### API Explorer

[GroupDocs.Parser for Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Delete a File](https://apireference.groupdocs.cloud/parser/#/File/DeleteFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs exposes.

### Request parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext</br>Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|versionId|File version id

### cURL example

{{< tabs "example5">}}
{{< tab "Request" >}}

```bash
curl -X DELETE "https://api.groupdocs.cloud/v1.0/parser/storage/file/parserdocs1%2Fone-page1.docx?storageName#MyStorage" \
-H  "accept: application/json" \
-H  "authorization: Bearer [Access Token]"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [File API](https://apireference.groupdocs.cloud/parser/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "example6">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Delete_File.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Delete_File.java >}}
{{< /tab >}}
{{< /tabs >}}

## File Copy API

This API allows you to copy a specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### API Explorer

[GroupDocs.Parser for Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Copy File](https://apireference.groupdocs.cloud/parser/#/File/CopyFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|**srcPath**|Path of the source file including file name and extension e.g. /Folder1/file.ext</br>Required. Can be passed as a query string parameter or as part of the URL
|**destPath**|Path of the destination file. Required.
|srcStorageName|Name of the storage of source file. If not set, then default storage used
|destStorageName|Name of the storage of destination file. If not set, then default storage used
|versionId|Source file version id

### cURL example

{{< tabs "example7">}}
{{< tab "Request" >}}

```bash
curl -X PUT "https://api.groupdocs.cloud/v1.0/parser/storage/file/copy/parserdocs%2Fone-page1.docx?destPath#parserdocs1%2Fone-page1.docx'&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" \
-H  "accept: application/json" \
-H  "authorization: Bearer [Access Token]"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [File API](https://apireference.groupdocs.cloud/parser/#/File) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example8">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Copy_File.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Copy_File.java >}}
{{< /tab >}}
{{< /tabs >}}

## File Move API

This API allows you to copy a specific file from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud/).

### API Explorer

[GroupDocs.Parser for Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Move File](https://apireference.groupdocs.cloud/parser/#/File/MoveFile) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|**srcPath**|Path of the source file including file name and extension e.g. /Folder1/file.ext</br>Required. Can be passed as a query string parameter or as part of the URL
|**destPath**|Path of the destination file. Required.
|srcStorageName|Name of the storage of source file. If not set, then default storage used
|destStorageName|Name of the storage of destination file. If not set, then default storage used
|versionId|Source file version id

### cURL example

{{< tabs "example9">}}
{{< tab "Request" >}}

```bash
curl -X PUT "https://api.groupdocs.cloud/v1.0/parser/storage/file/move/parserdocs%2Fone-page1.docx?destPath#parserdocs1%2Fone-page1.docx'&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" \
-H  "accept: application/json" \
-H  "authorization: Bearer [Access Token]"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [File API](https://apireference.groupdocs.cloud/parser/#/File) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "example10">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Move_File.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Move_File.java >}}
{{< /tab >}}
{{< /tabs >}}
