---
id: "working-with-folder"
url: "parser/working-with-folder"
title: "Working With Folder"
productName: "GroupDocs.Parser Cloud"
weight: 1
description: ""
keywords: ""
toc: True
---

## Get the File Listing of a Specific Folder

This API allows you to get a list of all files of a specific folder from the specified Cloud Storage. If you do not pass storage name API will find the folder in GroupDocs Cloud Storage. 

### API Explorer

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/) lets you try out [List Files in a Folder API](https://apireference.groupdocs.cloud/parser/#/Folder/GetFilesList) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|**path**|Path of the file including file name and extension e.g. /Folder1/file.ext</br>Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### cURL example

{{< tabs "example1">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
curl -X GET 'https://api.groupdocs.cloud/v1.0/parser/storage/folder/parserdocs?storageName#MyStorage' \
  -H 'accept: application/json' \
  -H "authorization: Bearer $JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
curl.exe -X GET "https://api.groupdocs.cloud/v1.0/parser/storage/folder/parserdocs?storageName#MyStorage" `
  -H "accept: application/json" `
  -H "authorization: Bearer $env:JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
curl -X GET "https://api.groupdocs.cloud/v1.0/parser/storage/folder/parserdocs?storageName#MyStorage" ^
  -H "accept: application/json" ^
  -H "authorization: Bearer %JWT_TOKEN%"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{
  "value": [
    {
      "name": "four-pages.docx",
      "isFolder": false,
      "modifiedDate": "2019-03-20T12:35:38+00:00",
      "size": 8651,
      "path": "/parserdocs/four-pages.docx"
    },
    {
      "name": "one-page.docx",
      "isFolder": false,
      "modifiedDate": "2019-03-20T12:17:34+00:00",
      "size": 351348,
      "path": "/parserdocs/one-page.docx"
    },
    {
      "name": "password-protected.docx",
      "isFolder": false,
      "modifiedDate": "2019-03-20T12:35:40+00:00",
      "size": 10240,
      "path": "/parserdocs/password-protected.docx"
    },
    {
      "name": "sample.mpp",
      "isFolder": false,
      "modifiedDate": "2019-03-20T12:29:10+00:00",
      "size": 289792,
      "path": "/parserdocs/sample.mpp"
    },
    {
      "name": "three-layouts.dwf",
      "isFolder": false,
      "modifiedDate": "2019-03-20T12:26:42+00:00",
      "size": 15433,
      "path": "/parserdocs/three-layouts.dwf"
    },
    {
      "name": "two-hidden-pages.vsd",
      "isFolder": false,
      "modifiedDate": "2019-03-20T12:17:36+00:00",
      "size": 457728,
      "path": "/parserdocs/two-hidden-pages.vsd"
    },
    {
      "name": "uses-custom-font.pptx",
      "isFolder": false,
      "modifiedDate": "2019-03-20T12:32:30+00:00",
      "size": 39823,
      "path": "/parserdocs/uses-custom-font.pptx"
    },
    {
      "name": "with-hidden-rows-and-columns.xlsx",
      "isFolder": false,
      "modifiedDate": "2019-03-20T12:17:37+00:00",
      "size": 15986,
      "path": "/parserdocs/with-hidden-rows-and-columns.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Folder API](https://apireference.groupdocs.cloud/parser/#/Folder) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example2">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Get_Files_List.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Get_Files_List.java >}}
{{< /tab >}}
{{< /tabs >}}

## Create a New Folder

This API allows you to create a new folder in the specified Cloud Storage. If you do not pass storage name API will create New Folder in default Cloud Storage.

### API Explorer

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/) lets you try out [Create Folder API](https://apireference.groupdocs.cloud/parser/#/Folder/CreateFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|**path**|Target folder’s path e.g. Folder1/Folder2/. The folders will be created recursively</br>Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### cURL example

{{< tabs "example3">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
curl -X POST 'https://api.groupdocs.cloud/v1.0/parser/storage/folder/parserdocs?storageName#MyStorage' \
  -H 'accept: application/json' \
  -H "authorization: Bearer $JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
curl.exe -X POST "https://api.groupdocs.cloud/v1.0/parser/storage/folder/parserdocs?storageName#MyStorage" `
  -H "accept: application/json" `
  -H "authorization: Bearer $env:JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
curl -X POST "https://api.groupdocs.cloud/v1.0/parser/storage/folder/parserdocs?storageName#MyStorage" ^
  -H "accept: application/json" ^
  -H "authorization: Bearer %JWT_TOKEN%"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{  
  "code": 200,
  "status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Folder API](https://apireference.groupdocs.cloud/parser/#/Folder/) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "example4">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Create_Folder.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Create_Folder.java >}}
{{< /tab >}}
{{< /tabs >}}

## Delete a Particular Folder

This API allows you to delete a particular folder in the specified Cloud Storage. If you do not pass storage name API will create New Folder in default Cloud Storage. To remove recursively inner folder/files you need to pass true value to a recursive parameter in Request. If it is set to false and folder contains data then API throws the exception.

### API Explorer

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Delete a Particular Folder API](https://apireference.groupdocs.cloud/parser/#/Folder/DeleteFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|**path**|Folder path e.g. /Folder1</br>Required. Can be passed as a query string parameter or as part of the URL
|storageName|Name of the storage. If not set, then default storage used

### cURL example

{{< tabs "example5">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
curl -X DELETE 'https://api.groupdocs.cloud/v1.0/parser/storage/folder/parserdocs?storageName#MyStorage&#x26;recursive#true' \
  -H 'accept: application/json' \
  -H "authorization: Bearer $JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
curl.exe -X DELETE "https://api.groupdocs.cloud/v1.0/parser/storage/folder/parserdocs?storageName#MyStorage&#x26;recursive#true" `
  -H "accept: application/json" `
  -H "authorization: Bearer $env:JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
curl -X DELETE "https://api.groupdocs.cloud/v1.0/parser/storage/folder/parserdocs?storageName#MyStorage&#x26;recursive#true" ^
  -H "accept: application/json" ^
  -H "authorization: Bearer %JWT_TOKEN%"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{  
  "code": 200,
  "status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Delete Folder API](https://apireference.groupdocs.cloud/parser/#/Folder/DeleteFolder) calls and lets you use GroupDocs for Cloud features in a native way for your preferred language.

{{< tabs "example6">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Delete_Folder.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Delete_Folder.java >}}
{{< /tab >}}
{{< /tabs >}}

## Copy Specific Folder

This API allows you to copy a Folder to another location in the GroupDocs Cloud Storage. If you do not pass source and destination storage names API will copy Folder within default Cloud Storage.

### API Explorer

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Copy Folder API](https://apireference.groupdocs.cloud/parser/#/Folder/CopyFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|**srcPath**|Source folder path e.g. /Folder1</br>Required. Can be passed as a query string parameter or as part of the URL
|**destPath**|Destination folder path. Required
|srcStorageName|Name of the storage of source folder. If not set, then default storage used
|destStorageName|Name of the storage of destination folder. If not set, then default storage used

### cURL example

{{< tabs "example7">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
curl -X PUT 'https://api.groupdocs.cloud/v1.0/parser/storage/folder/copy/parserdocs?destPath#viewerdocs1&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage' \
  -H 'accept: application/json' \
  -H "authorization: Bearer $JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
curl.exe -X PUT "https://api.groupdocs.cloud/v1.0/parser/storage/folder/copy/parserdocs?destPath#viewerdocs1&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" `
  -H "accept: application/json" `
  -H "authorization: Bearer $env:JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
curl -X PUT "https://api.groupdocs.cloud/v1.0/parser/storage/folder/copy/parserdocs?destPath#viewerdocs1&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" ^
  -H "accept: application/json" ^
  -H "authorization: Bearer %JWT_TOKEN%"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{  
  "code": 200,
  "status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Copy Folder API](https://apireference.groupdocs.cloud/parser/#/Folder/CopyFolder) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example8">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Copy_Folder.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud 4b05c33e76577ff3c4e35778db3f5ad5 Viewer_Java_Copy_Folder.java >}}
{{< /tab >}}
{{< /tabs >}}

## Move a Specific Folder

This API allows you to move a folder to another location in the GroupDocs Cloud Storage. If you do not pass source and destination storage names API will move Folder within default Cloud Storage.

### API Explorer

[GroupDocs.Parser Cloud API Reference](https://apireference.groupdocs.cloud/parser/#/) lets you try out [Move a Folder API](https://apireference.groupdocs.cloud/parser/#/Folder/MoveFolder) right away in your browser. It allows you to effortlessly interact and try out every single operation that our APIs expose.

### Request parameters

|Parameter|Description
|---|---
|**srcPath**|Source folder path e.g. /Folder1</br>Required. Can be passed as a query string parameter or as part of the URL
|**destPath**|Destination folder path. Required
|srcStorageName|Name of the storage of source folder. If not set, then default storage used
|destStorageName|Name of the storage of destination folder. If not set, then default storage used

### cURL example

{{< tabs "example9">}}
{{< tab "Linux/MacOS/Bash" >}}

```bash
curl -X PUT 'https://api.groupdocs.cloud/v1.0/parser/storage/folder/move/parserdocs?destPath#viewerdocs1&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage' \
  -H 'accept: application/json' \
  -H "authorization: Bearer $JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows PowerShell" >}}

```powershell
curl.exe -X PUT "https://api.groupdocs.cloud/v1.0/parser/storage/folder/move/parserdocs?destPath#viewerdocs1&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" `
  -H "accept: application/json" `
  -H "authorization: Bearer $env:JWT_TOKEN"
```

{{< /tab >}}

{{< tab "Windows CMD" >}}

```cmd
curl -X PUT "https://api.groupdocs.cloud/v1.0/parser/storage/folder/move/parserdocs?destPath#viewerdocs1&#x26;srcStorageName#MyStorage&#x26;destStorageName#MyStorage" ^
  -H "accept: application/json" ^
  -H "authorization: Bearer %JWT_TOKEN%"
```

{{< /tab >}}
{{< tab "Response" >}}

```json
{  
  "code": 200,
  "status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

### SDK examples

Our API is completely independent of your operating system, database system or development language. You can use any language and platform that supports HTTP to interact with our API. However, manually writing client code can be difficult, error-prone and time-consuming. Therefore, we have provided and support API [SDKs](https://github.com/groupdocs-parser-cloud) in many development languages in order to make it easier to integrate with us. If you use [SDK](https://github.com/groupdocs-parser-cloud), it hides the [Move Folder API](https://apireference.groupdocs.cloud/parser/#/Folder/MoveFolder) calls and lets you use GroupDocs Cloud features in a native way for your preferred language.

{{< tabs "example10">}}
{{< tab "C#" >}}
{{< gist groupdocscloud 39135fbf5cfb74deeeae6c47eafb2473 Parser_CSharp_Move_Folder.cs >}}
{{< /tab >}}
{{< tab "Java" >}}
{{< gist groupdocscloud c8b8e01a52ef2bae6fa5d78aba152238 Parser_Java_Move_Folder.java >}}
{{< /tab >}}
{{< /tabs >}}
