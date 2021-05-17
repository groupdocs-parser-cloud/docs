---
id: "working-with-storage"
url: "parser/working-with-storage"
title: "Working With Storage"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
---






## Storage existence API ##

This API intended for checking the existence of cloud storage with a given name from [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

### API Explorer ###

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/parser/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

#### Request parameters ####

|Parameter|Description
|---|---
|**storageName**|Storage name

### cURL Example ###

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/parser/storage/MyStorage/exist" \
-H  "accept: application/json" \
-H  "authorization: Bearer  [Access Token]"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

### SDKs ###

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Storage existence](https://apireference.groupdocs.cloud/parser/#/Storage/StorageExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### SDK Examples ####

{{< tabs tabTotal="2" tabID="2" tabName1="C#" tabName2="Java" >}}
{{< tab tabNum="1" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Storage_Exist.cs >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Storage_Exist.java >}}
{{< /tab >}}
{{< /tabs >}}

## Storage object existence API ##

This API intended for checking the existence of a file or folder in [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud).

### API Explorer ###

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Storage existence API](https://apireference.groupdocs.cloud/parser/#/Storage/StorageExists) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

#### Request parameters ####

|Parameter|Description
|---|---
|**path**|Path of the file or folder</br>Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used
|versionId|File version id

### cURL Example ###

{{< tabs tabTotal="2" tabID="3" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/parser/storage/exist/viewerdocs?storageName#MyStorage" \
-H  "accept: application/json" \
-H  "authorization: Bearer [Access Token]"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "exists": true,
  "isFolder": true
}
```

{{< /tab >}}
{{< /tabs >}}

### SDKs ###

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Storage Object existence](https://apireference.groupdocs.cloud/parser/#/Storage/ObjectExists) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### SDK Examples ####

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Java" >}}
{{< tab tabNum="1" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Object_Exists.cs >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Object_Exists.java >}}
{{< /tab >}}
{{< /tabs >}}

## Storage Space Usage API ##

This API intended for getting total and used space of the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)

### API Explorer ###

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [storage space usage API](https://apireference.groupdocs.cloud/parser/#/Storage/GetDiscUsage) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

#### Request parameters ####

|Parameter|Description
|---|---
|storageName|Name of the storage. If not set, then default storage used

### cURL Example ###

{{< tabs tabTotal="2" tabID="5" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/parser/storage/disc?storageName#MyStorage" \
-H  "accept: application/json" \
-H  "authorization: Bearer [Access Token]"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "usedSize": 31032368,
  "totalSize": 3221225472
}
```

{{< /tab >}}
{{< /tabs >}}

### SDKs ###

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [storage space usage API](https://apireference.groupdocs.cloud/parser/#/Storage/GetDiscUsage) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### SDK Examples ####

{{< tabs tabTotal="2" tabID="6" tabName1="C#" tabName2="Java" >}}
{{< tab tabNum="1" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Get_Disc_Usage.cs >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Get_Disc_Usage.java >}}
{{< /tab >}}
{{< /tabs >}}

## Storage File Versions API ##

This API intended for getting the list of file versions, stored in the [GroupDocs Cloud Storage](https://dashboard.groupdocs.cloud)

### API Explorer ###

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Storage File Versions API](https://apireference.groupdocs.cloud/parser/#/Storage/GetFileVersions) right away in your browser! It allows you to effortlessly interact and try out every single operation our APIs expose.

### Request parameters ###

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext</br>Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### cURL Example ###

{{< tabs tabTotal="2" tabID="7" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.groupdocs.cloud/v1.0/parser/storage/version/one-page.docx?storageName#MyStorage" \
-H  "accept: application/json" \
-H  "authorization: Bearer [Access Token]"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

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

### SDKs ###

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Storage File Versions API](https://apireference.groupdocs.cloud/parser/#/Storage/GetFileVersions) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

#### SDK Examples ####

{{< tabs tabTotal="2" tabID="8" tabName1="C#" tabName2="Java" >}}
{{< tab tabNum="1" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Get_File_Versions.cs >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Get_File_Versions.java >}}
{{< /tab >}}
{{< /tabs >}}
