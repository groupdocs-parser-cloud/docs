---
id: "working-with-storage"
url: "parser/working-with-storage"
title: "Working With Storage"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

## Storage existence API

This API intended for checking the existence of cloud storage with a given name from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

### API Explorer

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/parser/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|**storageName**|Storage name

### cURL example

{{< tabs "example1">}}
{{< tab "Request" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/parser/storage/MyStorage/exist" \
-H  "accept: application/json" \
-H  "authorization: Bearer  [Access Token]"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
  "exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Storage existence](https://apireference.groupdocs.cloud/parser/#/Storage/StorageExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### SDK example

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Storage_Exist.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Storage_Exist.java >}}
{{< /tab >}}
{{< /tabs >}}

## Storage object existence API

This API intended for checking the existence of a file or folder in [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

### API Explorer

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/parser/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|**path**|Path of the file or folder</br>Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|versionId|File version id

### cURL example

{{< tabs "example3">}}
{{< tab "Request" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/parser/storage/exist/viewerdocs?storageName#MyStorage" \
-H  "accept: application/json" \
-H  "authorization: Bearer [Access Token]"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
  "exists": true,
  "isFolder": true
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Storage Object existence](https://apireference.groupdocs.cloud/parser/#/Storage/ObjectExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### SDK example

{{< tabs "example4">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Object_Exists.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Object_Exists.java >}}
{{< /tab >}}
{{< /tabs >}}

## Storage Space Usage API

This API intended for getting total and used space of the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)

### API Explorer

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [storage space usage API](https://apireference.groupdocs.cloud/parser/#/Storage/GetDiscUsage) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|storageName|Name of the storage. If not set, then default storage used

### cURL example

{{< tabs "example5">}}
{{< tab "Request" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/parser/storage/disc?storageName#MyStorage" \
-H  "accept: application/json" \
-H  "authorization: Bearer [Access Token]"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
  "usedSize": 31032368,
  "totalSize": 3221225472
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [storage space usage API](https://apireference.groupdocs.cloud/parser/#/Storage/GetDiscUsage) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### SDK example

{{< tabs "example6">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Get_Disc_Usage.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Get_Disc_Usage.java >}}
{{< /tab >}}
{{< /tabs >}}

## Storage File Versions API

This API intended for getting the list of file versions, stored in the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)

### API Explorer

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Storage File Versions API](https://apireference.groupdocs.cloud/parser/#/Storage/GetFileVersions) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext</br>Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### cURL example

{{< tabs "example7">}}
{{< tab "Request" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/parser/storage/version/one-page.docx?storageName#MyStorage" \
-H  "accept: application/json" \
-H  "authorization: Bearer [Access Token]"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
  "value": [
    {
      "versionId": "null",
      "isLatest": true,
      "name": "one-page.docx",
      "isFolder": false,
      "modifiedDate": "2018-08-16T19:45:05+00:00",
      "size": 347612,
      "path": "/one-page.docx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Storage File Versions API](https://apireference.groupdocs.cloud/parser/#/Storage/GetFileVersions) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### SDK example

{{< tabs "example8">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Get_File_Versions.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Get_File_Versions.java >}}
{{< /tab >}}
{{< /tabs >}}
